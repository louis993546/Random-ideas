# GitLab CI Dashboard app

## TL;DR:

- A less convoluted way to setup a "TV style" dashboard for GitLab CI
- Up-to-date tech (2019)

## What we have right now

1. GitLab website
2. `/general-dashboard`
   - not being maintain anymore

## My priority

- Efficiency
  - It shouldn't require any powerful hardware
  - It shouldn't post (noticable) strain on GitLab
- Security
  - It should have as little access right as possible
- Maintainable
  - Up-to-date tech stack
  - Good architecture
- UX
  - Easy to understand for developers (the target audience)
- Flexibiltity
  - Since GitLab can be self-host, it should leave some wiggle room for user to configer their dashboard accordingly

### Implication

- Server should be optional
- HTTP pooling frequency needs to be configurable
- Uses Android secure storage for GitLab API key (for pooling)
- Just use the standard MD libraries

## Implementation

### Rejected options

- Hosted React webapp
  - Hosting cost money
- Self-host React webapp
  - Kinda contracdict the point of the whole thing: easy to setup
- Electron app
  - Needs a super computer just to show a dashboard

### Option 1: Android app (design for tablets)

- Shows a grid/list of existing branches

### Option 2: Android TV app