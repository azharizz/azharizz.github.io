---
date: 2024-09-17T07:00:00+07:00
# description: ""
# image: ""
lastmod: 2024-09-10
showTableOfContents: false
tags: ["data engineer", "portfolio", "data engineer tips", "data engineer story", "blog", "recruitment"]
title: "The Unwritten Rules of Data Engineering Tools Job Requirements"
type: "post"
---


{{< resize src="/images/A.png" width="720" height="480" alt="A_Post" >}}


# The Tool Overload in Data Engineering

Data engineering can feel like a never-ending buffet of tools like ETL frameworks, data warehouses, orchestration platforms, container services, and more. Some people even joke that data engineers are really “tool operators”. While each tool can simplify a specific task, juggling too many often makes workflows more complex than consolidating around a handful of versatile solutions. There’s no perfect fit toolset, but identifying the handful of platforms that match your daily workload is key to staying efficient and sane.

![Meme Cat](https://media1.tenor.com/m/EZ3AF0Hhw3UAAAAC/cat-holding-head-cat.gif)

# Focusing on What Matters most

One of the most important lessons I’ve learned as a data engineer is this: don’t waste time trying to learn every tool out there. It’s time-consuming and, honestly, easy to forget if you’re not using them regularly. Focus on the ones that drive your day-to-day work and the skills other data engineer or recruiters seek most often (cloud platforms, ETL frameworks, Docker, etc.). Once you’ve mastered one ecosystem, pivoting to a similar one is far easier. For example, if you’re proficient with AWS Redshift, picking up Google BigQuery usually takes just a bit of adaptation. In my experience, transitioning between companies with different data warehouses or cloud providers rarely upends my workflow. New tools often map to the same fundamental patterns. I think it's not hard as much like moving from one software framework to another.

# Meeting The Recruiter Filter: A Tool-Specific Mindset 

Recruiters can sometimes be extremely specific about the tools they’re looking for in a data engineering candidate. Not all of them, but I’ve had interview experiences where the requirement for AWS experience was non-negotiable even if I had strong experience with similar tools like GCP, Azure, or Databricks. While I tried to explain that I could quickly adapt to new tools (as I had in previous roles), that didn’t always help. One way I’ve tried to overcome this is by building side projects using the same stack the company is using, just to check that box.

# The Future: Fewer Tools or Smarter Use?

Will the future of data engineering be flooded with even more tools or will we shift toward consolidation? It’s hard to say. But what’s certain is the rapid rise of AI. Data engineers now play a key role in building infrastructure and platforms that support AI workflows created by data scientists, AI engineers, and others. That’s why it’s more important than ever for data engineers to stay updated on the latest AI-driven technologies. Another trend is building internal tools or data products—like how Netflix built Metacat to reduce dependency on third-party tools. Creating your own tooling might not be common for all data engineers, but it’s a great way to take control of your stack. **One of my job experiences involved creating web-based data products to replace Google Spreadsheets. The goal was to validate data before it was ingested into the data warehouse, since the spreadsheet was filled out by non-technical users outside the data team. Building this tool helped prevent many of the common errors that occurred with spreadsheet-based validation.** 
