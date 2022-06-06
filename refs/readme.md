## Linux kernel commits ##

* 6d36ce2 tools lib traceevent: Add UL suffix to MISSING_EVENTS
* 952a99c tools lib traceevent: Fix bad force_token escape sequence
* 99c621d tracing: Add saved_tgids file to show cached pid to tgid mappings
* 4da14d5 staging: greybus: firmware: Convert sscanf calls to strtoul
* afb5fdf staging: greybus: firmware: Change long long unsigned to unsigned long long
* 5099c4c staging: greybus: firmware: Remove extra braces from single line if
* 0c38018 staging: greybus: firmware: Remove trailing semicolon from FW_TIMEOUT_DEFAULT

## Dr. Dobbs optimizing Pixomatic articles (by Michael Abrash) ##

* [Optimizing Pixomatic for x86 Processors: Part I](http://www.drdobbs.com/architecture-and-design/optimizing-pixomatic-for-x86-processors/184405765)
* [Optimizing Pixomatic For Modern x86 Processors: Part II](http://www.drdobbs.com/optimizing-pixomatic-for-modern-x86-proc/184405807)
* [Optimizing Pixomatic for Modern x86 Processors: Part III](http://www.drdobbs.com/optimizing-pixomatic-for-modern-x86-proc/184405848)

## Simple DirectMedia Layer (SDL2) patches ##

* [https://hg.libsdl.org/SDL/log](https://github.com/libsdl-org/SDL)
* 2018-04-23 Added support for adjusting thread priorities using Linux RealtimeKit.
* 2013-02-14 Clear relative mouse mode and restore when bringing up sdl message box.
* 2013-02-05 Add defines to disable setlocale and fork. Disable that code by default for now.
* 2013-02-05 Use left facing arrow instead of right facing arrow for system cursor.
* 2012-11-19 Add SDL_CreateSystemCursor for Windows and Linux.
* 2012-10-11 Add GLX_X_VISUAL_TYPE_EXT so created window will use DirectColor if available (instead of TrueColor).
* 2012-10-11 Add XInitThreads to X11_CreateDevice.
* 2012-10-11 Fix Colormap when using X11_SetWindowFullscreenViaWM() path.

## Random articles about projects I’ve contributed to ##

* [Valve Picks Up Another All-Star Linux Developer](http://www.phoronix.com/scan.php?page=article&item=valve_linux_sdl&num=1)
* [Valve hires world-class development trio](http://www.develop-online.net/news/valve-hires-world-class-development-trio/0109284)
* [Valve joins Linux Foundation](http://www.pcgamer.com/valve-joins-linux-foundation/)
* [The making of the Xbox: How Microsoft unleashed a video game revolution ](https://venturebeat.com/2011/11/14/making-of-the-xbox-1/view-all/)
* [A First Look at the Larrabee New Instructions](http://www.drdobbs.com/parallel/a-first-look-at-the-larrabee-new-instruc/216402188)
* [Rasterization on Larrabee](http://www.drdobbs.com/parallel/rasterization-on-larrabee/217200602)

## LLDB Debugger Commits ##

* Merge RegisterContextPOSIX_x86_64 and RegisterContextPOSIX_i386 into RegisterContextPOSIX_x86
* Re-enable test_convenience_registers_16bit_with_process_attach test for Linux.
* Clean up RegisterContextPOSIX i386 code. Use 32-bit register enums without gaps on 64-bit hosts. Don't show 64-bit registers when debugging 32-bi
* Remove unused local variable.
* fix class/struct mismatch warning
* Warning cleanup.
* Clean up RegisterContextPOSIX. Renamed to POSIXBreakpointProtocol. Will clean up header files and m_register_infos shortly.
* Cleanup POSIX RegisterContext class hierarchies.
* warning cleanup (use LLDB_INVALID_HOST_THREAD instead of NULL)
* unused variable, typedef requires name warning cleanup
* Round plt entsize to addralign
* add register name to UnwindLog error message
* A clang::Type::Decayed type to kill compile warning
* add error checking and messages to 'target modules show-unwind' command
* clean up about 22 warnings messages
* Initialize m_leak member variable.
* Fix Linux Host::GetCurrentThreadID() to return real tid (not pthread_t). This fixes threadname logging (--thread-name) Add "-t" to TestLogging.py
* Fix thread name updating in Linux. "thread list" should report correct names always now. Created new LinuxThread class inherited from POSIXThread
* Optimize Host::GetThreadName() to read from /proc/$TID per Matt's suggestion.
* Add format specifiers to various format ids so we can print thread ids in decimal on Linux and FreeBSD.
* simple plugin now works with Linux fix assert in SetPluginInfo implement Linux ePathTypeLLDBSystemPlugins and ePathTypeLLDBUserPlugins implement 
* Fix Rendezvous breakpoint to only be set once, resolve addr in BreakpointLocationList::FindByAddress
* Fix "source list -n printf" on Linux (printf is symbol alias for __printf)
* Add silent option to command source. Patch from Matthew Sorrels
* Use target DisplaySource if available so we can get mixed source and assembly.
* Symbol prologue code checks if funciton lines up with symbol and uses function prologue code with line info if so.
* Fix ObjectFileELF crc32 code used when no build id is present.
* Add split symbol support to test makefile & add linux split symbol test case.
* Split symbol support for ELF and Linux.
* Add new files to CMakeLists.txt to fix cmake build error.
* Add newer Linux AT_ defines from elf.h.
* Remove extra modules.Append() as it causes dupes in the m_images array. (Used with image list, etc.)
* Fix unitialized variable in AuxVector::GetEntryName() which crashed in AuxVector::DumpToLog
* ObjectFileELF::GetModuleSpecifications on Linux should work now. Which means "platform process list" should work and list the architecture.
* Add ${ansi.XX} parsing to lldb prompt, use-color setting, and -no-use-colors command line options.
* Comment out ObjectFileELF::GetModuleSpecifications() function until I can debug where it's causing tests to fail.
*  Implement ObjectFileELF::GetModuleSpecifications(), and add PlatformLinux code to deal with unknown arch properties.
