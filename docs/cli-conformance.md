# Zowe CLI Conformance Checklist

A plug-in must follow meet the following requirements to align with the Zowe Conformance Program:

- The plug-in is constructed on [Imperative CLI Framework](https://github.com/zowe/imperative).
- The `@lts-incremental` version of your plug-in is installable into the `@lts-incremental` version of the core Zowe CLI, at minimum (cannot run as a standalone CLI). For more information about the semantic versioning that CLI uses, see [Maintainer Versioning](https://github.com/zowe/zowe-cli/blob/master/docs/MaintainerVersioning.md).
- Users of the plug-in can store mainframe connection information in user profiles.
- Users can override profiles using options on the command line and/or environment variables.
- The plug-in generally adheres to the CLI [Package and Plug-in Guidelines](https://github.com/zowe/zowe-cli/blob/master/docs/PackagesAndPluginGuidelines.md).
- The tests for your plug-in generally adhere to the guidelines listed in [Testing Guidelines](https://github.com/zowe/zowe-cli/blob/master/docs/TESTING.md) and [Plugin Testing Guidelines](https://github.com/zowe/zowe-cli/blob/master/docs/PluginTESTINGGuidelines.md). 
- The plug-in command/help syntax adheres to the [Command Format Standards](https://github.com/zowe/zowe-cli/blob/master/docs/CommandFormatStandards.md).
- Provide external (user guide, readme) documentation for the plug-in. For guidance, see [Documentation Guidelines](https://github.com/zowe/zowe-cli/blob/master/CONTRIBUTING.md#documentation-guidelines).
- Brand the plug-in (in documentation, for example) to be consistent with other CLI plug-ins. For example, "Zowe CLI Plug-in for Abc". 
- All commands in the plug-in should only write to `stdout` or `stderr` via Imperative Framework's `response.console` APIs. This ensures that your commands function with the `--response-format-json` flag. 

**Note:** You can also reference the [Zowe CLI Contribution Guidelines](https://github.com/zowe/zowe-cli/blob/conformance/CONTRIBUTING.md) to help you develop a plug-in efficiently. 

If you are new to the project, start creating your plug-in by cloning our sample plug-in. See [Zowe CLI Development Tutorials](https://zowe.github.io/docs-site/latest/extend/extend-cli/cli-devTutorials.html#getting-started) to learn more. 