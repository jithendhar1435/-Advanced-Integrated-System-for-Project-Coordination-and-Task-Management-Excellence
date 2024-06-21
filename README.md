## Comprehensive Task Management and Collaboration Platform for Enhanced Productivity and Workflow Optimization

[![Discord](https://img.shields.io/discord/753094126684053574.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/your-invite-code) [![Releases](https://img.shields.io/github/release-date/JordanKnott/taskcafe)](https://github.com/JordanKnott/taskcafe/releases) [![Docker pulls](https://img.shields.io/docker/pulls/jordanknott/taskcafe)](https://hub.docker.com/r/jordanknott/taskcafe) [![Go Report Card](https://goreportcard.com/badge/github.com/JordanKnott/taskcafe)](https://goreportcard.com/report/github.com/JordanKnott/taskcafe)

[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://www.paypal.me/your-donate-link)

---

This advanced task management and collaboration platform is designed to significantly enhance productivity and optimize workflow processes for both individuals and teams. Featuring an intuitive Kanban board interface, this platform is built to handle the complexity and nuances of modern project management needs.

### Features
The following features have been implemented:

- **Kanban Board Interface**: Manage tasks effortlessly with due dates, labels, and checklists.
- **My Tasks View**: Consolidate all assigned tasks in a single, easy-to-navigate view.
- **Personal Projects**: Create and manage projects independently.
- **Task Comments and Activity**: Enhance team collaboration with integrated comments and activity tracking.

This project is still in active development, with many more features on the way. For updates on development, join our [Discord server](https://discord.gg/your-invite-code). Check out the [Roadmap](https://github.com/JordanKnott/taskcafe/projects/1) for planned features.

### Installation
#### With Docker & Docker-Compose
Ensure you have Docker and Docker-Compose installed. Then follow these steps:

```sh
git clone https://github.com/JordanKnott/taskcafe && cd taskcafe
docker-compose -p taskcafe up -d
```

Visit [http://localhost:3333](http://localhost:3333) to complete the initial setup by creating the first system user.

#### From Source
Make sure Golang is installed on your machine. Then proceed with:

```sh
 && cd taskcafe
go run cmd/mage/main.go install
go run cmd/mage/main.go build
```

This process will:
- Install Yarn packages for the frontend.
- Build the React frontend and embed it in the binary.
- Compile the final executable binary found in the `dist` folder.

Copy the example config file `conf/app.example.toml` to `conf/app.toml` and configure it accordingly. Run database migrations with:

```sh
taskcafe migrate
```

Launch the web interface with:

```sh
taskcafe web
```

For a detailed installation guide on Ubuntu/Debian, refer to the [Wiki](https://github.com/JordanKnott/taskcafe/wiki).

### Comparison with Other Tools
Unlike other project management tools such as Trello or NextCloud, this platform is tailored to fit a unique workflow that prioritizes user preferences and enhances task management efficiency. While currently focused on delivering fundamental features, future updates will introduce advanced functionalities that distinguish this platform from its competitors.

### Contributing & Community
Join our [Discord server](https://discord.gg/your-invite-code) for support and community discussions. If you're interested in contributing, please read the [Contribution Guide](https://github.com/JordanKnott/taskcafe/blob/master/CONTRIBUTING.md) and adhere to our [Code of Conduct](https://github.com/JordanKnott/taskcafe/blob/master/CODE_OF_CONDUCT.md).

### License
This platform is licensed under the [MIT License](https://github.com/JordanKnott/taskcafe/blob/master/LICENSE).

---

Your feedback and contributions are invaluable in making this platform better. Please consider [donating](https://www.paypal.me/your-donate-link) to support the ongoing development of this project.
