# Vitest extension for Visual Studio Code</b>

<span style="font-size:larger;">Available on the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=milan-kovacic.vitest-lab).</span>

<br />

![](https://i.ibb.co/bJCbCf2/202203292020.gif)

# Features

- Run/debug vitest tests in vscode
- Watch mode is supported 🎊. Test reruns are blazing fast

![Watch Mode](https://i.ibb.co/YRhJj9f/Screen-Recording-2022-05-21-at-20-09-20.gif)

# Requirements

- Visual Studio Code >= November (version 1.85.0).
- Vitest >= 1.0.0

# Configuration

- `vitest.include` and `vitest.exclude`` are deprecated. The extension now loads the include and exclude paths from your vitest config file.
- `vitest.enable`: This plugin will try to detect whether the current project is
  set up with Vitest to activate itself. If detection fails, you can enable the plugin manually.
- `vitest.nodeEnv`: The env passed to runner process in addition to
  `process.env`
- `vitest.commandLine`: The command line to start vitest tests. **It should have with the ability
  to append extra arguments**. For example
  `npx vitest` or `yarn test --`.(This is a workspace setting. Do not change it in
  the user setting directly, which will affect all the projects you open)
- `vitest.debugExclude`: Automatically skip files covered by these glob patterns. Default:
  `[\"<node_internals>/**\", \"**/node_modules/**\"]`

# Frequently Asked Questions

#### **How can I use it in monorepo?**

See <https://vitest.dev/guide/workspace.html> for monorepo support.

#### **How can I use this extension when tests are under a sub directory?**

You can use VS Code command `add folder to workspace` to add the sub directory. The extension should work fine.

#### **`test.each` is not working**

Dynamic test name is not supported yet. This extension currently relies on the babel parser to calculate the positions of tests statically.
