- When there is a valid go.mod file in the root of your project directory, your project is a
  module.
- Here are a few of the key advantages of setting up a project as a module:
  - Improved Dependency Management
  - Versioning and Package Distribution
  - Enhanced Project Isolation
  - Reproducible Builds
  - Simplified Project Setup - `go mod init`
  - Better Tooling Support
  - Decentralized Code Management
  - Compatibility with Older Versions

## Routing Requests

- It's better to skip using http.DefaultServeMux and those related helper functions. Go for your own servemux that's scoped just to your project.
