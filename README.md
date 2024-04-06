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

## Non-idempotent action

Idempotence is a property of some operations in mathematics and computer science whereby they can be applied multiple times without changing the result beyond the initial application.

In the context of HTTP and web services, an action is said to be "non-idempotent" if performing it more than once has different effects than doing it a single time.

For example, the HTTP GET method is idempotent because calling it once or several times in a row on the same URL will return the same result without changing the server's state (assuming no changes to the resource in the meantime). On the other hand, the POST method is typically used for non-idempotent actions. When you POST data to a server, you're usually asking it to create or change a resource. If you send the same POST request multiple times, it will likely create multiple resources or make multiple changes, each time altering the server's state.
