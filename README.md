# Docker Ansible Role
Provides a base docker installation.

## Configuration
| Key | Description |
|-----|-------------|
| docker_version           | The version of docker to be installed. Wildcards may be used. |
| docker_yum_repo_url      | The URL of the Docker YUM repository. |
| docker_yum_repo_gpg      | The GPG key used to validate Docker RPM packages. |
| docker_daemon_json_data  | The docker daemon.json configuration, represented as a JSON string. |
| docker_insecure_registry | Any insecure registries to be configured, eg. 'localhost:5000'. |
