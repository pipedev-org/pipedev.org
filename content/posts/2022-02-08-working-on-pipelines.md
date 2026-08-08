---
title: "Working On Pipelines"
date: 2022-02-08
author: Ryan Bottriell
summary: "What is a pipeline and what do pipeline developers do all day?"
---

In this forum, we sat down to discuss pipelines in general and what it means to work on pipelines every day. As you'll see, our conversation didn't really get into the day-to-day, but we did talk more philosophically about pipelines and discovered some really interesting points of view from around the industry that exposed some of the reasons why it seems like "pipeline" is sometimes such a hard term to define.
As with the last couple of meetings, I tried to run things in a general lean coffee format. We spent ten minutes on each question/topic and then voted whether or not to move on. This helps to keep the notes nice and organized into topics, as well has helped to ensure that the group can stay engaged (hopefully).

## Working on Pipelines

### What is a pipeline?

…Was a great first question! We tried our best to define what we're really talking about when we say "working on a pipeline".

Some of the initial definitions that were proposed were around the idea of data transfer and translation, as well as automation. Although these things are definitely a big part of what pipeline software need to do, they are not a complete definition on their own.
We also talked about the idea of removing friction for artists and production. One could argue that a pipeline's job is to do pretty much anything that allows these folks to do their jobs more effectively and efficiently.

However, with that said, we also acknowledged that "The Pipeline" is a term that is not reserved for technologists, and exists whether we build tools to help out or not. In other words, the pipeline is ultimately just the process of taking ideas and turning them into content, but as pipeline developers, we are tasked with codifying pieces of that process whenever it's valuable to do so.
The common but effective analogy was brought up here, comparing media pipelines to any other factory or material production process. Raw goods (ideas) come inone side, and finished goods (pixels) go out on the other. Along the way, it passes through different departments and different people - following a designated path.

### What makes a pipeline good or bad?

This one seemed like a natural follow-up to the first, and at this point, we were talking more specifically about the pipeline software that we build every day.

Some initial thoughts came through along the lines of it should be portable, scalable, extensible - all of which feel very familiar to software engineers when we talk about what makes any software "good" or "bad".

At this point, it was brought up, that perhaps the real measure is just whether or not people want to use it. It's long been said that VFX studios are not software companies, and whether you agree with this sentiment or not it reinforces the idea that our pipeline code is only as "good" as the value that it provides to the business and the business values pixels. In this case, if the pipeline helps people those sweet pixels, then who's to argue that it's not "good"?

Well, maybe pixels aren't the end-all-be-all… At the end of the day, we all usually realize at some point that delivering even a small feature that improves the quality of life for some artists or production people can mean a lot to them - regardless of if it truly makes them more efficient.

To make things even more confusing for everyone, we then ran into another set of opposing forces: We often consider good pipelines to provide consistency and structure to the process, making things reliable and reproducible. However, just like we talked about earlier, a pipeline must also remove barriers and be as flexible as needed to allow the artists to do their best work (letting people go off-pipe).

We didn't get to a full conclusion here, but in general, we were converging on this idea of support, and that a good pipeline provides as much flexibility as it can without reducing its ability to streamline, and automate in the name of efficiency. This is a tough balance and one that leans more one way or the other depending on the project and studio.

### What is the division of time in pipeline?

This question was posed more as a poll of the room, basically asking how much time each person was spending doing new development vs. design vs. support vs. management work.

Of the specific answers, we saw things like…

- 50% design, 50% implementation
- 60% development, 20% support, and 20% meetings
- mostly DevOps, some proposals, some code cleanup and maintenance

…But the more interesting discussion was around what we considered made an impact on the day-to-day. First of all, is the production lifecycle. As a pipeline dev supporting one or more shows, those shows can have very different needs depending on where they are.

For example, shows that are starting up usually need lots of new tools to support a new look or new workflow. As the show gets into shot work this starts to shift, and by the time they reach delivery, it's all about bug fixes and immediate support.

The other major contributor that stood out to us was studio size. At smaller shops, the pipeline dev is often asked to wear even more hats than usual. They also might be even more limited in resources, needing to direct their attention to the work that allows them to be the greatest force multiplier. Similarly, a large studio has the time and need to invest in longer-term infrastructure projects that can properly scale and be used across a great number of projects.

This discussion got us wondering about our long-standing inability to really describe what a pipeline is outside of vague concepts, and how the broadly different roles that pipeline developer takes on in these different contexts may help to explain that struggle. This leads to our next question…

### What is NOT a pipeline developer's responsibility?

Right off the bat, the first thing that I think we all agreed on was that shot work should not be considered a responsibility of pipeline. By shot work, we are talking about the type of work usually assigned to a dedicated artist. Pipeline devs shouldn't be asked to animate a shot, for example. Although it seems obvious, sometimes the line can get blurred.

This is even more true for IT support. Pipe TDs are so often the first line of defence for production tickets and issues, but that often also means that they get asked IT questions about account permissions, access, software licenses, etc. Truthfully, the difference is not always an easy one to see for those submitting tickets.

Colorspace issues is another technical domain that often feels like pipeline but sometimes involves a deeper domain knowledge than is reasonable to expect from a pipeline dev. There's a caveat here as well, because sometimes in smaller studios the pipeline department is often the first and last team for lost support issues. What I mean by this is that when an issue makes the rounds and there's no one to resolve it, often it falls to pipeline to just figure out on their own.

We also talked about the design process, and the opinions were a bit split. In general, there was the sentiment that pipeline should not be responsible for determining workflows and how tools should be used in production. There are more fuzzy lines here, but the idea of having a product owner or representative user to provide requirements is always a good idea if you have the means.

### Pipeline rebuild vs rework?

This question is an age-old one, and for the sake of word count, I'll summarize this a little bit:

- Choosing a tech stack is not a unique problem to VFX, so there are lots of resources online to help with this.
- VFX work is always pushing us forward and changing, so we shouldn't necessarily believe that any pipeline tools will last very long
- We should be re-evaluating our code and feature set constantly to determine if are we doing well and progressing towards a better future

We also had a discussion comparing monolithic to modular codebases. The promise of something that is modular is that you can replace components without restarting entirely. In a modular system, you are basically admitting up-front that you are going to rebuild pieces of it later on. Our general experience is that a monolithic codebase can be easier to maintain as a small team, but tends to run up technical debt faster if you are not diligent.

### What are the current trends in pipeline and what does the future look like?

Ingest and delivery continue to be constants, and are ripe for possible innovations. Maybe USD will help here but there's no clear future.

The other big thing that is still top-of-mind for most of us is remote work. It definitely feels like it's here to stay, in one form or another. The one interesting insight is how little of an impact going remote has had on productivity. Whether this is sustainable as a culture is an open question, but it certainly helps to solidify the future of remote as an option in some form.

Being "cloud-native" still feels like a bit of a trend, too. There are other efforts like nimble collective and WetaM which present cloud-based creative workflow as well. It's still not clear to us if the cloud is really the future, and there is at least a little feeling with some that these conversations are getting stale and/or repetitive.

Some other points that came up:

- feels like we are seeing fewer projects that go with a single vendor, creating much more collaboration between studios
- a lot more conversations coming up about Rust as a language, so it definitely feels like a likely future
- game engines and realtime technologies (Unreal, Unity, Omniverse) continue to see more use and are empowering less-linear pipeline workflows
- virtual production is already happening a lot but the demand seems to only be growing
- digital humans, scanning, deepfakes, face swapping, de-ageing continue to be of interest and are starting to see much more application of AI and machine learning

## Final Words

Thanks again to everyone that showed up and made this discussion super interesting. As usual, I am always looking for ideas for future discussion topics and welcome any feedback on the notes or the events.

Thanks for reading!
