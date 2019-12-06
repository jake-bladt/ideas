# The Idea File

## Overview

Talking to people in the start-up community, I frequently hear people worry about having their ideas stolen. I nearly always tell them that ideas aren't worth stealing and that the approximate value of any idea before work is applied to it is zero.

Putting my money where my mouth is, I'm keeping my project ideas in public view - not just to prove a point, but in the hope that someone will steal the idea, create the product in question, and offer it for my use so that I don't have to build it myself.

## Project Ideas

### Authentication as a Microservice Cluster (Pilgrim)
Any non-trivial application I build based on the model of a static site backed by serverless functions will require some authentication solution and preferrably one that follows the same architecture. I'd also prefer to not requre an LDAP backing store because that's a lot of admin for what may be a small collection of users.

If I pick another project to start with, I'll probably create the minimum system necessary. If I choose to start with this project, I'll want to build something that can be dropped into multiple projects and configured.

### Beta-My-Book

This was the front-runner for a while: a site where authors can share unfinished material with their beta readers, get feedback, and make edits in real-time. I still really like the idea, but the primary motivation of building the site was to use it myself and, as it turns out, there's already a site that offers these services. Equipped as I am with training in DevOps and Continuous Deployment, the idea of building a competitor to an existing site on my own is no longer a deal-breaker, but the motivation to build it is much less if I can get the service from an existing site.

### Build, Seed, and Patch
BSP is a .net library that allows the repeatable creation of databases by writing idempotent scripts to setup and roll back entities and data. I suspect there's probably a tool out there that does this already, in which case I would happily use what's already available.

One possible use for this would be to be able to create and destroy a database as part of automated testing.

### Chatterbox
Chatterbox is a project I started to play with when I was doing a lot of Slack automation. This is a purpose-built server that accepts web hooks and applies transformations to those messages before forwarding them to messaging platforms (Slack initially, but e-mail and queue servers should be pretty straightforward add-ons.)

### Consensual World platform

The premise of this is to create a platform for presenting fictional settings as canon and allowing users to add their own content into the website while distinguishing between the two sources. This may be a product with an audience of one.

### Contain Me

Contain Me is an API that allows teams to manage and launch a subset of containers keyed by user.

### DBScaffold

A testing component to allow individual tests to build and seed parts of a database before they run (and tear them down after they're done.)

To be done right, may require a SQL-like DSL...

Also, I wonder what the practicality of using EFCore for continuous testing is. Could you do DB-first EF, then use the artifacts created to regenerate the database under test?

### The DevOps game

Possibly a Zork-like command-line game, possibly a web game - a game in which the player's job is to take a dysfunctional IT department to "ten deployments a day."

### Docker Decompose

A proof-of-concept application to take a docker-compose file, look for PLATFORM directives, and split the containers between Linux and Windows virtual machines, then connect them up using an overlay network.

### DraftNinja

DraftNinja is a perennial possibility and has ranged in scope from a desktop tool that can update relative values of draft choices in fantasy baseball in real-time as players are taken off the board to a full ML system that can look at years of box scores and come up with better predictive models than those that are commercially available. They all flounder on the fact that none of the solutions have a value proposition worth the work I would have to put into them. I just don't care about fantasy baseball as much a I used to. I don't know that I want to put in the effort to create a system I'd be comfortable putting serious money into. And I don't feel like I need a showcase piece so badly than I should spend months building one that doesn't bring me joy. Plus, I'm pretty sure the state of ML is a big enough moving target that whatever I learn building it will be immediately obsolete.

### Domain mail as a service (CloudMail?)

While sending e-mail has been cost-optimized as a service, managing domain e-mail accounts continues to be prohibitively expensive. The [best deal](https://www.rackspace.com/email-hosting/webmail/pricing) is still US$3/user/month, making many possible configurations prohibitively expensive. Shared hosting plans like those provided by HostGator manage domain e-mail free with LAMP hosting, suggesting that the price of providing this service is negligible.

CloudMail could possibly even be an orchestration service that manages cloud servers and resources owned by the clients. They provide cloud account keys and parameters. CM's servers spin up, monitor, amd scale mail servers, block storage, and other cloud resources on those accounts for an orchestration fee. If you need a single server managing a single pool of mail, the orchestration could be free.

### The Endorphin Engine

An actor decision engine based around an "endorphin profile" that allows for both rational and irrational actions, possibly using Akka.net.

### Fantasy Campaign hugo theme

A theme to generate websites for fantasy campaigns using the Hugo static website generator - eventually to be combined with a web front end meant to create the files used to generate the site.

### Foggy Chess

A chess game with "fog of war." Players can't see the board automatically. They can only see spaces that meet one of the following conditions:

* within one space of a king, pawn, bishop, or rook in a direction that piece can capture.
* capturable by a knight or queen.

This is based on a deliberately poor understanding of [Franklin K. Young's Logistic Grand Battle](https://www.futilitycloset.com/2019/11/16/the-fog-of-war/).

### Home Game Poker

A simple server and UI for running poker games over the Internet, straightforward enough for non=-technical users.

### Jayanesia

A political Euro-style game in which the players take the roles of power centers on a South Pacific archipelago and work towards differing goals through alliances, betrayals, and other actions.

### JEFE (JavaScript Entity Framework Extensions)

An extension to Entity Framework that generates RESTful endpoints and an EF-like library of objects to be used on the front-end, written in JavaScript (or maybe WebAssembly!)

### Magnate News Aggregator

A platform that scrapes the web, looking for news sources on a given topic and tracking their updates to create aggregator sites and newsletters.

### The Nimrod Project

A site focused on helping developers coordinate and manage their career and job seeking.

### The Open Water Project

A one-stop site to aggregate the information needed by charities focused on clean and potable water to choose where to start programs and to measure their efficacy. 


### Personal Website

It's been a few years since I put up a portfolio website for myself. It would be a static website, probably generated in hugo, and be unlikely to take more than 100 hours for the initial creation and deployment. As a downside, I don't have much to put in a profile website. The work that I've done for hire is just much more of a selling point than any project I have in github. If I decide to take this as a primary project, I really need to timebox it. More likely, I'll try to finish at least one "cool" project and then come back to it.

Also, if I get back into dev blogging, I'm more likely to give dev.to a try than to go my own way.

### QD Backup
This is a project I started years ago to replace the clunky interface and tools I was using to backup my essential files both to a network drive and to a cloud provider. I suspect [synchthing](https://syncthing.net/) does everything I need and would want to investigate that assumption before building my own tool.

### SimpleCloud
A UI to make setting up and monitoring basic cloud resources easier.

### Sunspot

A serverless function to allow processes that hold the correct secrets to request time-limited firewall modifications in real-time.

### Time Slices

A C# library for handling slices of time - different from TimeSpan in that it handle specific time spans - ie, 

```
// the first fifteen minutes of the year 2020
var slice = new TimeSlice(new DateTime(2020, 1, 1), TimeSpan.FromMinutes(15)); 
// a series of fifteen-minute slices covering the first day of the year 2020
var slices = new Series<TimeSlice>((new DateTime(2020, 1, 1), new DateTime(2020, 1, 2), TimeSpan.FromMinutes(15)); 
```

I've been kicking this one around for so long, I don't remember what project I wanted to use this for, but it probably involved histograms and time-series analysis.

### U of I

A lifetime learning portal that allows users to store links and notes to facilitate their self-teaching and to provide limited public views as a type of CV.

### WorldMap project

A fantasy worldbuilding tool that allows game designers/runners to start at the top, drawing continents, and oceans, and zoom all the way down to individual characters and items - probably meant to work with the Fantasy Campaign hugo theme.

