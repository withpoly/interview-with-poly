<p align="center">
    <img src="https://withpoly.com/favicon.png" width="200px" />
</p>

# Interview With Poly

Thanks for your interest in Poly! We're excited to get to know more about you. This repo contains enough detail about our interview process to give you a great shot at landing a job here. While we know that our process isn't perfect, it is designed to get to a point where everyone on the team has high conviction in hiring you.

## The Interview Process

We have an extremely rigorous interview process, but we're very transparent about it along the way, and want to give you the opportunity to decide at any point if Poly is the right choice for you. That said, we also try to make the process fun (or at least what we all consider fun!), and edifying. And you can always give us feedback if that wasn't the case.

The interview process is going to look roughly like the following:

1. An introductory call with a founding team member (this is usually an outbound call, given that we are much more likely to find you than the reverse, but there are exceptions to this!)
2. You will talk to another team member, who will want to know more about your background, prior projects, and hard/interesting problems that you have worked on. We'll likely be basically grilling you on specifics, and this interview might come off as "insistent", or "demanding". This is only because we are essentially trying to dig in deep enough to where we're satisfied that you are deeply aware of the technical trade-offs of a given system.
3. We'll have you do a take-home project or exercise (most of you will come here because of that). You'll have essentially unlimited time to work on this, but the longer that you work on it, the higher the standard becomes. On the other hand, working more on this also shows higher passion and conviction. Overall, we are extremely comfortable with both the "ninja that did this in less than an hour" types, but also the more methodical types. So if you're in a hurry, give it a shot!
4. We will do a team-wide set of interviews where you will be speaking with everyone on the team. As long as we are small, we will operate on a consensus basis for hires, so we all want to be highly excited to hire you. Please see the "Team Interview" section for more information on how to prepare for this.
5. If we are all very high conviction in your capabilities after all those conversations, the last thing we will do is pay you to fly out to meet us, and work with us for a while (less than a week at most). You have agency in this, in terms of when you can come, how long you can stay, and what you want to work on while you're here. We hope you have fun!
6. Finally, we'll make you an offer and/or discuss logistics. In most cases, we'll have already discusses some of the specifics already, so this won't be full of bad surprises.

And that's "it"! You can obviously bow out at any time, and we will try to not waste your time if things aren't looking like a strong fit.

## Team Interview Instructions

### Overview

Interviewing 1-on-1 with each team member will likely be a bit stressful. This section is intended to give you a brief overview of what our interviews are like, and how you can be unnaturally well-prepared to ace them.

First off, the interviews will be technical, and you will be expected to have a strong working knowledge of one language. You can choose that language for yourself, and you have latitude to do anything in pseudo-code if you are a bit fuzzy on the specific way to write something out.

Second, the interviews will be more about gauging your comfort with solving these kinds of problems on a day-to-day basis, so we always give you problems that we have specifically encountered in our work at Poly. The main question we want to answer is: "is this the kind of person that can do this kind of stuff every day?".

## Preparation

> **Important**
> Please install VSCode and install the [Live Share plugin](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare). This will allow us to collaborate on a code editing exercise.

### Specific Practice Activities

* The best practice you can do is to actually just take a few hours to build a tool, package, module, or repo from scratch. For python programmers, an easy thing to work on would be a CLI tool built in a tool such as [Typer](https://typer.tiangolo.com). You should try and create a CLI tool that does something like, e.g. print out a fractal in ASCII. Something complicated enough to be challenging but satisfying. Make sure you get practice with stuff like classes, list/dict comprehension, and syntax stuff like loops. That way, when you do your interview, you can focus on the problem and not the syntax.
* If you are doing more ML work, you should have a strong working knowledge of Pytorch and/or Numpy. You should be able to do things like finding the argmax of a tensor along some dimension, etc. Really just standard stuff that implies that you can work "natively" in pytorch. You should also have a precise understanding of how backprop works in code as well as in theory (but we won't make you write out equations, we promise!).
* If you are a front-end person, I would get a test project set up in [Nuxt 3](https://nuxt.com), which is the frontend framework we use. Though you will not be required to know Nuxt as a condition for being hired, the more you know the better your chances. Note that we aren't dogmatic about frameworks -- you will have more than enough leeway to convince us out of Nuxt if you so choose. We're excited when people argue with us about technical decisions (seriously!) because it implies passion.
* Be yourself, and don't feel expected to have to know everything. The interview is as much about reacting as it is to knowing.

## Technical Interview Instructions

The take-home kit is designed to help you showcase your skills in a much more thoughtful setting than a stressful real-time programming interview. These questions are designed to take a few hours. While we can't compensate you for the time you spend answering these questions, we hope that the experience of doing these problems is informative and educational. If not, we welcome any feedback on the interview process (which you can send alongside, or in lieu of, your code submission).

### Environment Setup

1. Clone (don't fork!) this library to your local system and create a new repo under your own name. This will allow you to submit your work by sharing your repo address and we can simply set one of our remotes to your repo to inspect your code against ours. However, forking this repo will make your answers visible to other candidates, so please don't do that.
2. Open the repo in your editor of choice (we _highly_ recommend Visual Studio Code)
3. You only need to answer the question(s) relating to the skill set you have. You can of course look at any problem but you shouldn't feel required to address other questions.
4. Look at the readme in that question in order to get more specific instructions
5. Place any build/run code in the folder with the README, and provide us with some instructions on how to dive into your code.

### Rubric and Success Criteria

Our primary goal is to give you the opportunity to show off your skills. If you are good at something, e.g. a particular library, threading, async, numpy jujitsu, etc. you have the opportunity to show it off in the context of your interview question. More specifically, here's how we evaluate your code:

1. **Did you understand the "hard part" of the problem and craft a succinct solution?** We want to know if you have the ability to find clever and functional solutions to hard problems. We are not interested in whether your code is optimized beyond broad O(n) considerations. So optimizing for number of lines of code, etc. is not meaningful to us. You can always add comments to help explain what optimizations you left out for time's sake
2. **Does your code exhibit high quality and logical structure?** Did you adhere to abstractions? Do your classes make logical sense? Did you use good programming patterns?
3. **Can we verify your solution?** Does the code run, or compile? Instructions do not need to be extreme, just some way to wrap our heads around what you've done.

### Stuff that doesn't matter

1. Writing unit tests
2. Fully-type hinted code
3. Complete analysis, charts, ablations, etc.

### Interview Questions

Please see the individual folders for questions

### Asking for clarification

If you have any clarifying questions about your interview prompt or the interview process, feel free to open a github issue here on this repo as well and I will try to address the question there.

### Submitting your result

You can e-mail us at [work@withpoly.com](mailto:work@withpoly.com) with a link to your repo.

> **Warning**
> Please do not open a pull request against this repo! That will make your
> submission public to anyone and easily searchable.
