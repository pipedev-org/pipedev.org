---
title: "What Makes a Pipeline Person?"
date: 2023-05-17
author: Ryan Bottriell
summary: "What is the role of a Pipeline TD, and is it changing?"
---

This month, Kirk asked to lead the discussion and came prepared with a list of questions to spark our discussion. This was our second in-person/hybrid event since COVID began and it continues to be a joy seeing everyone who makes an appearance.

## What Makes a Pipeline Person?

Firstly off, Kirk noted that often the Pipeline TD role is treated as a stepping stone - where folks expect to move on into other technology and software engineering roles over time. What if this wasn’t the case, however? What would it mean to make Pipeline TD a full career job, and, once you do, what does it mean to have a staff or principal pipeline TD?

As part of answering this question, we also wanted to discuss what actually differentiates a pipeline TD from other engineering roles. Closeness to production was a big factor here, which ultimately means that they have a more immediate impact and generally avoid working on development tasks that will take weeks or months to complete.

Another interesting note was the idea that the Pipeline TD role can change quite a lot over the course of a production, or even between productions. This ability to change focus and wear multiple hats is also typical for Pipeline TDs but not seen as much in other engineering roles.

In some ways, we pondered, the vagueness and uncertainty about the Pipeline TD role is part of what defines it for many people. Because the job is a lot of general problem solving, the day-to-day responsibilities can change drastically. This is compounded further when you account for the differences across studios of different sizes. Typically, smaller studios will broaden the roles of a Pipeline TD and may end up expecting them to take on longer term or more involved development if there is a lack of engineering resources (or none at all). 

### The Principle Pipeline TD

So what would a staff, senior staff, or principal Pipeline TD do? What happens to the role after “Senior Pipeline TD”, and what additional responsibilities could be expected?

Just like staff or principle engineers, they would still likely be expected to work on, or at least within, complex architecture - understanding and navigating impact beyond the scope of any one project or workflow.

Also like other engineering roles, they might be expected to have much more extreme depth of knowledge in one particular area of the pipeline and be an ambassador for it in their day-to-day work and amongst the larger TD team.

Perhaps they would also be expected to interact much more deeply with other engineering teams. In these interactions they could be expected to advocate for the development of in-between/glue/pipeline code that may often be considered too late by teams that are much more focused on an RnD-type project. Just like other engineering teams may be consulted on a project to understand its impact, this could be a formal responsibility for the Pipeline TDs who intimately know the various pipeline components and how they interact. 

Additionally, we think that these career-pipeline folks would advocate for best practices and devops workflows. They would take ownership of new pipeline code that comes from a project and work to improve, test, vet, and integrate changes for use in other productions.

Finally, these folks would likely be expected to represent their studios in the larger community. Attending conferences and meetups (like this one!), looking for and navigating collaboration opportunities with open source software teams or other studios. 

> Question for the audience: are there vertical slices of the pipeline that you could generalize and support across studios? Is there hope for open-source collaboration in this space?
Pipeline TD Role Over Time

We agreed, generally, that the “senior” title for TDs has become diluted over time. It used to come with more weight, but now can be achieved much earlier in one’s career. This is not inherently a bad thing, but does potentially expose a larger need to have new titles for those with additional experience in the role.

We took an informal poll to ask if anyone was looking to change the titles in Pipe TD land, but there was no strong sign from anyone that this was happening or needed to happen. That being said, we are a relatively small sample of those who would even be a part of such conversations.

### Show vs. Stream

This is an ongoing question in the community about how Pipeline TD teams should be organized. Do Pipeline TDs work in a centralized team for the whole studio, or are they assigned to specific shows? In either case, do they collaborate across the entire pipeline or do they focus on specific departments or streams (frontend depts, backend depts, etc)?

Our discussion showed that there’s a pretty big mix of these formats out in the wild. Sometimes studios will switch between these over time or even have a system which merges them in some way. For example, you might have some shows with dedicated Pipeline TDs and others that share them, but then also still divide the team based on each member’s best known area of the pipeline. Another example is having show-assigned TDs with a system of escalating issues to a central, shared team.

There was a general sentiment that having a centralized team can be nicer for those on that team (culture, comradery, support) but that often the production prefers to have someone deeply integrated into the team and available to support them without delay. 

Sometimes, the show-based TD is able to develop very efficient solutions for artists very quickly because they can collaborate with the artists more closely and already have important insight into the subtleties of the production. On the other hand, this type of development needs to be executed with a real concerted effort to communicate outside of the production or you can end up with code that is difficult to move between shows or that creates other knock-on issues in the pipeline.

### Support vs. Development

Rolling out of the last topic, we started to talk about what the division of works was for folks in the pipeline space. Ie what portion of your time is spent on support vs development?

In the end, we settled on a general ratio of 60:40, where it can swing back and forth over time from 60% development to 60% support but is generally in that range. To get to this number, though, we also had to discuss what the difference was between the two. 

Often, a support ticket requires code to be changed so how do you decide what is support and what is development. Triage and troubleshooting work is definitely support, for sure, but we still went back and forth on the differentiation for some time. In the end, the best distinction that we could muster was that any work related to maintaining a workflow or bit of functionality in the pipeline was support, and any change, addition, or augmentation to a workflow of bit of functionality should be considered development.

The hardest test of this definition is work that you need to do to make something faster because it can no longer support the scale of work passing through it. Ultimately, we decided that this is development because that something was built for a smaller scale, and is still working as such. You are therefore augmenting the tool in order to support this new requirement, which makes the work development, not support.

#### The "intended capabilities" Distinction

This destinction, where we are augmenting a tool beyond the limits of what it was built for, includes a particularly interesting insight. It hints at some kind of distinction around the capabilities which the pipeline was built for. If it was built with the intention of only being used at a smaller scale, then it is *development* when we expand the capabilities to include working at a larger scale. If it was already built with the intention of being used at a larger scale, then it is actually *support* if scenarios are found where it fails to meet that capability.

This categorisation mechanism is particularly challenging to use effectively when the intended capabilities of the pipeline are at all vague. In an ideal world, all capabilities are perfectly documented, such that everything that doesn't work "as advertised" leads to support, and everything beyond that is development. This is particularly challenging to define in the fast paced, dynamic, and complex environment of VFX pipelines. Despite this, it can still be very useful to use this disctinction when categorisating between *support* and *development* if we leave it open to reasonable interpretation, and foster an open, collaborative, and constructive culture to avoid abuse.

Here is an example categorisation of all Pipeline tasks which utilizes intended capabilities to distinguish between support and development:
* **Strategic Dev**: Enhancements to the capabilities of the tools and pipeline which are planned and prioritised through a global roadmap shaped by stakeholders (CapEx/OpEx mix).
* **Tactical Dev**: Enhancements to the capabilities of the tools and pipeline which are prioritised above strategic development because they are reasonably required for the immediate needs of specific productions.
* **Show Specific Tactical Dev**: This is a subcategory of Tactical Dev where the development made is only ever intended to be used on a particular production. (OpEx)
* **Strategically Aligned Tactical Dev**: Subcategory of Tactical Dev where there is progress towards the wider strategic direction, even if the progress is less optimally achieved (CapEx/OpEx mix). Strategically unaligned Tactical Dev can only be OpEx.
* **Pipeline Support**: Debugging, dev fixes, and general help, where the tools and pipeline do not seem to be working to their intended capabilities. (OpEx)
* **Production Support**: Debugging, asset fixes, configuration, setup, and general help where there is no reason to suspect the tools and pipeline are not working to their intended capabilities. (OpEx)
* **Triage**: Assessing the incoming requests into the above categories and starting the process for prioritisation or assignment. (OpEx)


### Spreading the Word

Our last topic/question for the evening was related to recruiting, and had us thinking about how we increase awareness for the technical roles in VFX. Many graduates or even experienced software engineers don’t know about the opportunities in our industry.

More technical courses in college and universities was one idea - just generally adding more cross-pollination of art and code at the academic level so that you don’t only see interest from those that already wanted to be in film.

The other idea was around increasing how much our industry is willing to share and communicate with the world at large and our engineering peers. We do some great sharing of ideas at VFX-related conferences, but our peers in other great technology companies write blogs, books and share much more code as open source projects than we do. Perhaps breaking down some of the high walls would help bring light to the work that we do and roles that exist.

Along the same lines, we are seeing the AI/ML industry throwing money at image generation and other image-manipulation technology, but not building on the file formats, tools and other lessons learned from the long VFX history. Perhaps the aforementioned community engagement could be valuable here not just for awareness but also for those on the other side.

### Until Next Time

This session was a lively discussion, and I hope that everyone involved enjoyed it as much as I did. You can always reach me via email or slack to suggest topics for the future or even if you just want to let me know of one or two questions that you’d love to have answered by our community.

Thanks for reading!
