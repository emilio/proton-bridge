## v1.6.6
- 2021-03-04

### New

- Allow to choose which keychain is used by Bridge on Linux
- Added automatic update CLI commands
- Improved performance during slow connection
- Added IMAP requests to the logs for easier debugging

### Fixed

- Fixed update notifications
- Fixed GUI freeze while switching to early update channel
- Fixed Bridge autostart
- Improved signing of update packages
- NoGUI bulid
- Background of GUI welcome message
- Incorrect total mailbox size displayed in Apple Mail


## v1.6.3
- 2021-02-16

### New

- Added desktop files and icon in Bridge repo
- Better detection of MacOS version to improve automatic AppleMail configuration
- Clearing cache after switching early access off

### Fixed

- Better poor connection handling - added retries for starting IMAP server after the connection was down
- Excluding updates from 'clearing cache'
- Not allowing copying from Inbox to Sent and vice versa
- Improvements to moving messages (unlabelling folders)
- Fixed the separation of release notes for 'early' and 'stable' channels


## v1.6.2
- 2021-02-02

### New
Introducing silent updates

- Introducing 'early' and 'stable' updates channels
- Allowing users to enable early access from within the GUI
- Adding and option to disable silent updates in settings

Changing the distribution of release notes

Performance and stability

- Implement support of UID EXPUNGE - to avoid avoid unnecessary resync
- Improve memory usage - gopenpgp dependency updated to v2.1.3
- Reducing network traffic by caching message size and body structure

Adding a scroll bar to the settings tab

### Fixed
- Fetch errors - introducing a stop to the imap server once there is no internet connection
- Setting up flags to avoid messages misplacement
- Inline messages incorrectly changed to attachments 
- Reporting bug from accounts with empty account name
- Panic when stopping import progress during loading mailboxes info
- Panic when modifying addresses during changing address mode
- Panic when trying to parse a multipart/alternative section that has no child sections
- Prevent potential loss of messages when moving to local folder and back


## v1.5.7
- 2021-01-21

### New
- Improvements to message parsing
- Better error handling
- Ensured better message flow by refactoring both address and date parsing
- Improved secure connectivity checks
- Better deb packaging
- More robust error handling
- Improved package creation logic
- Refactor of sending functions to simplify code maintenance
- Added tests for package creation
- Support read confirmations
- Adding GPLv3 licence button to the GUI
- Improved testing


### Fixed
- AppleMail crashes (related to timestamps)
- Sending messages from aliases in combined inbox mode
- Fedora font issues
- Ensured that conversations are properly threaded
- Fixed Linux font issues (Fedora)
- Better handling of Mime encrypted messages
- Bridge crashes related to labels handling
- GUI popup related to TLS connection error
- An issue where a random session key is included in the data payload
- Error handling (including improved detection)
- Encoding errors
- Installation issues on linux
