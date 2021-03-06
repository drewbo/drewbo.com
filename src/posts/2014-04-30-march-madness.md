---
title: March Madness Ticket Price Analysis
layout: post.html
draft: true
---

I don't want to bury the lede here: this analysis was ultimately a
failure. But I did learn things! Let's walk through the stages of this
analysis and see what lessons I should keep in mind for the next
investigation and try out some new graphing and visualization
techniques.

## Genesis

Scene: workplace cafeteria, the Monday after the first round of NCAA
basketball tournament games... "I thought about buying tickets during
the game but I wasn't sure we we're going to win." "Yeah, I checked
afterwards and prices were so much higher than earlier."

I'll work on my dialogue crafting skills before I try my hand as a
screenwriter but above is a rough paraphrasing of how this idea came
about. Two friends who had attended UVA wanted to go to the upcoming
sweet sixteen game but tickets were out of their price range by the time
the were ready to buy. The question for analysis: For games with
undetermined participants (e.g. super bowl, March Madness, all
tournament finals) how do ticket prices and available number of tickets
vary throughout the time leading up to the game, particularly during the
contests which determine the future participants? My hypothesis was that
ticket prices would rise and availability would fall in real time as
teams' fans became more sure off eventual victory. Critique \#1
(footnote, framed as a lesson "write out your hypothesis"): I should
have written this question out in full before proceeding. Doing so would
have helped me realize two things:

> 1.  The question itself needs some refining
> 2.  My eventual metrics were not going to fully answer this question

The added specificity that I really needed was to clarify what was meant
by "ticket prices". Listed prices? On which market? Sales?

When I went to review my metrics for the first time, I realized I was
only capturing listings (price and quantity) so I couldn't tell (1) if
people were actually buying tickets or if the seller was just removing
the listing or (2) what price people were actually paying (I came up
with a decent proxy in the end)

## Data Sources

Once I had the question (poorly) formed, I needed to find some data.
Secondary markets were going to be better suited for this analysis since
I assumed they would better simulate shifting market conditions and I
could scrape the data from a public website. My first choice was stubhub
but I had some trouble with their api so I switched to seatgeek. I
tested an r script to pull from api queries (using some regex to smooth
over my awkward switch between languages) then set up a simple batch
file in Windows scheduler to have it run every 5 minutes. Code included
in the appendix.

Critique \#2: invest time and effort in finding the most appropriate
source of data. In addition to the errors mentioned above, seat geek
sucks because it isn't stub hub, occasional data gaps

Show r plots Show linked graphs (price, number, probability of winning)

Appendix Code, discuss cron
