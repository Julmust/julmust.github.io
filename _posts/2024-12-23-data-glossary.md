---
title: "Data Glossary - Language matters"
date: 2024-12-23
author: Julmust
---
I recently switched jobs, from my old consulting gig to a cyber security start-up/scale-up named [Eye Security](https://www.eye.security/). Starting any new job is always a mental challenge but when you're entering a company just exiting the start-up phase, the mental strain is even higher. There's a lot of standardisation needing to be done and a lot of people needing to be convinced that for the company to scale the standardisation is needed. But don't get me wrong, it's rewarding work. Work I enjoy. One thing I'm currently working on that, in my opinion, is often overlooked or not talked about is implementing a data glossary.

In the eyes of many data engineers, a data glossary isn't needed. We'll just implement a data dictionary and the business can use that. But that's not true. Yes, there's an overlap between the two but they are far from the same. And both are needed. Let's start with the basics: what is a data glossary?

## Data Glossary? Never heard of her!
If you want the TL;DR: in your data glossary you **define the terminology the organisation uses**. It puts everyone on the same page.

If I'm to make an analogy, the data glossary is the data warehouse for your business terms. A single source of truth that the business is expected to abide by in all internal communication, reports, and dashboards. What does "Customer", "Annual recurring revenue", and "Subscription start date" actually mean? It might seem straight forward but believe me when I say it's not. These terms can have wildly different meanings to different business users.

By defining all these terms in a publically available location you'll notice that after an inital period of resistance (re-learning part of your vocabulary is hard) communication flows much more freely between business users. Not just that, all of a sudden your data team doesn't have to do guess work on what the business users mean when they ask for a report on "the ARR growth over the latest period".

## How does that differ from a data dictionary?
"Well doesn't a data dictionary cover all these things?" I hear you say. No it doesn't. Or rather: no, it *shouldn't*. A data dictionary contains a multitude of data that business users a) don't need and b) gets overwhelmed by. That doesn't mean they're "stupid" or that they don't want to learn the technical details but just as with any good report or dashboard the data presented should be only the data the viewer needs.

In a data dictionary you can read about the tests that runs against the table. What types the different fields are. Where they originated. If the field is a primary key. A single search can also generate multiple results as the data propagates through your platform. Business users does not need that information. They need to know "what does this term mean?" or, at most, "how is this field calculated?". **Reducing cognitive load should always be the goal.**

Here's a table that nicely reflects the differences between a data glossary and a data dictionary:
{:refdef: style="text-align: center; width: 70%; margin-left: auto; margin-right: auto"}
![](/assets/img/data-glossary-comparison.jpg)
{: refdef}

## Where do I start?
Data glossaries can be as simple, or as complicated, as you need them to be. A good starting point is a good page on a tool like Confluence. Set up a table, refer business users to that. Act as an information collector and update it. Or even better, have them update it for you.

This works for a while but as you grow that page is going to be harder and harder to find. That's why I'm, at Eye Security, planning to try [DataHub](https://datahubproject.io/). And here's where I'll dissapoint you. I don't know how good DataHub is right. But I'll report back on my findings once I do.
