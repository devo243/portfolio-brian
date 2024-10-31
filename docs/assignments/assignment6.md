---
title: Assignment 6
layout: doc
---

# Assignment 6


## Tasks

| Task | Instructions | Reasoning |
| --- | --- | --- |
| Join/Leave a Community | After checking out a bit of the website, you want to search if there is a community about cats. Thus, try to search and join this community.  | One of the core concepts of the website are communities. Thus, I want to know how easy is to find a community the user likes and become part of it. Can the user tell they joined the community and are able to leave the community too? Does the user stumbles onto anything difficulties while trying to join? |
| Creating a Community | While exploring the website you noticed there is not a community about your favorite series/character. Try to create a community about this character. | In addition to joining a community, user created communities are key to the longetivity of the website. Does the user quickly understands how to create a community? Is it easy or confusing? Are there any errors while trying to create? In the end, I want to know if the interface is understandable and it is a smooth experience. |
| Post Submission | You just stumbled to this new website and you want to share a drawing you made. Submit a post of a drawing of your choice to the website to an appropiate community. | Apart of communities, posts are the main concepts/backbone of the website. Thus, I wanted how the user was able to navigate through the interface and be able to succesfuly submit a post. Are there any difficulties or confusing elements while confusing? Are the instructions clear and easy to follow? Does the interface help with the process of creating a post? |
| Liking | Choose the post you like the most and like it | One of the main features of artBook is the ability to like posts. Thus, I wanted to know if the user is able to find the like button in each post and is able to tell a post has been liked. Was it a difficult/confusing endeavor or relatively straightforward? | 
| Post Deletion | After submitting a post, you notice that you didn't want to share it. Try to delete the post you submitted. | Finally, I wanted to test how error prone was my website through the delete post functionality. How easy is it to delete a post? How hard is it to recover if the user didn't want to delete the post? Are there any confusing obstacles while deleting a post? |

## User Testing

### User Testing #1: Jack

At the start of the user test, I gave the first task of trying to submit a post. At first, Jack was a bit confused about what to do. He first tried to go to a community but there wasn’t any button for submitting a post. After a minute, he figured out he had to create an account and login first, and he was able to access the full website. Thereafter, he was able to find the submit post page, and it was relatively easy for him to post a picture of a cat. However, after submitting the picture he wasn’t sure the post was submitted correctly (he saw the form reset but there weren’t any other indicators), but he was able to find his post on the feed after scrolling a bit. Overall, I think there wasn’t enough feedback for Jack to notice he did the task successfully.

Furthermore, I noticed he tried to post through the community page but was a bit surprised he had to go to a separate page to create a post. I didn’t consider while designing the website, but after doing the test, I see that is a bit janky having to go to a separate page and it would be a smoother experience if he was able to submit straight from the community page. 

After doing the first task, I sent him the next task of creating a community which was relatively straightforward, and he noticed he did it correctly as the UI in the navbar update with the new community. On the other hand, he was a bit annoyed that there was a more obvious alert that the community was created. Hence, I think this feature also suffers from the same problem as the first task. Thereafter, I gave him instructions on liking a post and joining/leaving a community which he had not much problem and everything was expected for him. One thing to note though is that he was expecting to have a page/list with his favorite posts which were not on the website. 

Finally, I gave him the task to delete a post, where a popup appeared to delete the post after clicking a delete button that was at the bottom of the post. There was confusion from him, when the popup didn’t disappear after he pressed the delete button and the wasn’t immediately removed. To check that it was removed, he had to refresh the website which he thought was not ideal. Unfortunately, this behavior was a bug I didn’t notice which affected the testing. In the end, he liked the website, but he mentioned that there could be some improvements in the flow and clarity.

### User Testing #2: Jan

During this testing session, Jan had an easier time navigating the site than Jack. After giving him the first task, he assumed he had to login first, so he created an account and was able to access all the features of the website. After that it was relatively easy for him to create a post. However, he was confused if he had submitted his post correctly, and so he went to the home feed and tried to search for it. After some scrolling, he was able to find it, but it was hard to notice the post at first. I expected that creating a post would be straightforward, but it wasn’t aware of the feedback issues the website had.
Still, we continued to test, and I gave him the second task, which was also straightforward for him to do. While filling in the form, he gave an image link that wasn’t valid, but I expected this by giving a preview for the icon, which he then recognized wasn’t a correct link and was able to correct it. However, he was annoyed there wasn’t a popup or something to say that he created the community correctly.
After that, we did the tasks for liking and joining/leaving a community which he had no problem with and was able to determine what to do. Finally, we got to the final task, which was deleting a post, which was very confusing for him as the popup for deleting the post didn’t work as he expected to do. He was expecting the popup to disappear and the post to disappear which did not happen. I was also expecting that behavior which I explained before was a bug I didn’t notice.
In the end, he liked the design of the website, but he’ll appreciate it if there were popups/alerts that an action was done successfully, which I didn’t take into account during the development of the website in A5.

## Opportunities for Improvements

### Better Popups and a better feedback system

- Type/Severity: Linguistic/Moderate

- Description: Currently, the website doesn't have a great feedback system to notice the user that an action was done succesfully or incorrectly. Thus, in the future, I'll create like popups or some reactive component on the website were something changes to aler the user of a correct or incorrect action.

### Flow and Navigation between pages and submissions

- Type/Severity: Linguistic/Moderate

- Description: Another issue I noticed while testing, it was that after creating a post/community the page would remain in the form page and not into the corresponding post/community page which made the experience/flow of the website very stuttering and made the user do more actions that they needed to do. So as a possible solution, is to change the page accordingly to the post or community page the user was creating. Anothe solution is to add the functionality of a page to another page. For example, creating a post can be added to each community page.

### Liking

- Type/Severity: Conceptual/Major

- Description: While the users were able to like a post easily, it was not clear what it meant for a post to be liked, which also affects the feauting concept. Hence, some solutions are creating a new page were the user can access their liked posts, and adding some clarification on how liking affects which post featured, and maybe also adding a like counter for each post.