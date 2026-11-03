# SetupMCP Excel.cmd

Windows setup for Excel Live MCP (desktop Excel 2016+; Codex, Claude, Google Antigravity).
This fork exists to publish the installer; the MCP server itself is installed from the official
repository `kousunh/excel-mcp-server`.

Run it as is: it requests administrator rights, and at every start it compares its own
`$script:InstallerVersion` with this file on `main` and, when a newer valid version is published,
replaces itself and restarts. To publish a change, edit this file, raise the version in the three
places (`title`, `echo` and `$script:InstallerVersion`), check that the PowerShell part parses, and
push to `main`.
