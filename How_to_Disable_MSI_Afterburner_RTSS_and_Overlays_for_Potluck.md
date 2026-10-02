# How to Disable MSI Afterburner, RTSS, NVIDIA App Overlay, and Discord Overlay

Potluck is a large Stardew Valley modlist, and programs that hook into
the game's rendering can sometimes interfere with smooth frame pacing.
During Potluck testing, MSI Afterburner / RivaTuner Statistics Server
(RTSS) were associated with a repeatable issue where the game would
initially run smoothly, then develop persistent FPS stuttering after
roughly 25--35 minutes of play.

## Symptoms

If one of these programs or overlays is interfering with Stardew Valley,
you may notice:

-   The game initially runs smoothly.
-   After playing for a while, FPS or frame pacing suddenly becomes
    noticeably stuttery.
-   The stuttering may begin anywhere and does not necessarily
    correspond to a particular map, activity, or event.
-   Changing locations or sleeping until the next day may not fix it.
-   Restarting Stardew Valley may temporarily restore smooth
    performance.

If you experience this behavior, make sure the programs and overlays
below are disabled before troubleshooting Potluck itself.

------------------------------------------------------------------------

## 1. Disable MSI Afterburner

1.  Open **MSI Afterburner**.
2.  Click the **Settings** gear.
3.  Under **General**, disable **Start with Windows**.
4.  Disable **Start minimized** if enabled.
5.  Click **Apply**, then **OK**.
6.  Find MSI Afterburner in the Windows system tray.
7.  Right-click it and choose **Exit**.

> Simply closing the MSI Afterburner window may minimize it to the
> system tray instead of actually closing it.

### Disable it in Windows Startup Apps

1.  Press **Ctrl + Shift + Esc** to open **Task Manager**.
2.  Select **Startup apps**.
3.  Find **MSI Afterburner**.
4.  Right-click it and select **Disable**.

------------------------------------------------------------------------

## 2. Disable RivaTuner Statistics Server (RTSS)

RTSS is commonly installed alongside MSI Afterburner and can continue
running independently.

1.  Open **RivaTuner Statistics Server**.
2.  Turn **Start with Windows** **OFF**.
3.  Find RTSS in the Windows system tray.
4.  Right-click it and choose **Exit**.

### Disable it in Windows Startup Apps

1.  Press **Ctrl + Shift + Esc** to open **Task Manager**.
2.  Select **Startup apps**.
3.  Find **RivaTuner Statistics Server** or **RTSS**.
4.  Right-click it and select **Disable**.

### Confirm MSI Afterburner and RTSS are actually closed

For the cleanest test, **restart Windows** after changing the startup
settings. After restarting, do not manually launch MSI Afterburner or
RTSS.

Open **PowerShell** and run:

``` powershell
Get-Process | Where-Object {
    $_.ProcessName -match 'Afterburner|RTSS'
}
```

If both are fully closed, the command should return **no matching
processes**.

For an additional check:

``` powershell
Get-CimInstance Win32_Process |
Where-Object {
    $_.Name -match 'Afterburner|RTSS'
} |
Select-Object Name, ProcessId, ExecutablePath
```

Again, you want **no results**.

------------------------------------------------------------------------

## 3. Disable the NVIDIA App Overlay

You do **not** need to uninstall the NVIDIA App or your NVIDIA graphics
driver. Only disable its overlay.

1.  Open the **NVIDIA App**.
2.  Open **Settings**.
3.  Find **NVIDIA Overlay** / **In-Game Overlay**.
4.  Turn the overlay **OFF**.

Launch Stardew Valley normally through Potluck/MO2 afterward.

------------------------------------------------------------------------

## 4. Disable the Discord Game Overlay

You can continue running Discord normally. Only its game overlay needs
to be disabled.

1.  Open **Discord**.
2.  Click the **User Settings** gear near your username.
3.  Find **Game Overlay** under the activity/game settings.
4.  Turn **Enable in-game overlay** **OFF**.

If you use the Discord overlay for other games, you can instead disable
it specifically for Stardew Valley through Discord's
registered-games/overlay settings.

------------------------------------------------------------------------

## Recommended Potluck Setup

For the cleanest and most predictable Potluck experience:

-   **MSI Afterburner:** Closed
-   **RivaTuner Statistics Server (RTSS):** Closed
-   **NVIDIA App Overlay:** Disabled
-   **Discord Game Overlay:** Disabled

Other recording, monitoring, FPS-limiting, or overlay software can also
hook into a game's rendering. If Potluck develops unexplained persistent
stuttering, temporarily close those programs as part of troubleshooting.

## Still Stuttering?

If the problem continues, restart Windows, confirm MSI Afterburner and
RTSS are not running, then launch Potluck again and test from a fresh
game session.

When requesting Potluck support, mention that you have already tested
with **MSI Afterburner, RTSS, NVIDIA Overlay, and Discord Overlay
disabled**.
