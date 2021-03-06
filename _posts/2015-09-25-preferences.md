---
layout: page
title: "Preferences"
category: doc
date: 2015-09-25 23:17:25
order: 2
---

BleachBit provides preferences (also called options or settings) which change how it works. To edit the preferences, click **Edit** - **Preferences**.

### Check periodically for updates via the Internet

When enabled, BleachBit checks for updates. If an update is found, a notification button appears. Click the button to read about the changes and download the new version. The new version is _not_ downloaded automatically.

### Hide irrelevant cleaners

Enabling this option reduces clutter at the cost of a slightly longer startup.

BleachBit determines whether a cleaner is relevant two ways: first, it checks whether there is anything to clean. For example, it only checks that Firefox has cache, but it doesn't check whether Firefox is installed. (This works well for applications you used once and then deleted.) Second, BleachBit checks whether the cleaner was already enabled: enabled cleaners are not hidden.

If a cleaner has a deep scan option, it is not hidden.

### Overwrite contents of files to prevent recovery

When files are deleted normally, the operating system only deletes the _reference_ to the file (not the _contents_), but later file can usually be undeleted. To securely delete files marked for cleaning (such as Firefox cache) to prevent this kind of recovery, enable overwriting files (also called file shredding).

Overwriting files is significantly slower than deleting files normally. Overwriting is supported for standard file deletions (such as deleting Firefox cache) and when deleting Firefox URL history (a special operation), but it is not supported for other special operations (such as deleting locked files in Windows). Overwriting is not effective with some situations such as the Linux ext3 and ext4 filesystems in `data=journal` mode. On Ubuntu the default is `data=ordered` mode which is effective to overwrite.

Since BleachBit 2.0 when running with administrator privileges, wiping compressed files on NTFS is effective.

To complement the limitations of overwriting individual files, use the **Free disk space** option under **System** to overwrite free disk space and hide previously deleted files.

### Exit after cleaning

When this option is enabled and when the cleaning is done, the application will close itself.

### Confirm before delete

When this option is enabled, the cleaning button requires a confirmation prompt before making changes.

### Use IEC sizes

This option affects only how sizes are reported, and it does not affect how the application functions. When enabled, one KiB is 1000 bytes. When disabled, 1 kB is 1000 bytes.

### Dark mode

When enabled, the application uses a dark theme. When disabled, the application uses a light theme. For a demonstration, see the video: [BleachBit version 2.3 dark mode](https://www.youtube.com/watch?v=kWM4-7X5_1g).

### Show debug messages

When enabled, both the GUI and the console will show technical messages that sometimes help trouleshooting. Most users do not need to enable this option.

### Custom

In the custom tab, choose a file or folder to delete. It will be deleted only when the Custom option is enabled under the System category.

### Drives

Before using the **Free disk space** option under **System**, select a writable directory for each drive (also called logical partition or mount point). The unallocated disk space in the chosen drives will be wiped.

When starting for the first time, BleachBit tries to guess the correct value. In Linux, a good setting is typically <tt>/home/(username)</tt> and <tt>/tmp</tt>, but only one should be used if both are on the same partition. In Windows, typically <tt>C:\\</tt> is a good choice.

### Languages

Select all languages you wish to keep. If your native language is Klingon, select Klingon. Locale files for unchecked languages will be deleted when cleaning **Localizations** under **System**.

This option is not available in Windows.

### Whitelist

Files and folders added to the whitelist will be skipped during preview and during cleaning.
