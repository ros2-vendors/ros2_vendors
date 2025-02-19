# Running ROS 2 Vendors Repos Check Workflow Locally

This workflow validates `.repos` and `.yaml` files in the repository. You can test it locally using the `act` tool.

## Prerequisites

Ensure that `act` is installed. You can install it with:

```bash
$ curl https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash
```

### Simulate a Pull Request Event

```bash
$ act pull_request
```

### Simulate a Manual Trigger (`workflow_dispatch`)

```bash
$ act workflow_dispatch
```

### Using a Custom Image (Recommended for `ubuntu-latest` Compatibility)

```bash
$ act pull_request --container-architecture linux/amd64 -P ubuntu-latest=ghcr.io/catthehacker/ubuntu:latest
```

