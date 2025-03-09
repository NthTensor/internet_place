+++
title = "Becoming a Contributor"
date = "2025-04-09"
+++

Any healthy community project attracts a crowd of people who want to help out, but don't know how. The [Bevy Game Engine][1] gets a lot of these people, which is great. I am an infrequent contributor to bevy and am somewhat active in community discussions, and so I'm occasionally in a position to offer advice to people caught in this situation. To make things easier, I thought I'd collect this advice into an article so I can easily link to it.

If you did get linked here from bevy you should also take a look at the [Contributing Guide][2] (which, incidentally, I helped write). If not, the advice I'm going to offer should be generally applicable to most open source projects.

This advice is aimed mostly at junior devs - especially those new to open source. If you're more experienced, the advice probably won't be very interesting.

Now, when you're first starting, out I recommend doing four things:
1. Offer to do tiny longstanding chores.
2. Study the code and take notes.
3. Ask questions in code-reviews.
4. Attempt ambitious projects and refactors.

## Tackle Tiny Chores
Starting small is the most obvious approach, and it's a good one. Most projects have a mountain of tiny little chores that no one ever seems to get to. Probably because the more senior contributors are preoccupied with larger problems. Part of why new contributors are valuable to projects is exactly that they can help tackle this backlog (with the other part being that they sometimes grow into senior contributors and help sustain the project).

The main thing you will get out of chores (apart from an exercise in self-discipline) is experience with the tooling and process in a low-stakes environment. If you're new to the language, or for example `git`, chores are the way to level up your skills until you reach basic proficiency. If you already have basic technical proficiency, it will still teach you about the social conventions and process particular to the community you are joining.

## Study The Code
If the previous section seemed obvious, this one may not: You should get out a pen and paper (or whatever note-taking app you prefer) and read the entire codebase top-to-bottom like a "Choose Your Own Adventure" novel. Pick an an example or some well-isolated top level logic, and open it in an editor with *go-to-definition* support. This is the "top" of your call-stack; from there you should trace down all the definitions, reading and annotating as you go, until you reach the "bottom" and your code hits the underplaying API calls. Your goal here is to produce an architectural overview describing all the layers of abstraction you encounter and how they fit together. If you stick at it, you should end up with something like [this][3].

I sense, some of you may have some concerns...

The first thing I want to assure you is *you can do this*. If you can write code, you can read it. Code comprehension is a skill, and like all skills you can develop it through regular exercise, even if it feels strange at first. The second thing you should know is: there is no substitute. The other things on this list will teach you the tooling and the process, teach you to make good engineering and design decisions, teach you where the codebase is going. But nothing will familiarize you codebase as it is like buckling down and reading it.

I don't think it's controversial to say that most codebases are poorly documented. Even those that are not tend to lack broad architectural overviews, or cohesive visions of how all the pieces fit together to make the whole. Those diagrams usually exist only in people's minds. If you've only worked on your own projects before, you've gotten those mental models for free. But when you are interacting with code written by others, potentially hundreds or thousands of others, you'll need to spend time to grok (a [wonderful term][4] from a [horrible book][5]) the existing structure. It won't necessarily happen on it's own. 

Note that you don't have to actually complete your architectural review for it to be a useful exercise. About 20%, or just enough to know how the lower-level API calls relate to the top level abstraction, is probably enough to get you to where you need to be.

## Ask Questions In Reviews
Bevy, like some other open source projects, has a [community review process][7]. Alice's article lays out how it works, so I'll just pick out the most salient point,

> Anyone (literally, anyone) can review a PR. GitHub just lets you do it!

Now I'll let you in on a little secret: Even if GitHub dosn't let you hit the "approve" button for your particular project, you can almost always leave comments on open PRs pointing out errors or asking questions. When you're just starting out, my advice is to do this a lot.

First, obviously, you've got to read the PR over. Don't leave review comments on PRs you have not read. But, if you followed the advice from the previous section, reading code should already feel natural to you. But this is a little different: when doing an architectural review, all you care about is how things fit together. When reviewing a PR, you should also be truing to ascertain if it is *correct*.

I'll warn you upfront: checking code for correctness is hard. How hard depends on the domain, but it's always hard. As a new contributor, you are likely to immediately run into code you either don't understand, or misunderstand (and which you may therefore incorrectly identify as an issue). This is fine and expected. So what you should, considering that you may make frequent mistakes, is (a) be polite and (b) ask a lot of clarifying questions.

Most of the time the author will be happy to explain, but sometimes you will actually catch bugs just by asking about confusing bits of code! The confusing bits are the most likely to be wrong. So the project gets additional valuable scrutiny on it's PRs, and you essentially get mentored by the author for a bit. As an aside, please try to be mindful of the author's time when following this advice. Ask for additional information, not additional work.

## Attempt Ambitious Projects
Many contributors seem to tend naturally to this particular approach, and I can hardly blame them. Ambition is a great motivator, and it seems to me to be selected for in the population of people who decide they want to "get good" at open source. My advice here is to temper your expectations, but to let yourself be ambitious. 

Once you know the code well enough to have opinions about improving it: follow those feelings - with the knowledge that your first few big projects are probably not going to make it to completion. Part of becoming a seasoned contributor is, honestly, fighting with big changes and finding out they have hands. Do not be discouraged, either by feeling you need to give up on a branch, or by the idea that you might not be ready because failure is possible.

`Note to self: Redraft this section.`

## Summary

Eventually you will find:
1. That the chores are no longer a good use of your time.
2. That you need to read up on the code less and less
3. That your questions reveal more and more issues.
4. That your ambitious projects actually succeed.

Congratulations, you're now a senior contributor.

[1]: https://bevyengine.org
[2]: https://bevyengine.org/learn/contribute/introduction/
[3]: https://hackmd.io/@bevy/rendering_summary
[4]: https://en.wikipedia.org/wiki/Grok
[5]: https://en.wikipedia.org/wiki/Stranger_in_a_Strange_Land
[7]: https://www.leafwing-studios.com/blog/triage-by-controversy/
