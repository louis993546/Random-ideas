# reMarkable template manager

## Existing solution
- (I think I saw 1 on GitHub. That might be the final nail to this coffin)

## Goal

- Make it easy to manage templates in your reMarkable tablet
  - template PNG
  - template list JSON
  - (Hopefully) icon

## Implementation

- Procedures
  1. User pluged in the USB cable to enable SSH
  2. User opens the app (desktop or mobile) and make sure it is accessible
  3. User sees the list of templates on device
  4. User can select one/multiple, and delete them
  5. User can also upload local PNG, and then it will ask for the data
- Execution
  - Probably directly using SSH
    - Some on-boarding process to ensure SSH is open
  - Desktop app makes more sense
    - You are probably not going to use it very often, especially on the go
    - You need USB to trigger SSH to start anyway
    - I can start with CLI, and add a UI wrapper later
  - JSON management is crucial
    - Always have backup/fallback
    - Avoid manipulating the whole list. Always try to just add/edit 1 object
    - Mapping it to type-safe object first might be a good idea
      - Find/replace/edit item in list is usually safer than edit JSON directly
      - i.e. strictly-typed language FTW
    - See if it is possible to check firmware version before doing anything
  - icon is gonna be a problem
    - Need to find out what `iconCode` actually refers to
    - Need to find out if putting new icon is even possible
