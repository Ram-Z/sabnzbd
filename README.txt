Release Notes - SABnzbd 4.0.0 Release Candidate 2
=========================================================

## Changes since 3.7.2
- In this major update we replaced a core part of Python's SSL handling
  with our own improved version. This results in large performance increases
  when downloading from news servers with SSL enabled.
  In addition, the general connection handling was overhauled, resulting in
  performance improvements for all news servers.
  Special thanks to: mnightingale, puzzledsab and animetosho!
- There are multiple settings that can tweak performance, see:
  https://github.com/sabnzbd/sabnzbd/discussions/2474
  We are trying to find the most optimal default settings, so you
  can help us by letting us know the results on your system!
- When adding a new news server, SSL is enabled by default.
- File assembly performance significantly improved by relying on the
  CRC32 instead of the MD5 to perform QuickCheck of files.
- Slowdown more gracefully when the cache fills up.
- Replaced separate Series/Movie/Date Sorting with general Sorter.
- HTTPS files are included in the `Backup`.
- Improved `Watched Folder` scanning and processing.
- Ignore resource fork files created by macOS.
- `Deobfuscate final filenames` is enabled for new installations.
- Dropped support for Python 3.7.

## Bugfixes since 3.7.2
- Restore applying `History Retention` setting at startup.
- Windows: Not all invalid characters were removed from filenames.
- Windows: Firewall rules were not removed by uninstaller.

## Upgrade notices
- The download statistics file `totals10.sab` is updated in 3.2.x
  version. If you downgrade to 3.1.x or lower, detailed download
  statistics will be lost.

## Known problems and solutions
- Read the file "ISSUES.txt"

## About
  SABnzbd is an open-source cross-platform binary newsreader.
  It simplifies the process of downloading from Usenet dramatically, thanks
  to its web-based user interface and advanced built-in post-processing options
  that automatically verify, repair, extract and clean up posts downloaded
  from Usenet.

  (c) Copyright 2007-2023 by "The SABnzbd-team" \<team@sabnzbd.org\>
