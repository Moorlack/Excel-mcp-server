# SetupMCP Excel.cmd

Windows setup for Excel Live MCP (desktop Excel 2016+; Codex, Claude, Google Antigravity).
The installer and the MCP server both come from this fork. Upstream releases of
`kousunh/excel-mcp-server` reach users only after they are merged into `main` here, so a broken
upstream update can be held back.

Run it as is: it requests administrator rights, and at every start it compares its own
`$script:InstallerVersion` with this file on `main` and, when a newer valid version is published,
replaces itself and restarts. To publish a change, edit this file, raise the version in the three
places (`title`, `echo` and `$script:InstallerVersion`), check that the PowerShell part parses, and
push to `main`.
