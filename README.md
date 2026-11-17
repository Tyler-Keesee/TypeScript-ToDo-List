# TaskFlow Pro - The 2025 Edition

## Windows 11: run the actual app (PowerShell)

This repo includes a browser-ready `index.html` and `main.js`. The most reliable **basic launch** does **not** require npm or compiling TypeScript. Install Git and Python 3, then run **each command separately**:

```powershell
git clone https://github.com/Tyler-Keesee/TypeScript-ToDo-List.git
```

```powershell
Set-Location .\TypeScript-ToDo-List
```

```powershell
python -m http.server 8000
```

Open **http://localhost:8000/** in Edge while the command runs; Ctrl+C stops the server.

**Run the actual shipped app:** index.html currently references the compiled `main.js` in the repository root. You can serve it without npm. The TypeScript/Vite build has passed clean-clone CI on Node.js 22 for Windows and Linux. The browser-ready `main.js` is still the direct launch option; build checks do not prove all browser interactions. No Python packages or `venv` are required.

If you specifically want to work on the TypeScript/Vite pipeline, install Node.js 22 and run:

```powershell
node --version
```

```powershell
npm --version
```

```powershell
npm ci
```

```powershell
npm run dev
```

Open the URL printed by Vite and check the browser console. **Build verification:** `npm ci` and `npm run build` passed on clean Windows and Linux CI runners using Node.js 22. To reproduce, run `npm run build` separately after `npm ci`. UI behavior and PWA installation still require browser testing.

---


A cutting-edge task management application built with modern web technologies.

## Features

- 🚀 Modern TypeScript implementation
- 🔄 Real-time task state updates
- 🌙 Auto-switching dark mode support
- 📱 Responsive design for all devices
- ⭐ Mark tasks as important
- 🏷️ Add tags to tasks
- 🔍 Filter tasks by status
- 📅 Due date tracking
- 📊 Task statistics dashboard
- 🔢 Multiple priority levels
- 🧹 Clear completed tasks

## Technical Details

- Uses ES2017+ JavaScript features
- Local storage persistence
- Web-standard Custom Elements
- CSS Grid and Flexbox for layout
- CSS Variables for theming
- Responsive design with media queries

## Usage

1. Add a task with text, priority, due date, and optional tags
2. Mark tasks as complete by clicking the checkbox
3. Star important tasks with the star button
4. Filter tasks using the dropdown
5. Remove completed tasks with the "Clear Completed" button

## Future Enhancements

- Offline support with Service Workers
- Cloud synchronization
- Task categories and projects
- Recurring tasks
- Time tracking
- Drag and drop reordering