# Builder

This repository contains the [Builder](https://buildpacks.io/docs/concepts/components/builder/) 
used for code submissions on [CodeCrafters](https://codecrafters.io/).

### Contract

- Given source code, outputs an OCI image along with logs relevant to builds.
- A tester can be mounted into this OCI image and used to test the code submission.

### Functionality

- Detects the language of the submission.
- Installs programming language, caching as much as possible.
- Installs dependencies, caching as much as possible.
- Outputs friendly logs for any operations that aren't cached.

### Testing Locally

Many of the scripts in this repository aren't customized to work on MacOS, so we use Vagrant to test this locally.

1. Create your Vagrant VM:

```shell
vagrant up
```

2. SSH into the VM and run tests using a sample configuration.
