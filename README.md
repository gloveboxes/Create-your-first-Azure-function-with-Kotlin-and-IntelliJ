# Creating your first Kotlin Azure Function

## References

[Create your first Azure function with Java and IntelliJ](https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-maven-intellij)

[Java Bindings]()

## Setting up Developer Environment

## Set up your development environment

To develop a function with Java and IntelliJ, install the following software:

- [Java Developer Kit](https://www.azul.com/downloads/zulu/) (JDK), version 8
- [Apache Maven](https://maven.apache.org), version 3.0 or higher
- [IntelliJ IDEA](https://www.jetbrains.com/idea/download), Community or Ultimate versions with Maven
- [Azure CLI](https://docs.microsoft.com/cli/azure)

> The JAVA_HOME environment variable must be set to the install location of the JDK to complete the steps in this article.

 We recommend that you install [Azure Functions Core Tools, version 2](functions-run-local.md#v2). It provides a local development environment for writing, running, and debugging Azure Functions.

## Create a Functions project

1. In IntelliJ IDEA, select **Create New Project**.  
1. In the **New Project** window, select **Maven** from the left pane.
1. Select the **Create from archetype** check box, and then select **Add Archetype** for the [azure-functions-archetype](https://mvnrepository.com/artifact/com.microsoft.azure/azure-functions-archetype).
1. In the **Add Archetype** window, complete the fields as follows:
    - _GroupId_: com.microsoft.azure
    - _ArtifactId_: azure-functions-archetype
    - _Version_: Use the latest version from [the central repository](https://mvnrepository.com/artifact/com.microsoft.azure/azure-functions-archetype)
    ![Create a Maven project from archetype in IntelliJ IDEA](media/functions-create-first-java-intellij/functions-create-intellij.png)  
1. Select **OK**, and then select **Next**.
1. Enter your details for current project, and select **Finish**.

Maven creates the project files in a new folder with the same name as the _ArtifactId_ value. The project's generated code is a simple [HTTP-triggered](/azure/azure-functions/functions-bindings-http-webhook) function that echoes the body of the triggering HTTP request.

![create new kotlin project](./resources/create-new-project.jpg)

![create new kotlin project](./resources/create-new-project-properties.jpg)

![create new kotlin project](./resources/create-new-project-confirmation.jpg)

![create new kotlin project](./resources/create-new-project-enable-auto-import.jpg)

## Azure Configuration

By default the pom.xml file is opened when the project is created.

You can set the 

1. Function App Name
2. Function App Region

Run the following command for a complete list of regions. Choose the location by the "name" field in the returned json array. 

```bash
az account list-locations
```

![create new kotlin project](./resources/create-new-project-skelton.jpg)

![create new kotlin project](./resources/project-default-http-trigger.jpg)

![create new kotlin project](./resources/project-convert-to-kotlin.jpg)

![create new kotlin project](./resources/project-converted-to-kotlin.jpg)

![create new kotlin project](./resources/project-configure-kotlin-in-project.jpg)

![create new kotlin project](./resources/project-configure-kotlin-in-project-confirm.jpg)

![create new kotlin project](./resources/project-clean-package-run.jpg)

![create new kotlin project](./resources/project-clean-package-results.jpg)

![create new kotlin project](./resources/project-azure-functions-run.jpg)

![create new kotlin project](./resources/project-test-http-trigger.jpg)

![create new kotlin project](./resources/project-azure-functions-stop.jpg)

![create new kotlin project](./resources/project-enable-debug-azure-function-maven-debug.jpg)

![create new kotlin project](./resources/project-enable-debug-azure-function-maven-debug-configure.jpg)

![create new kotlin project](./resources/project-run-edit-configurations.jpg)

![create new kotlin project](./resources/project-run-edit-configurations-add-remote-config.jpg)


![create new kotlin project](./resources/project-run-edit-configurations-add-remote-attach-debugger.jpg)

![create new kotlin project](./resources/project-debug-set-breakpoint.jpg)

![create new kotlin project](./resources/project-debug-run-debug-enabled-maven.jpg)

![create new kotlin project](./resources/project-debug-select-attach-debugger.jpg)

![create new kotlin project](./resources/project-debug-debugger-attached.jpg)

![create new kotlin project](./resources/project-debug-switch-to-run.jpg)

![create new kotlin project](./resources/project-debug-step-through-code.jpg)

![create new kotlin project](./resources/project-debugger-stop.jpg)