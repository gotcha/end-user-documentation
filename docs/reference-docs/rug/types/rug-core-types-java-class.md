
## Type: `java.class`
**Java class**

### `java.class` Operations


#### Operation: `addAnnotation`
    Annotate the element with the given annotation

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***pkg*** | `class java.lang.String` | *Package where the annotation is sourced* |
| ***annotation*** | `class java.lang.String` | *The annotation to add* |


#### Operation: `addImport`
    Add an import to the containing Java source

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***fqn*** | `class java.lang.String` | *The fully qualified name of the import* |


#### Operation: `blockingProblem`
    Report a severe, blocking problem

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `interface com.atomist.rug.runtime.FunctionInvocationContext` | ** |


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


#### Operation: `hasAnnotation`
    Does the element have the given annotation?

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***annotation*** | `class java.lang.String` | *The string name of the annotation to look for* |


#### Operation: `lineCount`
    Line count

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


#### Operation: `movePackage`
    Move the type to the given package

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***newPackage*** | `class java.lang.String` | *The package to move the type to* |


#### Operation: `name`
    Return the name of the type

***Parameters***

*None*


#### Operation: `pkg`
    Return the package

***Parameters***

*None*


#### Operation: `println`
    Cause the editor to print to the console. Useful for debugging if running editors locally.

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |


#### Operation: `rename`
    Rename the type

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***newName*** | `class java.lang.String` | *The new name of the type* |


#### Operation: `renameByReplace`
    Rename the type by replacing a pattern in the name

***Parameters***


| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***target*** | `class java.lang.String` | *The name of the type to replace* |
| ***replacement*** | `class java.lang.String` | *The replacement pattern* |
