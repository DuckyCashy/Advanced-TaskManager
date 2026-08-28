# Advanced Task Manager

A Windows 10/11 WPF monitoring application inspired by the Windows Task Manager layout, with extra benchmarking and hardware-observation features.

## Current build
- Task Manager-style dark navigation and content layout
- Processes, Performance, App history, Startup apps, Users, Details, Services, Settings
- Live CPU, RAM, GPU, disk and network graphs
- 60-second graph history with min/max readout and filled live trace
- GPU Engine performance-counter monitoring when the Windows counter is available
- Benchmark CSV export includes GPU usage
- System tray support
- Safe close / accidental End Task guard: closing the window minimizes it to the tray
- Simple Mode from Settings
- Configurable monitoring interval

## Important limitation
The safe-close guard is intentionally not advertised as security or true process protection. Windows can still terminate the application through Task Manager, `taskkill`, services, or an administrator/debugger. It only protects against normal/accidental window closure.

## Build
Requires Visual Studio 2022 or the .NET 8 SDK on Windows.

Open `src/AdvancedTaskManager/AdvancedTaskManager.csproj` and build for Windows x64.

NuGet packages:
- WPF-UI 4.3.0
- System.ServiceProcess.ServiceController 8.0.0
- System.Diagnostics.PerformanceCounter 8.0.0
