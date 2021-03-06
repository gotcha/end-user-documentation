## Rug CLI Commands and Syntax

This page documents syntax and functionality of the Rug CLI.

*Note:* All commands listed below are provided only as examples of the
syntax.  They may refer to Rugs and Rug archives that do not exist and
therefore may not work.

### Configuring

In order to use the CLI the following file named `cli.yml` needs to be
placed in `~/.atomist`.  The contents of the simplest possible
`cli.yml` are below.

```yaml
# Set up the path to the local repository
local-repository:
  path: "${user.home}/.atomist/repository"

# Set up remote repositories to query for Rug archives. Additionally one of the
# repositories can also be enabled for publication (publish: true).
remote-repositories:
  maven-central:
    publish: false
    url: "http://repo.maven.apache.org/maven2/"
  rug-types:
    publish: false
    url: "https://atomist.jfrog.io/atomist/libs-release"
  rugs:
    publish: false
    url: "https://atomist.jfrog.io/atomist/rugs-release"
```

The Rug CLI will create the above `cli.yml` if you do not already have
one.

### Commands

The CLI will assume the current working directory to be the root for execution.

#### Using the CLI as Rug users

##### Invoking Editors

Run an editor as follows:

```sh
$ rug edit atomist:common-editors:AddReadme --artifact-version 1.0.0 parameter1=foo parameter2=bar

$ rug edit atomist:common-editors:AddReadme parameter1=foo parameter2=bar
```

`artifact-version` is optional and defaults to `latest` semantics.
`--change-dir` or `-C` for giving a generator a target directory.

##### Invoking Generators

```sh
$ rug generate "atomist-project-templates:spring-rest-service:Spring Boot Microservice" \
    --artifact-version 1.0.0 MyNewProjectName parameter1=foo parameter2=bar

$ rug generate "atomist-project-templates:spring-rest-service:Spring Boot Microservice" \
    MyNew Project parameter1=foo parameter2=bar
```

`artifact-version` is optional and defaults to `latest` semantics.
`--change-dir` or `-C` for giving a generator a target directory.

##### Describing Rug Artifacts

In order to list all parameters, describing an artifact is available in the
following form:

```sh
$ rug describe archive atomist-project-templates:spring-rest-service

$ rug describe editor "atomist-project-templates:spring-rest-service:Spring Boot Microservice" \
  --artifact-version 1.0.0

$ rug describe generator "atomist-project-templates:spring-rest-service:Spring Boot Microservice" \
  --artifact-version 1.0.0
```

##### Listing Local Archives

To list all locally available Rug archives, the following command can be used:

```sh
$ rug list -f version="[1.2,2.0)" -f group=*atomist* -f artifact=*sp?ing*
```

The local listing can be filtered by using `-f` filter expressions on `group`,
`artifact` and `version`. `group` and `artifact` support wildcards of `*` and `?`.
`version` takes any version constraint.

#### Using the CLI as Rug developer

All the following commands need to executed from within the Rug project directory.

##### Running Tests

To run all tests:

```sh
$ rug test
```

To run a specific named test:

```sh
$ rug test "Whatever Test Secanrio"
```

To run all scenarios from a .rt file:

```sh
$ rug test MyRugTestFilename
```

##### Installing a Rug archive

Creating a Rug zip archive and installing it into the local repository
can be done with the following command:

```sh
$ rug install
```

This command packages the project into a zip archive, creates a Pom
and installs both into the local repository under, usually
`.atomist/repository`.

### Dependency Resolution

The Rug CLI will automatically resolve and download the dependencies
of the given Rug archive when `edit` or `generate` is invoked. The
archives along with their dependencies will be downloaded to a local
repo (not the one in the user's home directory) via Aether and
resolved from there.

Therefore running above commands is a two step process:

1.  Search and resolve (eventually download) the archive referenced in
    the command. The result of a resolution is cached for 60mins or
    until the `manifest.yml` is changed
2.  Start up `rug-lib` passing parameters over to run the editor or
    generator

### Advanced Topics

#### Turning on Verbose output for Debugging

If you want a more verbose output that includes any exceptions that
Rug command may have encountered, please add `-X` to your command.
For example:

```sh
$ rug test -X
```
