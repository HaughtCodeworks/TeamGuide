# QA Mindset

One important principle to apply when building amazing software applications is cultivating a QA Mindset while developing your product.  I'm not sure where I first heard this mentioned, but Rand's post on the subject stuck with me. [The QA Mindset](http://randsinrepose.com/archives/the-qa-mindset/).  If you haven't read it, make a point to do so.

## What is QA?

First, let's cover the basics of what QA is before we proceed. QA is short for quality assurance, the maintenance of a desired level of quality in a service or product, emphasizing attention to every stage in the process of delivery or production.  More concretely, it's a set of principles and approaches used to ensure your software product works as expected and maintains its quality.

Defining quality is a subjective matter. There are [books](https://en.wikipedia.org/wiki/Zen_and_the_Art_of_Motorcycle_Maintenance) written about it. Suffice it to say that in order to build an amazing product your quality needs to be the highest you can manage.

When I got started in the IT industry in the 1990s, most places I worked at had a dedicated QA department.  Their entire job was testing the product.  It was nice to know that every change was thoroughly reviewed and issues were caught before they got into production.  While there are obvious pluses to this there are also some downsides, namely added cost and extra time to get features into production.  Back then things moved more slowly and many products were only updated on a monthly (or longer) basis.

Today things have shifted as more software products are being built by smaller teams, without the staff or resources to run a QA department.  None of the projects I've worked on since 2004 have had a dedicated QA person, let alone a team.  So how do smaller teams manage quality?  Typically the developers or the product team will test new features themselves.  They optimize for shipping features quickly and if a bug appears, they focus on fixing it just as fast.  Sometimes they lean on their user base to catch errors, preferring to get software into the hands of users as early as possible.

Is this a good trend?  My answer is yes, as long as the task of ensuring quality is not lost.  Enter the QA mindset.

## Fostering a QA Mindset

We know we need to own our product's quality, so how does the QA mindset fit into that exactly?  It is a shift in thinking that we can't just let the product team or a QA department make sure we're delivering quality features in our software.  We have to look out for this ourselves.  Our team uses a review process for each change where a developer who didn't work on the change reviews and approves it before the product team/client sees it.

The following principles comprise what we consider the QA mindset.  On your next feature or bug fix, keep them in mind as go about your work.

1. Do you really understand what this feature or change is about?  How does it help your users?  How does it improve the product or make the lives of your customers better?  If you don't have the answers to these questions, how can you be sure the submitted change is of the highest quality and fit for the product?

2. Think about the user experience of the feature or change.  Is it intuitive? Does it make things too complicated?  I typically follow my gut and if I have any sense of doubt on a change, I voice my concerns.  If you have any difficulties using a feature, it's likely users who are less familiar with the product will be even more frustrated.

3. Be a pessimist. Don't just rubber stamp the obvious, sunny day scenario.  What if you do something unexpected with the interface?  How well does the feature react?  If your team is developing a test plan for each feature, you can walk through each of those steps and include any additional scenarios you might come up with.

4. Get creative when you're testing. If you're filling out forms what happens if you submit it empty?  What if you put in nonsense data or something clearly wrong like 'lorem ipsum' when the input is asking for numeric data?  What if you put in a name that is 500 characters long?  You may think it's silly, but trust me at some point a user will do something like this in production.  It's better to know what will happen and make sure it reacts as you'd expect.

5. Probe the restrictions. Test your web pages anonymously. If your system has different user permissions, see if you can get to anything you shouldn't be able to access.  Going further, can you use direct links to get to things you shouldn't be able to?  What if you use curl to post form data to different end points?  Sure, you may not be able to do it in the app's UI, but what if a hacker tried to submit different kinds of data to your end points?

One thing to remember through all this.  You're not here to punish your fellow devs or make them look bad. You're trying to catch anything that will reflect poorly on your team and the product if users are the ones to find the issue. Be compassionate in how you bring forth your findings.  Being tactful is always the best choice, especially in the case where you're trying to find the flaws or faults in software your teammates are shipping.

## Making it a Habit

Using a QA mindset while you program may not be something you or your team do.  Make it a habit. Create a checklist of these principles and consider each point before you consider your work done.

I have noticed one thing over years of encouraging a QA mindset on my teams.  It becomes second nature after a while.  When I'm working on a feature these concerns spring to mind automatically.  I think of it as a form of defensive programming.  If you practice thinking this way, it'll start coming easier for you as well.

## Product Benefits

Every product and business is different, and your project's tolerance for risk will drive how robust your QA process should be.  In mature software products,
the business knows the value of QA and has it integrated into their process. Having a QA mindset still benefits the developers by allowing them to move quickly and avoid unnecessary delays in new releases.

I see even larger gains with startups where the focus is on speed.  Uncaught bugs and untested features could easily erode confidence in the new product and lead to a loss in traction.  Knowing your development team can not only ship features quickly but avoid these costly mistakes may be the edge your fledgling app needs.

With the latest trends toward faster, more efficient software teams, having developers own their own quality is more important than ever.

Though it takes intention and practice to hone a QA mindset, the upside of how it can help your team and product is worth it.  Consider how these ideas can be brought into your team today. Happy shipping!