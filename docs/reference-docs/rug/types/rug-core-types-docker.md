
## Type: `docker`
**Docker file type**

### `docker` Operations


#### Operation: `addAdd`
    Add ADD directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***addContents*** | `class java.lang.String` | *The contents of the ADD directive* |


#### Operation: `addCopy`
    Add COPY directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***copyContents*** | `class java.lang.String` | *The contents of the COPY directive* |


#### Operation: `addEnv`
    Add Env directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***envContents*** | `class java.lang.String` | *The contents of the Env directive* |


#### Operation: `addExpose`
    Add EXPOSE directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***exposeContents*** | `class java.lang.String` | *The contents of the EXPOSE directive* |


#### Operation: `addLabel`
    Add LABEL directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***labelContents*** | `class java.lang.String` | *The contents of the LABEL directive* |


#### Operation: `addMaintainer`
    Add MAINTAINER directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***maintainerContents*** | `class java.lang.String` | *The contents of the MAINTAINER directive* |


#### Operation: `addOrUpdateCmd`
    Add or update CMD directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***cmdContents*** | `class java.lang.String` | *The contents of the CMD directive* |


#### Operation: `addOrUpdateEntryPoint`
    Add or update ENTRYPOINT directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***entrypointContent*** | `class java.lang.String` | *The contents of the ENTRYPOINT directive* |


#### Operation: `addOrUpdateExpose`
    Add or update EXPOSE directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***exposeContents*** | `class java.lang.String` | *The contents of the EXPOSE directive* |


#### Operation: `addOrUpdateFrom`
    Add or update FROM directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***fromContents*** | `class java.lang.String` | *The contents of the FROM directive* |


#### Operation: `addOrUpdateLabel`
    Add or update LABEL directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***labelContents*** | `class java.lang.String` | *The contents of the LABEL directive* |


#### Operation: `addOrUpdateMaintainer`
    Add or update MAINTAINER directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***maintainerContents*** | `class java.lang.String` | *The contents of the MAINTAINER directive* |


#### Operation: `addOrUpdateWorkdir`
    Add or update WORKDIR directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***workdirContents*** | `class java.lang.String` | *The contents of the WORKDIR directive* |


#### Operation: `addRun`
    Add RUN directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***runContents*** | `class java.lang.String` | *The contents of the RUN directive* |


#### Operation: `addVolume`
    Add VOLUME directive

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***volumeContents*** | `class java.lang.String` | *The contents of the VOLUME directive* |


#### Operation: `blockingProblem`
    Report a severe, blocking problem

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `interface com.atomist.rug.runtime.FunctionInvocationContext` | ** |


#### Operation: `content`
    Return file content

***Parameters***

*None*


#### Operation: `eval`
    Operate on this. Use when you want to operate on an object in an embedded language such as JavaScript or Clojure

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***arg0*** | `class java.lang.Object` | ** |


#### Operation: `fail`
    Cause the operation to fail with a fatal error

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |


#### Operation: `filename`
    Return file name, excluding path

***Parameters***

*None*


#### Operation: `lineCount`
    Return the number of lines in the file

***Parameters***

*None*


#### Operation: `majorProblem`
    Report a major problem

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `interface com.atomist.rug.runtime.FunctionInvocationContext` | ** |


#### Operation: `minorProblem`
    Report a minor problem

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `interface com.atomist.rug.runtime.FunctionInvocationContext` | ** |


#### Operation: `path`
    Return file path, with forward slashes

***Parameters***

*None*


#### Operation: `println`
    Cause the editor to print to the console. Useful for debugging if running editors locally.

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |


#### Operation: `underPath`
    Does this path begin with the given pattern? Pattern should contain slashes but not begin with a /

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***root*** | `class java.lang.String` | *The root path to begin searching from* |
