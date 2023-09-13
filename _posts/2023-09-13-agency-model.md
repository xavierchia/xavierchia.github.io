---
title: The mathematical reason why agencies get stuck at $50k MRR
published: true
layout: post
permalink: agency-model
excerpt:  Can we just keep adding more clients until at 150 clients we hit $300k MRR?
image: /images/default.png
categories: entrepreneurship
---

Every agency gets stuck around $50k in monthly revenue. Hardly anyone ever breaks through that barrier and reaches that next level where the agency generates reliably $300k+ in monthly revenue.

There might be a few months were revenue goes up a bit. But then it quickly goes back down again.

I've been fascinated by this pattern for a while now. And I think I've finally figured out why this happens.

Let's dive in.

For simplicity, let's assume our agency only offers one package for $2k/month.

So with 25 clients, we're at $50k MRR.

Now why can't we just keep adding more clients until at 150 clients we're at $300k MRR?

Two reasons: churn and owner capacity.

Let's start with churn.

## Churn

No matter how good your service delivery, your agency will experience churn. Clients will leave for the most random reasons. Co-founders will break up. Companies will go out of business. People will get fired. And so on.

So let's assume our agency has a baseline churn rate of 8% per month, assume service delivery is absolutely flawless. That means that every month 8% of our clients will leave.

It's important to note that churn rate is a percentage of the total number of clients. So if we have 25 clients, 8% churn means that, mathematically, 2 clients will leave every month.

But if we have 150 clients, 8% churn means that 12 clients will leave every month.

This means that the bigger your agency grows, the more new clients you have to acquire every month just to stay at the same revenue level.

So when you start, you can grow quite comfortably adding a few new clients every month. However, after a while you will inevitably hit a plateau simply because the number of new clients you are able to acquire every month and the number of clients that leave every month will be roughly the same.

Let's assume you're able to acquire 2 new clients every month. Since once you hit 25 clients, meaning $50k MRR, 2 clients will leave every month, you will hit a plateau at $50k MRR.

{:.centered}
![](/images/client_plateau.png)

I'm oversimplifying a lot here obviously. So let's have a look at another key factor that prevents agencies from growing past $50k MRR: owner capacity.

## Owner Capacity

When you start your agency, you're doing everything yourself. This is only possible up to a certain point. At some point you will have to hire people to help you.

Typically, even with the most amazing systems in place, a single person is only able to handle service delivery for 10-20 clients. Beyond this point, it becomes impossible to keep all the balls in the air. Call it the [Dunbar's number](https://en.wikipedia.org/wiki/Dunbar%27s_number) of service delivery.

So you'll have to hire people to help you.

Again let's keep things as simple as possible by assuming you're able to hire the most amazing people.

However, one lesson every business owner has to learn at some point is that no one ever cares about your business as much as you do. No one will ever work as hard as you do. No one will ever be as invested as you are.

So as soon as you have other people take over service delivery, you will inevitably experience a drop in quality. And this will lead to more churn.

And not only that. The more clients you onboard, the less time you as the owner will have to spend with each client. 

Meaning, churn rate grows as a function of the amount of your time you're able to spend thinking about each client.

Let's assume you spend 50% of your time working *on* the business and 50% working *in* the business and work 60 hours per week.

So with 10 clients, you will still be able to dedicate 3 hours per week to each client. But with 20 clients, you will only be able to dedicate 1.5 hours per week to each client. 

And once you hit 50 clients, you will only be able to dedicate around 30 minutes per week to each client. This is hardly enough to stay on top of the most basic facts.

Eventually you will of course no longer be involved in service delivery at all.

Churn will approach a local maximum of, say, 15% per month. Meaning that every month 15% of your clients will leave.

We can use the following formula to illustrate how churn rate grows as a function of the amount of time you're able to spend thinking about each client:

```
churn =  0.08 + 0.07 * (1 - 1/number_of_clients)
```

We start at 8% churn when you're able to spend 100% of your time thinking about each client. And then we add some additional churn as a function of the amount of time you're able to spend thinking about each client. Eventually we hit the local maximum of 15% churn.

{:.centered}
![](/images/churn_growth.png)

If we now put everything together, we can see that the number of new clients we have to acquire every month just to stay at the same revenue level grows quite quickly as we add more clients.

So even if we're able to acquire 2 new clients every month, we would now hit a plateau already at around $30k MRR. This happens because at around 15 clients, we're now losing 2 clients every month since the churn rate has grown at this point to 14% and 15*14% = 2.

{:.centered}
![](/images/increased_churn.png)

In practice this effect is usually not as pronounced. More clients also means more referrals, for example, so the number of clients you're able to acquire every month will grow as well.

Nevertheless, no matter how you look at it, your agency will inevitably hit a plateau at some point. And typically it will be around $20k-$60k MRR.

## The Takeaway

The fundamental lessons to take away here is that you'll need a radically different approach to hit through that omnious $50k MRR barrier.

More of the same will not cut it. Slow and steady growth will not cut it. You'll need a completely different approach.

You might be able to hustle a bit more on the acquisition side, improve your conversion rate by getting better case studies, and so on. But even if you manage to acquire 50% more clients every month, you'll still be stuck at the same level.

Let's do some quick napkin math again.

How many clients would we need to acquire in our simplified model to get to $300k MRR?

Well, we would need to acquire and retain 150 clients. At since point, churn rate is 15% per month. 

So we would need to acquire 150 * 15% = 22.5 new clients every month just to stay at this revenue level.

That's a 10x increase in the number of clients we need to acquire every month compared ot the 2 new clients we needed to acquire every month to get to $50k MRR.

It is very unlikely that you can 10x your acquisition efforts without a complete overhaul of your approach.

{:.centered}
![](/images/growth_bw.png)
{:.centered}
![](/images/plateau_table.png)