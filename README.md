Advanced Integrated System for Project Coordination and Task Management Excellence
Features
The following features have been implemented:

Manage tasks through a Kanban board interface (set due dates, labels, add checklists)
View all your current assigned tasks through the My Tasks view
Personal projects
Task comments and activity
This project is still in active development, so some options may not be fully implemented yet.

For updates on development, join the Discord server.

For a list of planned features, check out the Roadmap!

Installation
With Docker & Docker Compose
You'll need both Docker & Docker Compose installed.

First, clone the repository and navigate to the project directory:

sh
Copy code
git clone <repository_url> && cd taskcafe
Now, start the services:

sh
Copy code
docker-compose -p taskcafe up -d
This will start a Postgres instance as well as a Taskcafe instance.

Visit http://localhost:3333 to access the installation screen and create the first system user.

From Source
You'll need Golang installed on your machine.

Next, clone the repository and navigate to the project directory:

sh
Copy code
git clone <repository_url> && cd taskcafe
Build the binary using Mage:

sh
Copy code
go run cmd/mage/main.go install
go run cmd/mage/main.go build
This will:

Install all yarn packages for the frontend
Build the React frontend
Embed the React frontend in the binary
Compile the final executable binary
The newly created taskcafe binary can be found in the dist folder. It contains everything necessary to run except the config file. An example config file can be found in conf/app.example.toml.

For more information on configuration, please read the wiki. The config will need to be copied to conf/app.toml in the same place the binary is.

Make sure to fill out the database section of the config in order to connect it to your database.

Run the database migrations with:

sh
Copy code
taskcafe migrate
Now you can run the web interface by executing:

sh
Copy code
taskcafe web
A more detailed guide for installing on Ubuntu/Debian is available.

How is This Different from Other Tools (Trello, NextCloud, etc.)?
One of the primary goals of this project is to provide a project management tool that fits personal workflows and is enjoyable to use for personal projects.

During alpha development, the focus is on building "basic" features—features that are standard across all Kanban boards/project management tools.

Once out of alpha, many features will be added to differentiate this product from others (check out the Roadmap for ideas on future plans).

Contributing & Community
If you have questions regarding how to use this project, check out the Discord server.

If you're interested in contributing, please read the contribution guide first!

There is also a Code of Conduct to follow.

License
This project is licensed under the MIT License.
