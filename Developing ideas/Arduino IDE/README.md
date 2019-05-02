# Arduion IDE

- I am sure that a million people have already done this kind of project
- The specific goal of this one
    - Super easy for beginner to use
        - Code completion
        - Easy to navigate through codes
        - Good onboarding to get things started
- See how it can be integrated with virtual breadboard
- If it can integrate a Arduino simulator that's be great
    - Basically simulate the whole ATmega 168 micro controller
    - If this works it would be the biggest feature
- Right now I am in favor of forking IntelliJ CE
    - It's code completion is just too good
    - It's UI is flexible enough to accommodate the panels that needs to be added for the features

## Headline feature: Arduino simulator

- Technically that would be a project on it's own, but the integration is what makes it special
- How it works (as a user)
    - You code a bunch of stuff
    - You click "Run" and select a new Arduino ${boardVariant} simulator
    - A Panel opens with all the pin's output
    - You can click on the pin to simulate button click
    - On the RHS is a panel for user to enter some kind of scripting language to run long operations on GPIO
        - e.g. repeat(forever(), 5000) { click(pin2) }