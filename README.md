# Y86 Syntax Highlighter

Syntax highlighting for Y86 assembly (`.ys` and `.s` files) from CS:APP.
Supports Y86-64, with Y86-32 (`l`-suffixed) instructions also recognized.

Highlights instructions, registers, labels, directives
(`.pos`, `.align`, `.quad`, ...), immediates, and `#` / `/* */` comments.

## Install
1. Download `y86-highlighter-0.1.0.vsix`.
2. In VS Code, open the Extensions tab, click the `⋯` menu, and choose
   Install from VSIX…
3. Select the downloaded file, then reload the window.

<img width="581" height="306" alt="Install from VSIX" src="https://github.com/user-attachments/assets/58056943-fa1a-49c9-a8bf-6279532514c7" />

Or from the terminal:
```
code --install-extension y86-highlighter-0.1.0.vsix
```

If `.s` files open as a different assembly language, add this to your
settings:
```json
"files.associations": { "*.s": "y86" }
```

## Preview
GitHub Dark theme

<img width="266" height="343" alt="GitHub Dark" src="https://github.com/user-attachments/assets/bc4b0ec2-22fe-4aee-b321-e284237627b5" />

Default VS Code Dark theme

<img width="313" height="470" alt="Default Dark" src="https://github.com/user-attachments/assets/52a90568-71d7-4c66-8df4-59b0e860b54a" />

## Development
After changing the grammar in `syntaxes/y86.tmLanguage.json`, rebuild and
reinstall:
```
cd path/to/y86-highlighter
npx @vscode/vsce package --allow-missing-repository --skip-license
code --install-extension y86-highlighter-0.1.0.vsix --force
```
Then run Developer: Reload Window. To iterate faster, open the folder in
VS Code and press F5 to launch a test window with the extension loaded.
