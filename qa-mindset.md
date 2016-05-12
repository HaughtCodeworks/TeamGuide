# QA Mindset

One important principle to apply when building amazing software applications is cultivating a QA Mindset while developing a product. QA is short for quality assurance, the maintenance of a desired level of quality in a service or product, emphasizing attention to every stage in the process of delivery or production.  More concretely, it's a set of principles and approaches used to ensure a software product works as expected and maintains its quality.

## Fostering a QA Mindset

Our team uses a review process for each change where a developer who didn't work on the change reviews and approves it before the client sees it. The following principles comprise what we consider the QA mindset.

1. Do you really understand what this feature or change is about?  How does it help your users?  How does it improve the product or make the lives of your customers better?  If you don't have the answers to these questions, how can you be sure the submitted change is of the highest quality and fit for the product?

2. Think about the user experience of the feature or change.  Is it intuitive? Does it make things too complicated?  Follow your gut and if you have any sense of doubt on a change, voice your concerns.  If you have any difficulties using a feature, it's likely users who are less familiar with the product will be even more frustrated.

3. Be a pessimist. Don't just rubber stamp the obvious, sunny day scenario.  What if you do something unexpected with the interface?  How well does the feature react?  If your team is developing a test plan for each feature, you can walk through each of those steps and include any additional scenarios you might come up with.

4. Get creative when you're testing. If you're filling out forms what happens if you submit it empty?  What if you put in nonsense data or something clearly wrong like 'lorem ipsum' when the input is asking for numeric data?  What if you put in a name that is 500 characters long?  You may think it's silly, but at some point a user will do something like this in production.  It's better to know what will happen and make sure it reacts as you'd expect.

5. Probe the restrictions. Test your web pages anonymously. If your system has different user permissions, see if you can get to anything you shouldn't be able to access.  Going further, can you use direct links to get to things you shouldn't be able to?  What if you use curl to post form data to different end points?  You may not be able to do it in the app's UI, but what if a hacker tried to submit different kinds of data to your end points?

You're not here to punish your fellow developers or make them look bad. You're trying to catch anything that will reflect poorly on your team and the product if users are the ones to find the issue. Be compassionate in how you bring forth your findings.  Being tactful is always the best choice, especially in the case where you're trying to find the flaws or faults in software your teammates are shipping.