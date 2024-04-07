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

## `fmt.Fprintf()` vs `fmt.Sprintf()`

`fmt.Fprintf()`: Used for writing formatted output to a specific writer (e.g., file, buffer). It's about outputting the formatted text to somewhere.

`fmt.Sprintf()`: Used for creating a formatted string without immediately outputting it anywhere. It's about getting the formatted text as a string for use in your code.

## Content sniffing

Go automatically sets the `Content-Type` header using `http.DetectContentType()` under the hood. But this function can’t distinguish JSON from plain text. So, by default, JSON responses will be sent with a `Content-Type: text/plain; charset=utf-8` header. We can prevent this doing something like this:

```
w.Header().Set("Content-Type", "application/json")
```
