# Security 101 Bootcamp
**Brought to you by [Aura Information Security](https://aurainfosec.com) and Summer of Tech**

Welcome to the Security 101 bootcamp for Summer of Tech 2020! This page will guide you through some of the hands on aspects, in case you missed the talk.

> ### **⚠️ WARNING ⚠️** 
> With great power comes great responsibility.<br />
> 
> Never hack a website or app if you don't have explicit permission.<br />You only have permission to hack the "Aura Hacker Store" on `sot.aurainfosec.io`.<br />
> 
> You must not maliciously hack any teammates you're working with. Rickrolling is fine.<br />
> You must abide by the [Summer of Tech Code of Conduct](https://summeroftech.co.nz/about/code-of-conduct/).

## 0. Links

  - Summer of Tech #code channel on Slack: https://app.slack.com/client/TV6M47FCY/C011KM58BQD
  - Hacking Platform: https://sot.aurainfosec.io
  - Scoreboard Platform: https://scores.sot.aurainfosec.io


## 1. Getting Started

We've built a hacking platform where your team (or just you, if you're going solo) can get a fully isolated and intentionally vulnerable web application. This is a great place to learn how to identify and exploit security flaws, so that you can prevent them from happening in your own applications.

1. Visit https://sot.aurainfosec.io
2. Choose a team name and click "Create / Join Team"
3. Note down the password for other team members, or in case someone wants to join you later.
4. Enter the Aura Hacker Store!

From here, have a look around. Use the app like a normal visitor would. When you're more familiar with an applications' intended functionality, it's easier to spot unintended bugs.

## 2. Find the Scoreboard

Aura Hacker Store is built using OWASP Juice Shop, and that comes with a page where you can see all the challenges you've completed, and get hacking tutorials.

We'll following the first tutorial we see which leads us to the score board. If you don't want to follow a tutorial, skip to **4. Submit a CTF Flag**.

Here are some ideas for finding the right URL:
  - Try and guess it. If you made a scoreboard page, what URL would you choose?
    + This is why "security by obscurity" doesn't work; just because the developers haven't put a link on the Hacker Store doesn't mean visitors can't just guess the URL!
  - Look for a reference to it in the client-side javascript by opening Firefox Developer Tools.
    + This is why access controls (e.g. logging in) are needed to keep  unauthorised people away from secret pages; you shouldn't rely on the URL being unguessable
  - It's becoming common practice for websites to have a security page or text file that includes contact details and other important information. Maybe this website has one?

You'll know you've found it when you see a scoreboard full of challenges, and get a banner which says you've found the scoreboard. It'll also have a random string, or CTF Flag, which we'll use in Step 4.

## 3. Perform a DOM-based XSS Attack

Cross Site Scriping, more commonly called "XSS" (because CSS was taken ;)), is when an attacker is able to run their own javascript on a victim's page. This is bad because javascript can change the way a page looks and ask you for you password, or it can intercept information like credit card details, or just redirect you off to a fake banking site.

In this challenge we'll follow the tutorial for a DOM-based XSS Attack. Find it on the scoreboard, and click the orange hat button.

You'll know you've done it when you've been able to make a popup appear, and a banner shows on the page saying you've solved it.

## 4. Join the Competition (Optional)

> ℹ️ **Important** This is completely optional. If you just want to have fun and learn, don't worry about this. 

You should have (at least) two CTF Flags, which are the random-looking strings included in the banners you get when you solve a challenge.  
But since you have a fully isolated Aura Hacker Store instance, it can't show your progress to anyone else but you and your teammates. 

If you want to compete, submit your flags to the [Security 101 Bootcamp Scoreboard](https://scores.sot.aurainfosec.io). This will publicly record your points on the [scoreboard](https://scores.sot.aurainfosec.io/scoreboard), so we'll all be able to see how well everyone is doing!  
Only one team member needs to do this.

To do this:

  1. Visit https://scores.sot.aurainfosec.io
  2. Register an account, and create a team with the same name that you used for your Aura Hacker Store
  3. Visit the "Challenges" page
  4. Find "Score Board", click it, and enter the flag from that banner. That's 100 points!
  5. Find "DOM XSS", click it, and enter the flag from that banner. Sweet, another 100 points!

You can use the Challenges page to see how many points you can earn by solving various challenges.

## 5. FAQ

### What now?

Have fun! Hack the Aura Hacker Store at your own pace. Optionally, use the bootcamp scoreboard at https://scores.sot.aurainfosec.io

### How do we work as a team?

You can all join the same Aura Hacker Store instance by using the same team name, and sharing the password.

Set up an invite-only channel in Slack for your team to collaborate and help each other out. 

### I can't see my CTF Flag anymore!

On your Aura Hacker Store scoreboard, to the right of each _solved_ challenge, is a flag button. Click that to make the banner and CTF flag show up again (at the top of the page).

### I need help with a challenge

The Aura team are in the Summer of Tech Slack while the bootcamp runs, and **we are here to teach and help**. No question is silly, please just ask!

Ask for help in #code, tell us the challenge you're stuck on, and one of us will respond.

You can then invite the Aura team member in to your private team channel once you know who's able to help.

### Do people really make apps with these bugs?

Yes, bugs like these are unfortunately really common. Check out the [OWASP Top 10 Web Application Vulnerabilities](https://owasp.org/www-project-top-ten/) to learn more. 

The OWASP Top 10 is one of the most commonly referred to documents when it comes to web app security, so it'll be time well spent.

### What's Burp Suite and how do I use it?

Burp Suite is a tool which makes it a bit easier to hack. Aura's penetration testers use it a lot in their day to day work. A lot of hacking is trying lots of little variations and seeing what breaks; Burp Suite can automate that. Hacking also involves report writing with clear steps to reproduce the bug; Burp Suite can keep track of all the requests and responses. There are lots of things tools Burp Suite can do. 

**We've written a quick intro guide here:** https://github.com/aurainfosec/summer-of-tech-2020/using-burpsuite.md

Burp Suite has a [free community edition](https://portswigger.net/burp/communitydownload) with a limited feature set. [OWASP ZAP](https://www.zaproxy.org/) is another excellent option, is free open source, and can even be integrated into DevOps pipelines for automated testing!

### Isn't this just OWASP Juice Shop?

Yes it is! Juice Shop is fantastic. We've just given it a lick of paint to make it more fun for the Security 101 Bootcamp.

### But doesn't that mean...

Yes, it does mean that the excellent companion guide, Pwning OWASP Juice Shop, will guide you through each and every challenge. That's great, and we have no problem with you using that.

There are also all of the challenge solutions. You should just ignore this until after the Security 101 bootcamp. You could use the answers to get a massive score, but then you're just someone who can blindly read and follow instructions. We don't want to hire people like that at Aura. We want curious, independent thinkers who can follow their nose and find and exploit vulnerabilities.

### What can I do to get an internship at Aura?

Tell us what you learnt at this bootcamp when the Summer of Tech Meet and Greet happens. Tell us what you got stuck on, and how you pushed through it. Tell us what you went away and learnt after the bootcamp. Show us some examples of your (legal) hacking skills in practice.

### Where else can I do legal hacking?

  - [BugCrowd.com](https://bugcrowd.com)
  - [HackerOne.com](https://hackerone.com)
  - [OverTheWire](https://overthewire.org)
