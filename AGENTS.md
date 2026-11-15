# Project instructions

## Dependency execution and isolation

The user does not want npm or potentially untrusted dependency scripts running
directly on their machine because of malware concerns.

- Run npm, package installation, dependency lifecycle scripts, builds, and tests
  only inside Docker containers. Do not run them directly on the host.
- Do not download or install a host Node.js/npm runtime for this project.
- Give containers only the project files and access needed for the task. Do not
  mount the user's home directory, credentials, or Docker socket into build or
  test containers. Do not use privileged containers.
- Keep the final serving image limited to the compiled app and its web server.
- If Docker access is unavailable, explain the blocker instead of falling back
  to host npm execution. Ask the user to perform any necessary administrator
  authentication in their own terminal; never request their password in chat.
