# Visual Studio Code – Tips & Commands (Single-Block Cheat Sheet)

ASSUMPTIONS
- OS: Linux (Ubuntu)
- VS Code: latest stable
- Default keybindings
- Terminal available

OPEN VS CODE
- code .
- code <folder>
- code <file>

If `code` command is missing:
Ctrl+Shift+P → Shell Command: Install 'code' command in PATH

CORE LAYOUT
- Explorer (files): Ctrl+B
- Editor: code tabs
- Terminal: Ctrl+`
- Command Palette (everything): Ctrl+Shift+P
- Status Bar: language, git, errors

ESSENTIAL SHORTCUTS
- Command Palette: Ctrl+Shift+P
- Quick Open File: Ctrl+P
- Toggle Terminal: Ctrl+`
- Toggle Sidebar: Ctrl+B
- Search in Files: Ctrl+Shift+F
- Replace in Files: Ctrl+Shift+H
- Comment Line: Ctrl+/
- Format File: Shift+Alt+F
- Go to Definition: F12
- Rename Symbol: F2
- Multi-cursor (same word): Ctrl+D
- Move Line: Alt+↑ / Alt+↓

EDITOR TIPS
- One project = one folder
- Prefer Ctrl+P over file tree
- Use multi-cursor aggressively
- Split editor: Ctrl+\

TERMINAL USAGE
- Opens in project root
- Same shell as system
- Common commands:
  npm run dev
  python main.py
  flutter run
  docker compose up
- New terminal: Ctrl+Shift+`

GIT (BUILT-IN)
- Initialize repo: git init
- Workflow: stage → commit → push
- Common commands:
  git status
  git add .
  git commit -m "message"
  git push

EXTENSIONS MANAGEMENT
- List extensions:
  code --list-extensions
  code --list-extensions --show-versions
- Install extension:
  code --install-extension publisher.extension
- Uninstall extension:
  code --uninstall-extension publisher.extension
- Export extensions:
  code --list-extensions > extensions.txt
- Reinstall on another machine:
  cat extensions.txt | xargs -n 1 code --install-extension

FORMATTING
- Enable format on save (settings.json):
  "editor.formatOnSave": true
- Manual format: Shift+Alt+F

DEBUGGING (BASIC)
- Click gutter to add breakpoint
- Run → Start Debugging
- Inspect variables, call stack, watches

SEARCH & REFACTOR
- Symbol search: Ctrl+T
- File symbol: Ctrl+Shift+O
- Safe rename: F2

JSON / CONFIG FILES
- IntelliSense enabled by default
- Use formatter often
- Errors shown in Problems tab

PERFORMANCE TIPS
- Disable unused extensions
- Do not open home directory
- Reload if editor misbehaves:
  Ctrl+Shift+P → Reload Window

COMMON FIXES
- Terminal not opening → Reload Window
- IntelliSense broken → check language mode, reload window
- Git not detected → ensure git init is run

PRO TIPS
- Learn Command Palette first
- Keep extensions minimal
- Use workspace settings per project
- Commit small and often
- VS Code is an editor, not a file manager

VERIFICATION CHECKLIST
- Command Palette opens
- Terminal opens in project root
- Formatter runs on save
- Git panel shows changes
- Extensions load correctly

END
This is sufficient for daily professional VS Code usage.
