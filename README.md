# Zeus

Zeus is a desktop coding agent and personal assistant that runs entirely on **local models**, on
your own computer. Nothing you type is sent to an AI service. It keeps working until the task is
done.

This repository has the installers and update files. Download the latest version from
**[Releases](https://github.com/buggs119/Zeus-Release/releases)**.

## Install

**Windows 10 / 11 (64-bit):** download `Zeus_X.Y.Z_x64-setup.exe` and run it. During setup Zeus
looks at your graphics card, memory and disk, recommends models that fit, and downloads the model
and its runtime for you. You can switch between CUDA (NVIDIA), Vulkan and CPU in Settings → Models.

**macOS (Apple Silicon):** download `Zeus_X.Y.Z_aarch64.dmg` and drag Zeus to Applications. On a
Mac, Zeus runs its models through [oMLX](https://github.com/jundot/omlx), so install and start oMLX
first. The app isn't notarized by Apple yet: the first time, right-click Zeus → Open, or run
`xattr -dr com.apple.quarantine /Applications/Zeus.app` in Terminal.

Zeus updates itself: it checks for a new version when it starts, and under Settings → Updates.

## What it does

- **Agent:** works on code in your projects. Reads and edits files, runs commands and tests, uses
  git, and keeps going until the job is finished, with checkpoints you can undo.
- **Assistant:** research, writing, planning, email and notes, plus scheduled tasks that run on
  their own.
- **On-screen assistant:** a small helper on your desktop that you can talk to and share your
  screen with.
- **Learns as you use it:** remembers your preferences and projects, learns from its own mistakes
  and from your 👍 / 👎, and gets better over time.
- **Code graphs:** maps how your code fits together, built locally.

## Files in this repository

- `latest.json`: tells installed copies of Zeus which version is newest (read by the in-app updater).
- `catalog/models.json`: the list of recommended models Zeus shows during setup. It's updated here
  so recommendations can change without a new release.
