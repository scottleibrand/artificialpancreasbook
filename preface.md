---
description: My Story And The Evolution Of DIY Closed Looping
---

# Preface

The room was dark and still, but I couldn’t move a muscle. I had woken up for some reason, but I realized I could not move. Had someone broken into my apartment? Was I paralyzed with instinctual fear? No, all was quiet and there was no movement. Instead, the realization dawned that my blood sugar was probably low. I managed to turn my head slightly to the left, and somehow could see the screen on the receiver of my CGM. It said the worst thing it could possibly say: “LOW”. That meant my blood glucose \(BG\) levels were below 40 mg/dL, and likely dropping.

I could also see the juice box sitting right there on the bedside table. I needed to grab it, take the straw off and open the wrapper, and manage to get the straw in and take a drink. Four or five simple steps. I had done so thousands of times in my decade of living with type 1 diabetes. So why wasn’t I doing it now? Why couldn’t I move? Why was I paralyzed? If I didn’t drink the juice, my blood sugar might keep dropping and I could slip into a coma and die. Since I lived alone, it might take days for someone to notice that I had not shown up to the office or was not responding online. I was going to die, and this was what it felt like to be afraid, alone, and in the dark unable to move.

And then I woke up.

Thankfully, that was “just” a terrible nightmare. However, it’s the nightmare that changed my life - and I may even be bold enough to say that it ultimately changed the lives of thousands of other people with type 1 diabetes, too.

\*\*\*\*

The day after I had that terrible nightmare, I remember staying in my office at work until around 9pm. I had called my parents, who were in Alabama, from my office in Seattle. I was crying. I was afraid to go home, because I didn’t want to go to sleep. I was afraid of what might happen if that nightmare became reality. Because unfortunately, it could happen. Although it is not very common, and it’s hard to find the numbers on just how common it is \(because it’s hard to know what causes it\), the phenomenon known as “dead in bed” from type 1 diabetes can happen. There’s a variety of reasons it may happen, which I’ll describe later. But around March 2013, it didn’t matter to me how unlikely it was to happen. It felt very, very likely to happen and very real.

Some of the solutions at the time would have involved getting a roommate. I didn’t want a roommate. I had lived with roommates in the dorm throughout college, and I was thrilled to have moved to Seattle for work, and be living by myself. Getting a roommate felt like a step backward.

The best thing I could do at the time was the solution I had already been using for years. Every night before bed, I would text my mom and tell her when I expected to be up or get going for the day, such as when my first meeting was. Every morning, my mom \(who was in a time zone two hours ahead of me\), would text me around the time I was planning to get up. The plan was that if I didn’t respond after a while, she would call me. There were numerous reasons I may not respond right away, such as if I had gone in to work early or got wrapped up in a spontaneous meeting. Or, in the worst case, that I hadn’t woken up to my phone alarm because my blood sugar was too low. Ideally, I would answer the phone or text her back and let her know I was awake, ok, and fine. But the plan was that if she couldn’t reach me by phone, she would then call the apartment manager of my building and have them come check on me. If they couldn’t get me to come to the door, they’d call 911.

Thankfully, up to that point \(and even until now\), 911 never had to be called. It seemed, and seems, so silly to need all of these backup plans when there’s an even more simple solution: making the alarms on my continuous glucose monitor \(CGM\) alarm louder.

\*\*\*\*

To just about anyone who’s not living with a chronic disease, this problem seems like it’s easily solvable. Change the alarm on the CGM. Allow users to configure the alarm sound, so they don’t get used to always hearing the same sound, and their brain will be less likely to ignore the sound.

However, changing a medical device is a lot harder than you might think. Devices are designed many years before they actually come to market. Making a change to a device often takes half a decade or longer. So despite me speaking to all of the CGM manufacturers on the market many times, and begging them - in person, on the phone, and by email - to enable users to make the alarms louder... it didn’t do any good.

To be fair, they did respond. But the responses from the companies were frustrating. I was told that they were working on it and it would be out in the future. \(Although it never did come out on a hardware-based device\). I was told that it wasn’t a problem for most people. \(At the time of writing, there are 45,000 search results on Google when one types in “louder CGM alarm”, with a variety of hacks and tips suggested . Even in 2013, I definitely wasn’t the only one with this concern.\)

It didn’t feel like it was enough. I was frustrated by being told to wait. I had the problem then, that day, that night, and every night for the rest of my life. And what could I do about it? Nothing. I was “just” the patient and the “user” or “consumer” of the device. I had no ability to change medical devices to better suit my needs.

\*\*\*\*

In April 2013, I met and began dating Scott Leibrand. On our first date, when we began talking about type 1 diabetes, he had asked me why my CGM didn’t talk to my insulin pump. Coming from a tech background, he \(and everyone else who doesn’t have chronic illnesses and hasn’t become used to the weird status quo of healthcare technology being antiquated, and devices not being interoperable with each other\) didn’t think that made very much sense. But again, we couldn’t do anything about it. I told him about my nightmare, and how I had an idea for a louder alarm system that would send alerts to my phone, instead of relying on the physical CGM device. It would be designed to be loud, and with varying types of sounds, to wake me up. But if I didn’t wake up, it would then alarm my mom or someone else and give them an earlier warning to call and check on me.

However, there was one flaw with this idea: it required accessing the CGM data in real time. And at the time, there was no real-time data sharing from any CGM device. In fact, I couldn’t even get my own data off my physical CGM. The FDA- approved software was only approved for PC computers - and I had a Mac. So not only was real-time data a pipe dream, but so was my own review of my data from my own device. It was frustrating, to say the least.

\*\*\*\*

Fast forward to a few months later. I had been active on Twitter for years, and somehow saw a tweet surface by a gentleman named John Costik. It showed a picture of how he was somehow managing to pull the CGM data off the receiver - and in real time! He was then sending it to the cloud, where he could view his son’s data remotely. I was thrilled - if we could manage to do the same thing, we could then build my louder alarm system!

I sent that tweet to Scott, who suggested that we actually reach out to John and ask him to share his code, so we didn’t have to recreate the wheel. This was a new idea to me - my professional background is in communications, so I was unfamiliar with the concepts of “open source” and people freely sharing their code to help one another. Scott messaged John, and John said yes, he would share the code.

At the time, pulling data off the CGM still required a PC, so I borrowed an old, clunky PC laptop from Scott to sit under my bedside table. We set up John’s code so that when I plugged in my CGM to the laptop, it would pull the data off the receiver. There was a script that would tell it to pull the data off every 5 minutes, which is when a new BG data point would come in. Scott and I designed it to take the new data and add it to a file in the Dropbox folder on the computer. It would then be uploaded to the cloud, and downloaded to a virtual Linux server we set up for the purpose. From there, we designed a simple series of rules to tell the computer when to alarm me. We also got a simple $5 alarm app called “Pushover”, which would receive the commands and send the alarms to my phone.

![Showing how DIYPS works: automated BG uploads to the cloud, coupled with inputs about carb &amp; insulin, enables push alerts and predictions to the devices of my choice.](.gitbook/assets/diyps_example.jpg)

It worked fantastically, even on the first night. I got several alarms telling me that my blood glucose level was going high, or low. And I actually heard the alarms! It was an incredible relief to know that I had this backup system in place.

As I had envisioned months ago, I also wanted to build a tiered alarm system, in case I still somehow managed to sleep through the alarms while I was deeply sleeping, or if my BG was exceptionally low. Scott and I put together a very simple webpage to display the data. We also added simple web buttons. When I woke up to an alarm, I would open my phone and press the “snooze” button. This would snooze the system. However, if I didn’t respond to my alarm in a period of time, and if my blood glucose was a certain level, it would then alarm the next person. \(At this point, I decided to have Scott be the recipient of the next level of alarms, instead of my mom, since he was co-designing the system, and also because he lived 20 miles away.\)

The tiered alarm system worked well, too. A few days after we created it, Scott got alarmed, woke up, and called me. I woke up to his phone call even though I had slept through the Pushover alarm. I was able to drink a juice box and go back to bed safely.

After that, we decided that we should add more buttons to the system. Instead of just hitting a “snooze” alarm, we designed and inserted a few buttons for the key actions I usually was taking: eating carbs \(i.e. drinking a juice box or eating a snack\), taking insulin \(if my BG was high\), or setting a short, temporary basal rate of 0 for 30 minutes \(effectively reducing my insulin temporarily to ward off a future dip in BGs\). That way, Scott would be able to see what I did, and not just that I was awake.

I became an exceptionally well-trained guinea pig \(in my own words\), pressing a button every time I ate something or adjusted my insulin delivery. We realized that, in addition to real-time CGM data, it would be valuable to combine all of the manual inputs along with the CGM data in order to forecast into the future what was likely to happen. This meant that I could get predictive alarms and alerts - instead of just being reactive to having already gone low or high.

We used the publicly available data on insulin activity curves to simulate the predicted insulin activity for correction boluses to bring down high blood sugar. But we had also noticed that withholding normal basal insulin caused blood sugar to rise, so we decided to track net insulin activity to model this insulin reduction. This means that you could actually have “negative” insulin activity, compared to your normal baseline levels of insulin activity from your basal rates. Having “negative” insulin- on-board \(IOB\) meant that there would be the opposite effect of positive insulin on board: blood sugar would rise from having less insulin than usual. This is helpful because you can’t remove

insulin after it’s been injected or infused into your body. However, you can reduce your baseline amount of insulin to help compensate for insulin you’ve already received, and help prevent blood sugar from dropping \(as\) low in the near future.

This was a huge step forward. Within a few months, we had evolved from a simple, “louder alarm system” to essentially having built an algorithm and an “open loop system” that suggested insulin dosing adjustments and carb corrections. We didn’t know it at the time, but this was the precursor to the first open source closed loop algorithm that would later be known as OpenAPS.

\*\*\*\*

We jokingly called this system “DIYPS”, which stood for the “Do- It-Yourself Pancreas System”. And it was life-changing.

I no longer feared going to sleep at night. If I was predicted to go low or high, or was actually low or high, it would alarm me. If I didn’t wake up, it alarmed Scott, and he would call me. And it didn’t just work overnight anymore, either.

Over the few months that we were creating DIYPS and were using it at night by my bed, Kevin Lee and others used John’s code as well. Kevin in particular spent a lot of time making an Android-based uploader, so that you could have a mobile uploader. This enabled me to plug my CGM receiver into a small Android phone, and use DIYPS throughout the day. It helped immensely during the day, too.

One day I had eaten lunch, taken insulin, and went to my next meeting. However, I found out that the meeting had been

moved to another campus - about a mile away. I had to walk, quickly, to make it to the meeting. My insulin from lunch started to take effect even more quickly, due to the exercise. DIYPS pushed an alert to me in the middle of my hurried walk, and I drank a juice along the way. As a result, I didn’t have a nasty low BG when I arrived at my meeting.

I was enamored. And I had a feeling that this type of tool could help other people too. I began talking about it online & sharing with other people. Scott and I were invited to participate in DiabetesMine’s D-Data Exchange in June 2014. This event was notable for us for two key reasons.

First, we got to have a table during the “demo” portion, and talk to people about DIYPS. I was excited to share with other people what we had done, how it was working for us, and our ideas to safely share it with others. We had used John’s code to get data off the CGM, which is how I learned about open source. I wanted to make DIYPS open source, too.

However, during the demo discussions, a few people came up and were asking us about DIYPS. How did it work? We were making dosing recommendations off a CGM? Did we know that the CGM was not designed for that? As we answered all of these questions, we found out that these were individuals from the FDA \(the U.S. regulatory agency with oversight for medical devices\). The end of the conversation involved a strong recommendation to not share or distribute the code for DIYPS, because among other reasons, it was making dosing recommendations from a CGM, which wasn’t yet approved for that. And regardless, they considered sharing code to be distributing medical devices, which would be regulated by the FDA.

Gulp. Sharing code on the internet was seen as distributing a medical device? That didn’t make sense to us, but we respected \(and were scared by\) the input. After all, we were two individuals who developed something that worked for me. We didn’t want to get sued, or have a US Marshall come and kick down my door, because we shared our code online.

But the other reason that D-Data 2014 was notable was meeting the gentleman with the demo table to our left: Ben West. Ben was showing off his work that he had spent years on, figuring out how to reverse engineer and evaluate the communications from an insulin pump. We didn’t know it at that very moment, but his work was and is pivotal in the movement of open source closed loop insulin delivery.

We walked away from D-Data re-evaluating how we would be able to share DIYPS with other people. At the very least, we knew we could talk about the concept, even if we didn’t share the code of DIYPS itself. I could raise awareness for the problem of not-loud-enough CGM alarms and the lack of customization.

\*\*\*\*

Over the next few months, we talked with more people about DIYPS, and we also learned more about Ben’s work. One day - we can’t remember exactly when - a collective lightbulb went off. Ben’s work included not just the ability to read from the insulin pump, but he had also discovered the commands to talk and “write” to the insulin pump. Those commands included being able to set temporary basal rates on the pump remotely, using the Carelink USB stick \(designed to read data from the pump\) and a computer. What if we used a computer holding our DIYPS algorithm, and translated the “recommendations” into commands, and sent that to the pump? We could close the loop?

We could close the loop. 

\*\*\*\*

This was late fall in 2014. We had a chance to present DIYPS more formally at the fall D-Data Exchange in November. We talked about DIYPS and what we had learned from it, and what we wanted to do next. We said that we thought we could close the loop, and that we would try to do so.

We joked about setting a deadline for August 2015 for closing the loop. Why then? Well, Scott and I had gotten engaged, and would be getting married in August 2015. That meant he would be married to me - and all my CGM alarms! So by the time we got married & moved in together, Scott was very invested in figuring out more diabetes automation, because he knew he was the lighter sleeper, and therefore the one likely to wake up to alarms!

I always mention our “goal” timeline because I’m blown away with how fast we actually managed to close the loop. Granted, we had already developed the algorithm \(inside DIYPS\), and I had spent a year testing, tweaking and improving it. Ben had spent years figuring out the pump communications. But within three weeks, Ben, Scott, and I had managed to put together a combination of systems where the DIYPS algorithm would output recommendations that were sent as commands that the radio stick would send to the pump. The data would be read off of the pump, and the CGM, on a regular basis. The algorithm would update the calculations and the predictions, and do it over and over again. It was actually pretty “simple” at that stage!

I very clearly remember the moment that we were able to send a command to the pump. It wasn’t connected to my body - we were testing with a spare pump - but the circle appeared on the screen that alerted us to the fact that a temporary basal rate had been successfully sent to the pump. A few days later we managed to fully close the loop. The night that we closed the loop, I decided to test it on the pump connected to my body. I felt very confident in doing so, because I had the alarms on my CGM as well as the supplementary \(and very loud\) phone alarms that we had designed. Originally, I planned to wake up every few hours to monitor the system, but I love to sleep, so I decided I would just sleep and not bother about the monitoring.

I woke up the next morning and felt discombobulated for a minute. Why did I feel different? Oh yes, I had let the closed loop system run. I took a look at my CGM, and was astonished to see that my BGs had stayed in range all night. I didn’t have a single alarm go off! Anytime my blood glucose rose, the closed loop system gave a little more insulin. When my blood glucose level dropped and was predicted to go low, it reduced the baseline insulin accordingly. My discombobulated feeling wasn’t that anything was wrong - it was the fact that I had gotten a solid 9+ hours of sleep with my blood glucose perfectly in range, and without having to wake up at all.

At that point, I surprised Scott. We originally planned for this to be an overnight-only system that would just sit on my bedside table. However, it worked so well, I wanted to see what it would do during the day, too! So I unplugged it, put it in my laptop bag with one of Scott’s spare batteries, and went to work.

You probably won’t be surprised to learn it worked well during the day, too. It sat on my desk at work, or was in my bag or pocket when I walked around town. I never wanted to turn it off or let anyone take it from me. In fact, four and a half years later, the only time I have not looped was when I was forced to stop, one weekend soon after I had started. I had corrupted the SD card on the Raspberry Pi mini-computer I was using due to unplugging and replugging the power source so many times as I moved between work and home, and letting the battery die a few times. The system stopped working on a Friday afternoon, and we couldn’t find anywhere to get an SD card faster than Amazon Prime 2-day shipping, so I had to go from Friday afternoon until Monday afternoon without my closed loop. It was terrible going back to my old normal. It was such a clear reinforcement of how much benefit this closed loop system was to me, both day and night. We got the SD card replaced and I have been using a DIY closed loop \(with many more backups\) ever since.

\*\*\*\*

DIY closed looping worked incredibly well for me. The computer would send commands to the pump via the radio stick, telling the pump to set or adjust 30-minute temporary basal rates to adjust my insulin delivery. If the system broke or died for any reason, at the end of the 30-minute temporary rate, it would fall back to “standard” pumping, just like before. We assumed that the system would fail, so we designed the system to only set a temporary basal rate if it would be safe to let that basal run to completion and then revert back to standard basal rates. Insulin delivery was adjusted conservatively with that assumption that each adjustment was the last command the system might send.

We wanted to find a way to share this with others. We didn’t think a lot of people would want to do it, but a few might. And we had spent so many months improving the algorithm, and designing for safety. We also knew it wasn’t if, but when and how, the system would fail, so we designed it to fail safely. We thought it was important for others to be able to start from where we had gotten to, rather than recreate the wheel and re- learn some of the same safety lessons.

However, we vividly remembered the conversations with the FDA employees who said that DIYPS code sharing would be ‘distributing a class III medical device’ - and DIYPS was just a system that made recommendations. Now we were wanting to share code for a system that would allow people to automate their insulin delivery.

But we also felt a moral imperative to share what we had learned. Many people who are unfamiliar with type 1 diabetes think that an automated insulin delivery system introduces many new risks. And it does. But the calculation also must include the everyday risks of living with type 1 diabetes. It’s already incredibly risky. Insulin is a life-saving drug, but too much insulin, or the right amount of insulin given at the wrong time, can cause harm, or death. Insufficient insulin can also cause issues in the long run. Having a computer track insulin dosing every five minutes and make micro-adjustments limited by software and hardware safety limits is, for most of us, a lot safer than doing things manually.

We decided that we would share what we had learned. But we’d do a few things in order to share it as safely as possible. First, we wrote a plain-language ‘reference design’ that discussed how the system was designed for safety and outlined all the safety considerations built in via hardware and software. This would be the recommended first stop and first read for anyone considering building themselves a similar system. Second, we would share the code components that had been built. They were two distinct pieces. One was the ‘openaps toolkit’, which was all of the separate commands to read and write to a connected insulin pump. The other eventually became the “oref0” repository, which included the actual algorithm that would determine the needed insulin adjustment. So, the code in of itself was not a single device. You couldn’t press a button and “get” a pancreas. You’d have to take all the components and build it yourself. We decided to call this project, and the movement, “OpenAPS”, to stand for the ‘open source artificial pancreas system’. OpenAPS was launched on the web on February 4, 2015.

