---
description: Create Training Courses for Labeling Datasets
---

# Getting Started with UDT Courses

{% embed url="https://www.youtube.com/watch?v=2XXENmAIyzE&feature=emb\_title" caption="This video has everything you need to know!" %}

## Creating a Course

{% hint style="warning" %}
You'll want to have a dataset before you begin! No labels are needed.
{% endhint %}

You can create UDT courses online in a couple easy steps. First navigate to [universaldatatool.com/courses](https://universaldatatool.com/courses), then click "Create a Course".

![Create a Course](../.gitbook/assets/image%20%287%29.png)

Now you just need to upload your dataset. You can drag and drop or select your dataset here. The samples will be used to construct tests!

![Upload the Dataset](../.gitbook/assets/image%20%288%29.png)

You should now be inside the course editor!

## Editing a Course

Every course has an Instructor URL and a Student URL. Your Instructor URL has a secret code in it that allows you to come back, view passing students and edit the course. So don't lose it! After you create a course it should be in your address bar.

{% hint style="info" %}
Here's an example of an Instructor URL:

[https://universaldatatool.com/courses/course/8f55e988-e2ba-4411-8540-dcd5fd96592d/edit?edit\_key=4eb518683bab1898e1683c8d254d201f](https://universaldatatool.com/courses/course/8f55e988-e2ba-4411-8540-dcd5fd96592d/edit?edit_key=4eb518683bab1898e1683c8d254d201f)

And here's an example of a Student URL:

[https://universaldatatool.com/courses/course/8f55e988-e2ba-4411-8540-dcd5fd96592d](https://universaldatatool.com/courses/course/8f55e988-e2ba-4411-8540-dcd5fd96592d)

See how the Instructor URL is longer and has an "edit\_key"?
{% endhint %}

We can now add sections, tests, exercises, quizzes and explanations to create a full training course.

### Creating a Course Item

Anytime you see this icon, you can create a new course item.

![Create a new course item](../.gitbook/assets/image%20%2811%29.png)

![After clicking the Icon, you can select a new item to create](../.gitbook/assets/image%20%281%29.png)

### Markdown Descriptions

It's just markdown! Put whatever you want inside to explain the motivation of your dataset or specific details. Maybe start with a general overview, then do a deep dive in a second section.

### Question / Quizzes

Quizzes are used to make sure that your labelers read the preceding paragraph.

![A quiz quickly tests the knowledge of your labelers.](../.gitbook/assets/image%20%283%29.png)

### Tests / Exercises

**Tests and exercises are the bread and butter of a UDT course.** They make sure your labelers actually know how to label with real examples. 

#### 1. Select the samples

![Most people just pick samples randomly :shrug:](../.gitbook/assets/image%20%286%29.png)

#### 2. Edit the Solution

Here you can add solutions to the dataset. **If your dataset already has labels, they'll automatically be imported.** Your labelers will be tested on these solutions!

![Label some data!](../.gitbook/assets/image%20%285%29.png)

#### 3. Configure the Test

Configure your test with instructions, make it a practice exercise etc.

![](../.gitbook/assets/image%20%2810%29.png)

## Sharing a Course with Labelers

Share your course using the "Go to Course" button at the top of the page. That will take you to a page that you can send to all of your labelers.

![](../.gitbook/assets/image%20%282%29.png)

After a student successfully completes the course, they'll be prompted to enter their email. Their email will now appear in the "Passing Students" dialog.

![View the passing students](../.gitbook/assets/image.png)

## Running On-Premise

Check out the [github repository for on-premise instructions](https://github.com/UniversalDataTool/courseware)!



