# macOS Dark Mode Sync IDEA Plugin

[![Build Status](https://travis-ci.com/gilday/dark-mode-sync-plugin.svg?branch=master)](https://travis-ci.com/gilday/dark-mode-sync-plugin)

Plugin for synchronizing IDEA's theme with macOS's Dark Mode. When macOS is in
dark mode, plugin sets IDEA to Darcula, but when macOS is in light mode, sets
IDEA theme to IntelliJ

## Building

    ./gradlew build

## Testing

    ./gradlew runIde

## How Does It Work?

The plugin polls the macOS Dark Mode configuration by executing the following
command and interpreting its output.

    defaults read -g AppleInterfaceStyle

When the plugin detects that macOS is using Dark Mode, it sets the IDEA theme to
"Darcula". When the plugin detects that macOS is not using Dark Mode, it sets
the IDEA theme to "IntelliJ".
