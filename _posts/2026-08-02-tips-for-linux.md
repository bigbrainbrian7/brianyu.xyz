---
layout: post
title:  "10 Essential Steps to Win CyberPatriot"
date:   2026-10-02
categories: CyberPatriot
---

CyberPatriot is one of those competitions in which the time you put in is what you get out. As with anything else, there's ways to use your time better, and ways to use it worse. Here, I try to document what's worked best for me.

---

### **PREFACE**
This is not a be-all end-all list. Nor does it apply in every case. But there's typically not many cases worth deviating from it, and its uncommon to hear conflicting advice from other top teams.

#### 1. **BASELINE BASELINE BASELINE**  

CyberPatriot is at its core an incident response competition (at least for the earlier rounds). An attacker has entered your system, messed everything up, and left you in this precarious situation. In any real-world environment, the best thing you can do is roll back or wipe and restart your server. That kind of defeats the purpose of CyberPatriot, though. So what can you do that lets you achieve a similar effect?

Baseline, or in application, compare your infected machine to a clean one. There are a lot of ways to go do this. For Linux, one of the most efficient ways is to compare the MD5 checksums of your system's potentially modified files to their original installation state (read more about it [here](https://manpages.debian.org/unstable/dpkg-dev/deb-md5sums.5.en.html); P.S. there are tools that automate it for you). 

However, that doesn't capture everything. Which packages are installed, services that are running, files that were manually added -- the list goes on. Some strategies to handle that include scripts, mounting another file system and diffing, or manually comparing with a tool like Meld, but I encourage you to find what works for you! Whatever you end up doing, though, always look for an opportunity to baseline. Otherwise, you'll spend your time scouring every single file, having no idea where to look.

#### 2. **VULNERABILITY CATEGORIES** 
Once you create a practice test, you'll start seeing a lot of the gaps between a realistic scenario and a CyberPatriot image. What can test-takers reasonably find? How do you ensure your image contains vulnerabilities that have been seen before? How can you best simulate a CyberPatriot image? Even in real rounds, the test creators are following the same design strategies time and time again.

So what's the only thing they release after a round ends? The vulnerability categories, which reveal that they design the image around them. They follow a similar distribution each time (quite a few in user auditing, application security, etc.). Hence, try to structure your game plan around them, and if you notice one category is lacking mid-competition, then there might be a lot of points to gain there.

#### 3. **RUN THROUGH YOUR CHECKLIST**

First off, if you don't have a checklist, just call it wraps. It's not worth risking forgetting something, no matter how good you think your memory is. Not only does it track your knowledge, it also grounds you to a structured process during the stress of the competition, and keeps your results consistent.

Hopefully, you have a list of vulnerabilities that you've seen before. You want a somewhat structured process to run through them to ensure that you don't miss any of them and forget some "low-hanging fruit". At the end of the day, repetition is king, and trying your checklist on a few different images will ensure you know how it could go wrong and what to do if it does.

#### 4. **LOW-HANGING FRUIT**

Naturally following, once you finish going through your checklist, you might be clueless on what to do next. Time and time again, I've scoured through the system, looking for the most hidden rootkit or an obscure configuration. Every time except one, it's been something extremely simple. 

A majority of the points are very straightforward. If your score is low, don't try looking for complex stuff. Go for the best cost-benefit ratio -- stuff you already know. So before the competition, make sure you know your fundamentals.

#### 5. **TALK TO YOUR PEERS**

Even if your peers happen to be your competitors, talking to them is a great way to share knowledge, a mutually beneficial action. Further, talking about what you know greatly solidifies your own understanding. It's not a zero-sum game.

Although I don't encourage you to share checklists directly (unless you're teammates), discuss your personal strategies, what works for you, and what confuses you. You'll be surprised by how much you never realized, since you've only looked at it from your own perspective.

#### 6. **READ WALKTHROUGHS**

This one's a little bit iffy. You want to save the walkthroughs until you genuinely need them, when you cannot get ANY further in an image. A little advice for general studying: it should almost be your goal to struggle, as that's where you'll learn the most, so don't take the easy route and use ChatGPT or prematurely read write-ups.

However, reading walkthroughs can also be an incredible way to build up your vulnerability list and understand the security mindset. Reading one or two (at the sacrifice of your later learning) might be a good idea to make sure you're staying on the right track.

#### 7. **TAKE SCREENSHOTS**
Know how many points you go, know if you lost points, lets you compare your vulnerability distributions with vulncats (vulnerability categories)

#### 8. **TAKE NOTES**
If you got a vuln and then lost it, but the scoring report doesn't show anything, you might be fried.

#### 9. **TAKE SNAPSHOTS**

Snapshots are your best friend. They let you make checkpoints and confidently try potentially system-breaking changes. If you're not confident (e.g., you don't want to restart your image because of settings that might apply on boot), snapshot, apply, and go from there.

#### 10. **PRACTICE WITH YOUR TEAM**

Grind sessions get boring, and its easy to lose motivation to continue working. Thats why working with your teammates, even if you're learning completely separate topics, is so crucial. Despite the efficiency loss and ease of getting distracted, these types of sessions are what keep you consistent and excited for what you'll accomplish together.

#### **CONCLUSION**
