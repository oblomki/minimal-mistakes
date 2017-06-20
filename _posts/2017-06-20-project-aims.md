---
published: false
---
## Project Goals

What's the point of re-writing my app yet again? Well, I've tried in Laravel and find it becomes messy with so many files and folders. I want to compare it with another language and framework to see whether rapid prototyping can be easier and faster. Perhaps I will find that Laravel really is as good as it gets, but the only way to know is to explore other options. 

I also want to learn a more generally applicable language, like Python, as that will open doors to other avenues, such as data analysis.

So, my checklist:

- A framework with rapid generation, little configuration, and a robust app in as few lines as possible. 
- Authentication, Attachments, oAuth, mail (including for Gmail and Outlook APIs), scheduling must be taken care of with strong existing libraries. I certainly don't want to write that myself.
- I may try to separate the front and back ends: PHP/Ruby/Python on the back end, with Vue JS on the front. This way, perhaps I can get to a point where I know the back end works, then stop making further changes to it. It would also alleviate some of the performance issues around large frameworks like Rails, though that shouldn't be a great concern at these very initial stages. So, an easy and robust API framework.
- I will reduce the app to just three controllers, from the 6-7 in the current version: users, mailboxes, emails.

The options so far are:

### Laravel


*Pluses* 

+ It's a great framework, with so much built in.
+ It's well-integrated with Vue.
+ It's very easy to deploy, especially with Forge, which I already pay for.

*Minuses*

- Compared to Django, Laravel seems to have an excess of files for even a simple application. I'd prefer a simpler structure.
- I wonder if other languages could be more enjoyable to work in. Although I know Laravel enough to build something today, and would be starting from scratch in another language, it may be worth it in the long term.


### Django


*Pluses* 

+ It's written in Python, which I would ultimately like to learn more than the alternatives.
+ It has an admin panel built in.
+ The Django REST Framework is well-reviewed.
+ I like how simple the structure is: just a handful of files for a basic project.
+ I like that the project can be split into component apps. Something I missed in Laravel, and don't see in Rails.

*Minuses*

- It seems quite unintuitive to learn. I don't look forward to it.


### Rails


*Pluses* 

+ Looks very nice to work in. I can generate something that works very quickly.
+ It has a built-in API mode.
+ Very-well documented.
+ Lots of Gems, big community.
+ Vue support added with Rails 5.1

*Minuses*

- Deployment looks more involved than Laravel.
- The language isn't as versatile as Python.
- May be hard to cuystomise. Though this project is actually quite straightforward.

### Node


*Pluses* 

+ Fast.

*Minuses*

- Not sure what range of existing libraries are available compared to Rails or Django.
- More of a web language at the moment.


## Conclusion

The process of just writing this out makes things clearer. The project in questions boils down to a trivially simple CRUD app. So it won't cost me much to simply try it out in Rails, and see how I like it. I might even decide to try the same thing out in Django. Then, if the grass really isn't greener, I can switch back to Laravel and learn Python separately, for non-web stuff.