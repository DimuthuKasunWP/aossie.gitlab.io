
## Mind The Word

### Idea: Firefox and Safari Ports

#### Description

Mind The Word (MTW) is a browser extension that helps users to learn vocabulary of new languages. When visiting a webpage written in the user's native language, MTW will randomly translate a specified percentage of words into the language that the user wants to learn. By seeing the new words in context, the user will be able to infer and memorize their meanings.

MTW was originally implemented for Google Chrome around 2011, and in 2016 a GSoC student [partially ported it to Firefox](https://github.com/OiWorld/MindTheWordFirefox), after having implemented many other features. The port was not complete, because Firefox's browser API did not contain all the features on which MTW for Chrome relied. Moreover, the Firefox port is completely independent from the original Chrome extensions, and hence the two do not share code. This means that they need to be maintained separately, and users of Firefox and Chrome might have different experiences when using the corresponding MTW versions.

In this project idea, we would like to revisit this goal. We would like to:

1. Complete the Firefox port.
2. Port the extension to Safari as well.

Moreover, the ports should preferably be done in a modular way, to increase code sharing and code reuse. This has been successfully done in [another project](https://www.gitlab.com/aossie/CarbonFootprint); and we recommend inspecting its code to evaluate whether something similar would be feasible for MTW.

A proposal to work on this idea should carefully inspect which features of Chrome's API MTW is currently using and check that they exist in Firefox's API and in Safari's API as well. And if they don't, the proposal should propose suitable workarounds.

#### Requirements

For this project, we are looking for a student with:

- excellent knowledge of Javascript, HTML, CSS.

- good software engineering skills, in order to produce modular and reusable code across all ports.


#### Mentors

Rohan Katyal, Bruno Woltzenlogel Paleo

