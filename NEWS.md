
## RStudio 2023.05.0 "Mountain Hydrangea" Release Notes

### New

#### RStudio IDE
- Updated to Electron 23.3.0 (#13030)
- Moved Help panel font size setting to Appearance tab in Global Options (#12816)
- Update openssl to 1.1.1t for Windows (rstudio/rstudio-pro#3675)
- Improve visibility of focus rectangles on Server / Workbench Sign In page [Accessibility] (#12846)
- Added ability to enable minidump generation for Electron crashes (#13025)

#### Posit Workbench
- Added the `session-connections-block-suspend` session option, controlling whether active connections can block suspension of an R session.
- Added the `session-external-pointers-block-suspend` session option, controlling whether R objects containing external pointers can block suspension of an R session.
- Added http server request processing statistics for the rserver, logged as info/debug messages, controlled by the option `www-stats-monitor-seconds` in rserver.conf (rstudio/rstudio-pro#4554).
- Updated code server to 4.12.0 to address security vulnerabilities
- Updated nginx to supported version 1.24.0 (rstudio/rstudio-pro#4532)

### Fixed

#### RStudio IDE
- Fixed display problems with Choose R dialog when UI language is French (#12717)
- Fixed focus switching to Help Pane search box after executing ? in the console [Accessibility] (#12741)
- Fixed initial focus placement in Help Pane [Accessibility] (#10600)
- Fixed invalid element role on session-suspended icon [Accessibility] (#12449)
- Improve screen-reader support for Console pane toolbar [Accessibility] (#12825)
- Background script jobs are now run using the global environment. This fixes the behaviour of `source()` in backgrounds jobs. (#11866)
- Fixed bug that caused Update Available dialog to show after the user selected to Ignore Update (rstudio/rstudio-pro#4179)
- Fixed bug that prevented updating to the latest release if version was previously ignored (#12874)
- RStudio no longer uses `reg.exe` when attempting to enumerate R versions in the Windows registry (#12599)
- Fixed file-type icons not displaying in Finder on Mac (#12252)
- Fixed saving and restoring window location when maximized or partially offscreen (#12463)
- Fixed display of macOS message dialogs (#12928)
- Set theme of menu bar, title bar, and dialogs (dark vs. light) based on RStudio theme (#12247)
- Fixed issues with mouse back / forward navigation in Source pane, Help pane (#12932)
- Fixed opening files from command-line with relative paths (#12495, #12563)
- Fixed issue with column preview with older versions of the 'pillar' package. (#12863)
- Fixed bug where the OK button was disabled in Choose R dialog when only one version of R installed (#12916)
- Improved robustness when chosing custom R version in Windows desktop (#12969)
- Fixed bug that prevented RStudio Desktop from starting on Linux if desktop.ini was unreadable (#12963)
- Improved RStudio Desktop startup behavior when user state folder inaccessible (#12988)
- Fixed saving files to UNC paths on Windows (#12652, #12935)
- Fixed window disappearing when restoring from maximized on macOS (#13010)
- Fixed Project Build Tools preferences pane showing &mdash text in French UI (#11134)
- Fixed inserting cross references in a Quarto document showing no references (#12882)
- Fixed keyboard shortcut help not displaying in Emacs or Sublime Text mode (#11376)
- Fixed issue with rendering development documentation with R 4.3.0 (#12945)
- Fixed issue with use of "Whole word" with Find in Files search (#13017)
- Fixed issue with diagnostics freezing session with documents containing pipebind operator (#13091)

#### Posit Workbench
- Fixed unlabeled buttons for screen reader users when page is narrow [Accessibility] (rstudio/rstudio-pro#4340)
- Removed redundant mouse-only New Session widget from accessibility tree [Accessibility] (rstudio/rstudio-pro#4338)
- Fixed launcher error details not showing on the homepage when clicking "Error Details" (rstudio/rstudio-pro#4333)
- Fixed theme button's semantics so it is meaningful to screen reader [Accessibility] (rstudio/rstudio-pro#4337)
- Fixed screen reader accessibility for the homepage theme dropdown menu [Accessibility] (rstudio/rstudio-pro#4339)
- Fixed hidden controls on Session Info dialog remaining active [Accessibility] (rstudio/rstudio-pro#4341)
- Add keyboard support to the "Show list" control in New Session dialog [Accessibility] (rstudio/rstudio-pro#4461)
- Fixed job details to be hidden from screen reader when visibly hidden [Accessibility] (rstudio/rstudio-pro#4466)
- Fixed sign-in pages to be more mobile and zoom friendly [Accessibility] (rstudio/rstudio-pro#4472)
- Cache results for user and group lookups (rstudio/rstudio-pro#4451)
- Increase timeout for stale messages error (rstudio/rstudio-pro#4325)
- Reduce database queries and remove locking around DB calls (rstudio/rstudio-pro#4492)
- Eliminate assertion failed error when reloading config with load balancing enabled (rstudio/rstudio-pro#4504)
