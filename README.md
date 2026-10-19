# Y86 Syntax Highlighter

Syntax highlighting for Y86-64 and Y86-32 assembly (`.ys` and `.s` files) from CS:APP.

Highlights instructions (including `iaddq`), registers, labels, directives
(`.pos`, `.align`, `.quad`, ...), immediates, and `#` / `/* */` comments.

## Try it
Open this folder in VS Code and press F5 to launch an Extension Development Host.

## Install
`npx @vscode/vsce package` then `code --install-extension y86-highlighter-0.1.0.vsix`
