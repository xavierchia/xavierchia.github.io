---
title: ⭐️ The simple system I’m using to stay in touch with hundreds of people 
published: true
layout: post
permalink: stay-in-touch
excerpt: Staying in touch with people is one of these asymmetric habits that require little effort, time and resources but has an unlimited upside. 
image: /images/default.jpg
categories: personal-brand-building


---

Staying in touch with people is one of these asymmetric habits that require little effort, time and resources but has an unlimited upside. It’s the easiest and most effective way to make your life more serendipitous. 

Okay enough of that. Since you clicked on the headline I will assume you understand why it makes sense to keep in touch with people. 

Unfortunately, for most people (me included) this isn’t something that happens naturally. 

So unless you have a solid system, chances are high that you won’t reach out to people regularly and miss out on a ton of fun and opportunities. 

Derek Sivers has a cool [system](https://sive.rs/hundreds). He divides all people he wants to stay in touch with into four categories: A, B, C, D:

- people on the A list are contacted every three weeks,
- people on the B list every two months,
- people on the C list every six,
- and people on the D list once a year.

While this system sounds deceptively simple, like most people, I wasn’t really able to make it work. 

You obviously need some technology but all CRMs (and PRMs) I tried felt overkill. Derek ended up [programming](https://sive.rs/dbt) his own database software which he however never shared publicly.

Also:

- What exactly do you write? Derek’s advice is rather vague: “Just find out how they’re doing. See if you can help them in any way.”
- What about people you never interacted with? How do they enter the system?

Now I recently finally figured out a way to make Derek’s system work. Obviously, this is why I’m writing this post. 

Let’s get into it. It’s free, fun, and simple.

## The Setup

I’m using one Airtable base with two tables. 

The first one is titled **Established Contacts**. As the name suggests it’s for everyone I already interacted with at some point and want to keep in touch with.

{:.centered}
![](/images/CleanShot 2022-01-26 at 10.54.48@2x.png){: width="800px" }



I like to keep things as simple as possible, so there are only 7 columns: **Name**, **Contact Info**, **Notes**, **Category**, **Last Contact**, **Next Contact,** **Trigger Reminder**.

The first three columns are simple text columns while the third one, **Category**, is a single select column (”A”, “B”, “C”, “D”). 

The **Next Contact** column is calculated as a function of the values in the **Category** and **Last** **Contact** columns.

{:.centered}
![](/images/CleanShot 2022-01-26 at 11.03.27@2x.png){: width="300px" }

Here's the formula in case you want to copy it:

```html
IF(
    Category="D",
        DATEADD({Last Contact},12,'month'),
        IF(Category="C",
            DATEADD({Last Contact},6,'month'),
            IF(Category="B",
                DATEADD({Last Contact},2,'month'),
                IF(Category="A",
                DATEADD({Last Contact},3,'weeks'))
              )
           )
    )
```

The values (e.g. contacts in the C category are contacted every 6 months) are exactly the same that Derek Sivers uses.

The **Trigger Reminder** column is then populated by comparing the **Next Contact** column with today’s date.

{:.centered}
![](/images/CleanShot 2022-01-26 at 11.03.17@2x.png){: width="300px" }

Here's the formula:

```html
IF(  
    AND(    
        {Next Contact},
        NOW() >= {Next Contact}  
        ), 
    "Trigger Reminder"
   )
```

The second table, titled **Potential New Contacts** is even simpler. In it I store information on cool people I haven’t talked to so far. 

{:.centered}
![](/images/CleanShot 2022-01-26 at 10.56.25@2x.png){: width="800px" }

Whenever I come across a cool project, interesting piece of content or I get a referral, I add the person in question to this table.

In the **Name** column, I usually save a link to their website, project, or Twitter account. The **Notes** column is used to store some information about why I think this person is interesting. 

For example, one entry might read: “*He publishes incredible posts on his blog: [https://jon.bo/posts/](https://jon.bo/posts/)*”. 

The remaining two columns in this table **Reach Out** and **When to Reach Out** are populated automatically. 

So next, we’re going to talk about automations, since this is where all the magic happens.

## Automations

Let’s start at the end.

Every morning I’m getting a short email that says:

*Hey,*

*You should today reach out to ____. Here are the notes you took: ____*

*And here's who you should keep in touch with: ______*

I already check my inbox every day so getting a reminder like this is perfect for me. Checking a database or some website would definitely add too much friction. 

The email tells me exactly what to do. Then I do it. 

Now, how is this email generated?

With a simple Airtable automation!

To create an Airtable automation, click on the **Automations** button in the upper right corner.

{:.centered}
![](/images/CleanShot 2022-01-26 at 11.12.16@2x.png){: width="800px" }

Here’s what my complete automation looks like. 

{:.centered}
![](/images/CleanShot 2022-01-26 at 14.52.18@2x.png){: width="800px" }


In words:

- Every day at 6am in the morning the automation is started.
- The first action is to find all records in the **Established Contacts** table where the **Trigger Reminder** column contains the word “Trigger Reminder”. (Remember that this column is populated through a formula that compares today’s date to the **Next Contact** column.)
- The second action is a little custom script that automatically picks one random entry from the **Potential New Contacts** table and then updates the **Reach Out** and **When to Reach Out**  fields for this entry. Of course, the script only picks from the list of entries that haven’t been picked before. This is why the **Reach Out** column is updated. Only records where the **Reach Out** column is not equal to “Yes” are used. Moreover, the script returns the record it picked randomly so I can use this information in the next step.
- The final step is that all the information from the previous steps is put into an email which is then sent to my email address. This includes the one entry from the **Potential New Contacts** table that was picked randomly and the list of people from the **Established Contacts** table that are due for a new message.

Now that’s it!

Every morning I’m getting an email that tells me who I should reach out to today. After I sent the messages, I open Airtable and update the **Last Contact** column to today’s date. In total, this process takes maybe 15 minutes per day. 

You can find all further technical details below but first I want to take a brief moment to talk about something more important. 

What kind of message do you actually send to people?


## What to Write

Here’s what I do. 

I typically spend a few minutes researching what they’ve been up to recently.

I check their social profiles, personal websites, and read or watch any content they published that I missed. 

Then I share a few thoughts or questions. 

Most importantly, I always send the kind of messages I’d like to receive. They’re short, genuine, and (ideally) helpful. I never try to sell anything and there’s no agenda other than to keep in touch.

Sometimes I just share a related article or book I think they might find interesting and sometimes I offer specific help or advice with a problem they’re facing right now. 

Of course, not everyone publishes content or updates regularly. In that case, I usually just ask what they've been up to lately.

You’d be surprised how many people are really happy to get these kinds of messages and they often spark all kinds of deeper conversations. 

Okay, like I said, more technical details below. And in any case, let me know what you think and if you have any suggestions on how I can improve my system.

Thanks,

Jakob

## Technical Details

This is what the trigger looks like:


![](/images/CleanShot 2022-01-26 at 15.00.33@2x.png){: width="300px" }

This is what the first action looks like:

{:.centered}
![](/images/CleanShot 2022-01-26 at 14.53.21@2x.png){: width="300px" }

And this is the second action:

{:.centered}
![](/images/CleanShot 2022-01-26 at 14.53.30@2x.png){: width="300px" }

Moreover, this is the code I’m using to pick a random entry and the update fields accordingly:

```html
let table = base.getTable("Potential New Contacts");
let queryResult = await table.selectRecordsAsync();
var items = queryResult.records
let todo_items = [];
for (let i = 0; i < items.length; i++) {
    var record = items[i]
    if (record.getCellValue("Reach Out") != "Yes") {
        todo_items.push(record);
    }
}
console.log(todo_items.length);
let rightNow = new Date();

var random_record = todo_items[todo_items.length * Math.random() | 0];
await table.updateRecordAsync(random_record.id, {
    "Reach Out" : "Yes",
    "When to Reach Out" : rightNow
})
output.set("Name",random_record.getCellValue("Name"))
output.set("Notes",random_record.getCellValue("Notes"))
```

Last but not least, this is the action I’m using to compile and send the daily email.

{:.centered}
![](/images/CleanShot 2022-01-26 at 14.53.50@2x.png){: width="300px" }