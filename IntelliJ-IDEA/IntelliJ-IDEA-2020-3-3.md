# IntelliJ IDEA 2020.3.3 Is Available

[Irina Maryasova](https://blog.jetbrains.com/author/irina-maryasova-jetbrains-com) March 16, 2021

The new bug-fix update for IntelliJ IDEA 2020.3.3 is out! You can update to the new version from inside the IDE, with the Toolbox App, or using snaps if you are an Ubuntu user. It is also available for download from [our website](https://www.jetbrains.com/idea/download/?_ga=2.180702247.1486359510.1616506392-980181392.1600866411#section=mac).

In this release, we’ve added an important new feature:

### Trusted projects 可信任项目

IntelliJ IDEA 2020.3.3 introduces the concept of **trusted projects**, designed to mitigate the risks associated with opening projects from unknown and untrusted sources.

Many modern build systems, including Maven and Gradle, rely on code execution for building the project model that the IDE needs in order to understand the project structure and its dependencies. In Gradle, the build script itself is code written in either Groovy or Kotlin. In Gradle and Maven, the build script can reference plugins – the build system will download the plugins from locations specified in the build scripts and execute code in those plugins.

In addition to the issues inherent to the Maven and Gradle design, some of IntelliJ IDEA’s features (for example, startup tasks) introduce additional code execution possibilities enabled by sharing a project together with its .idea directory.

Thus, the simple act of opening a project in the IDE could lead to code execution from the project build scripts. If a malicious actor creates the project, this can be a significant security risk. Unfortunately, the risk is not merely hypothetical – there have been recent attempts to [attack security researchers](https://blog.google/threat-analysis-group/new-campaign-targeting-security-researchers/) by sending them Visual Studio projects containing malicious code.

We’ve introduced **trusted projects** to mitigate these risks. When you open a project, IntelliJ IDEA doesn’t execute any code from it and checks whether it is trusted or from a trusted location. If the project currently is not trusted, the IDE will ask you to choose whether to open it in **safe** mode or **full-trust** mode. If you open a project in safe mode, the IDE will disable all potential code execution upon opening. Since this makes it impossible to build an accurate project model, many IDE features, such as error highlighting, will be disabled. However, you can still browse the project’s contents and open its source files in the editor.

当您打开一个项目时，IntelliJ IDEA不会执行项目的任何代码，并检查它是可信的或是来自可信的位置。如果项目当前不可信，ide将要求您选择是在**安全模式（safe mode）**下打开它，或者是在**完全信任模式（full-trust mode）**下打开它。如果您以**安全模式**打开一个项目，idea将在打开时，禁用所有可能的代码执行。自此许多IDE特性，比如错误高亮显示将被禁用。但是，您仍然可以在编辑器中浏览项目的内容和打开其源文件。

![Trusted Projects](https://blog.jetbrains.com/wp-content/uploads/2021/03/Trusted-projects.png)

The same protections also apply to other build systems (e.g. sbt) and project types (e.g. Python and JavaScript).

To avoid showing warnings for every project, the IDE allows you to define **trusted locations** in Preferences/_Settings | Build, Execution, Deployment | Trusted Locations_. Projects in directories specified as “Trusted Locations” are always considered trusted. To ensure that you get the untrusted project warnings only when something out of the ordinary is happening, we recommend adding the directory where you usually create projects to your trusted locations.

建议将通常创建项目的目录添加到可信的位置：

![Trusted locations settings ](https://blog.jetbrains.com/wp-content/uploads/2021/03/Trusted-locations-settings.png)

If you want to disable the untrusted project warnings, you can add your PC’s root directory to the trusted locations. However, we do not recommend doing this, as it could potentially leave you open to an attack.

Note that building or running a Maven or Gradle project from the command line carries the same security risks as importing it into an IDE. So if you choose to open the project in the safe mode, you also need to avoid running Maven or Gradle commands in the terminal.

注意，从命令行构建或运行Maven或Gradle项目与将其导入IDE中存在相同的安全风险。因此，如果您选择以安全模式打开项目，您还需要避免在终端中运行Maven或Gradle命令。

For more information, please refer to the [documentation page](https://www.jetbrains.com/help/idea/2020.3/project-security.html) on project security.

### Bug-fixes

IntelliJ IDEA 2020.3.3 also brings significant fixes:

*   Fixed the crashes happening on IntelliJ IDEA startup. \[[JBR-3066](https://youtrack.jetbrains.com/issue/JBR-3066)\]
*   Fixed the issue causing unnecessary backslashes to be added in Markdown files containing code blocks. \[[IDEA-258796](https://youtrack.jetbrains.com/issue/IDEA-258796)\]
*   Fixed the IntelliJ IDEA crashes occurring when the CUBA plugin tried to set a zoom level for the CEF browser. \[[JBR-2947](https://youtrack.jetbrains.com/issue/JBR-2947)\]
*   Keychain is now available on Apple Silicon. \[[IDEA-258912](https://youtrack.jetbrains.com/issue/IDEA-258912)\]
*   Fixed the run configuration errors when using Cucumber tests with Java. \[[IDEA-256627](https://youtrack.jetbrains.com/issue/IDEA-256627)\]
*   Fixed issues with the _Close All But Pinned_ and _Close All_ actions. \[[IDEA-256044](https://youtrack.jetbrains.com/issue/IDEA-256044)\]
*   Fixed logs’ spamming when disconnecting from Docker. \[[IDEA-259400](https://youtrack.jetbrains.com/issue/IDEA-259400)\]
*   Fixed the wrong behavior of the Diff view. \[[IDEA-257651](https://youtrack.jetbrains.com/issue/IDEA-257651)\]
*   Fixed a focus issue in the branch list. \[[IDEA-254354](https://youtrack.jetbrains.com/issue/IDEA-254354)\]

That’s all for today! Check out the full list of addressed issues in the [release notes](https://confluence.jetbrains.com/display/IDEADEV/IntelliJ+IDEA+2020.3.3+(203.7717.56+build)+Release+Notes). If you have any suggestions for improving IntelliJ IDEA, do not hesitate to post them to our [issue tracker](https://youtrack.jetbrains.com/issues/IDEA) or comment on this post.

Happy developing!

https://blog.jetbrains.com/idea/2021/03/intellij-idea-2020-3-3/

