# Serenade GIF

Turn a video or an animated GIF into a sprite-sheet texture and the
`llSetTextureAnim` script that plays it, for use in the Second Life®
virtual world.

**[Download the latest version](https://github.com/LunarSerenade/serenade-gif/releases/latest)**

Windows 10 / 11, 64-bit. No installer. Each release carries the program
two ways, and they are the same program:

- **`Serenade.GIF.exe`** on its own. Download it and run it. On launch it
  writes a folder named `Serenade GIF licences` beside itself, holding the
  notices and licence texts listed below. If the folder it is sitting in
  cannot be written to, it uses `%LOCALAPPDATA%\Serenade\serenade-gif\licences` instead, and the
  **Licences** button in the toolbar shows the same documents either way.
- **`Serenade.GIF.rar`**, the same `.exe` with `NOTICE.txt`,
  `EULA.txt`, a short `Guide.txt` and the `licenses` folder already
  unpacked next to it. Take this one if you have the author's permission
  to pass the program on, because those files have to travel with it.
  Passing on the program itself needs that permission (see REDISTRIBUTION
  in the EULA); the open-source components inside it carry their own,
  broader rights that no permission of the author's can limit.

---

## Updates

The app checks this repository for a newer release a few seconds after it
starts. When one exists a strip appears at the top of the window; from
there you can read the release notes and let it install and restart
itself, or skip the version. You can also ask at any time with the
**Check for Updates** button in the toolbar.

No personal data, no account, and nothing about the files you process is
sent when it checks. It is an anonymous read of two public files in this
repository, the release list and `status.json`, and GitHub sees only what
any browser fetching a public page would send.

An in-app update replaces the program file only. If your copy came as the
`.rar`, the `NOTICE.txt`, `EULA.txt` and `licenses` folder beside it are
left as they were and may fall behind. The copies in the `Serenade GIF
licences` folder are rewritten every launch and are the ones that match
what you are actually running.

## What this repository holds

Serenade GIF is not open source; the source is not published here. This
repository is the distribution point:

- **Releases**, holding the `.exe` and the `.rar` for each version, plus
  the FFmpeg source tarball described under Open-source components.
- **`status.json`**, a small file the app reads on launch so we can post a
  notice, or withdraw a build, without shipping a new one.

Bug reports and feature requests are welcome in
[Issues](https://github.com/LunarSerenade/serenade-gif/issues).

## Open-source components

Serenade GIF's own code is closed, but the program is built on open-source
software and ships a good deal of it inside the executable: Python, Pillow,
OpenCV, NumPy, Tcl/Tk, FFmpeg and others. Every one of them is named,
attributed and licensed in `NOTICE.txt`, with the full licence text of each
in the `licenses` folder. Both travel with the download, and the program
itself has a **Licences** button in the toolbar that shows all of them
without leaving the app.

Two of those components, the bundled `ffmpeg.exe` and the FFmpeg libraries
inside OpenCV's video decoder, are covered by the GNU Lesser General Public
License version 2.1. That licence carries obligations this repository has to
meet, so to be explicit about them:

- **Source.** The FFmpeg source for the bundled `ffmpeg.exe` is the
  unmodified official FFmpeg 7.1.5 release, attached to each release here
  as `ffmpeg-7.1.5.tar.xz` (with its upstream signature `.asc`), so the
  source sits in the same place as the binary. Nothing in it is patched.
  It is a static build, so zlib 1.3.1 and the mingw-w64 and GCC runtimes
  are compiled into it as well, and those are not part of that tarball.
  `NOTICE.txt` names them and carries a written offer, good for three
  years, covering the source of everything in both FFmpeg components.
  Requests go through Issues.
- **Modification and reverse engineering.** The EULA permits you to modify
  your own copy for your own use and to reverse engineer it as far as
  needed to debug those modifications, and permits extracting any bundled
  third-party component out of the executable and redistributing it under
  its own licence. Those permissions are not the author's to withdraw.
- **Replacing the library.** Set `OPENCV_FFMPEG_DLL_DIR` to a folder
  holding your own interface-compatible build of
  `opencv_videoio_ffmpeg4130_64.dll` and OpenCV loads yours instead. Set
  `SERENADE_FFMPEG` to your own `ffmpeg.exe` and the app uses that in place
  of the bundled one.

## Legal

Second Life® and Linden Lab® are trademarks of Linden Research, Inc.
Serenade and Serenade GIF are not affiliated with or sponsored by
Linden Research.

Use of the software is governed by the EULA included with the download.
