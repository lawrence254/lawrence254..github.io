---
layout: post
title: Data Analytics And Global Warming
date: 2018-01-25
description: My First Attempt At Data Analytics. # Add post description (optional)
img: gw.jpg
tags: [Data Analytics,Analytics,Weather,Kenya,,Africa,Gloal Warming,OpenData,Python,Pandas]
author: Lawrence Karanja # Add name author (optional)
---

So today I decided to dive into the deepend of Data Analytics without any 
previous know how of what or how this field of IT/Statistics(Had to cover everyone there) even worked and I have to say 
I'm equally excited,frightened and somewhat disapointed.

Let's get rght into it. I  am really excited at all the possibilities that this field has to offer 
in terms of gaining more insight into the gargantuan amounts of data that we humans are generating every second of everyday. 
Let us get "Techy" for a minute here... In the last 2 years or so we have managed to generate 90% of all the data in the world today,
This translates to a whopping 2.5 quintillion bytes per day(<a href="https://www.domo.com/learn/data-never-sleeps-5">Data Never Sleeps 5.0</a>). 

With all this data we can now be able to drill down and find patterns and information that we didn't know existed before. This is made possible through
tools such as Pandas, Hadoop among others to be mentioned in later posts.

Let's get into what is frightening about all this data that we generate. The problem that I have is that we are generating so much data about ourselves 
but we have no real control over what company A, B or C are allowed to store about us or even how they should use this data. Considering how valuable 
data is nowadays, controlling the data that a company is allowed to use and for what purpose seems paramount but I digress.

So let's get into my first day dealing with and learning about Data Analytics. My mode of learning? YouTube of course, there are a lot of 
materials that teach data analytics using a variety of tools. I happened across this video <a href="https://www.youtube.com/watch?v=POe1cufDWFs">Data Science with Python Pandas by Athena Kan</a> that I felt 
did a great job of introducing the concepts of data analytics. Within the tutorial there are exercises that are used to show these concepts in practise 
and so I decided to learn by following along. The exercise involves going through a global temparature dataset but I decided to remain local so that 
I can gain real insights about where I'm from.

And herein lay my problem, getting the historical temperature dataset for Kenya proved to be almost nightmarish. The first place I looked was <a href="http://www.opendata.go.ke/datasets">Kenya OpenData</a>
but I was dissapointed because nothig was forthcoming. Inspite of this I decided to try and download a random dataset but apparently I have to sign up to ESRI to get access to the datasets(I stand to be corrected).
I decided to hit google and try my luck elsewhere and after a couple of fails I landed at http://sdwebx.worldbank.org/climateportal/index.cfm?page=country_historical_climate&ThisCCode=KEN where I found historical data going back to 1901.
This dataset was very appealing to me since it closely matched the one used in the tutorial and it had enough differences that I learnt a few things on my own.

At first after finishing the tutorial successfully I was very happy since after all I had just completed my first Data Analytics excercise. But after the excitment had died
down I became worried after I did predictions based on the data that I had and realized that as hot as it is currently there's no reprieve anywhere in the near future for temperatures
going down. And that is when the full weight of how serious global warming really is dawned on me. The models may not be 100% accurate but they still paint a very grim picture.

Data analytics has proved to be really good at telling the story behind the mountains of hidden data available, but can it be used to
provide actionable insights that will cut through all the beauracracies and just provide solutions to effectively combat global warming? 
That remains to be seen and I will continue to work towards helping in this regard by learning as much as I can and going through as much data as I can.

The repository for this first attempt at analytics is at https://github.com/lawrence254/KenyaTemp and anyone who has any pointers on how to get more from it can email me.
