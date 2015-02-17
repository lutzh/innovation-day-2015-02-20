# Xebia/Blaze Innovation Day 2015-02-20
On February 20th 2015 XSD and representatives from GDD will be visiting RFS,
aka Wehkamp, to join the Blaze project teams for an innovation day.

The setup for this day will be slightly different from our usual free-for-all,
*"do whatever you want as long as it transfers some knowledge"* approach,
although there's plenty of room for that too. 

The difference is that, if at all possible, you should pick a topic or
mini-project that can have some impact on things that the Blaze project
teams are currently working on. See below for a list of suggestions and
hints or ask one of the Blaze team members for guidance.

No worries if there's nothing that appeals to you and you'd rather work
on your own projects, just see it as a good source of inspiration for
what to work on.

**Tip:** for the mobile guys we have managed to save three Google Glasses
from obliteration so perhaps you can have some fun with those?

## Schedule

When?           | what?
:---------------|---------------------------------------
08:00 - 09:00   | arrival, breakfast, gear setup
09:00 ~ 09:20   | kickoff in Cookies (cantine)
09:30 - 13:00   | hacking on projects
13:00 ~ 14:00   | lunch in Cookies
14:00 - 16:30   | hacking on projects
16:30 ~ 18:00   | final presentations in Cookies


## Location
RFS (Wehkamp)
Meeuwenlaan 2, Zwolle

**Directions**:
From the A28 in the direction of Zwolle/Groningen, take exit 19 (Centrum),
go right, go right again, go right again into the parking to the side and
rear of the RFS building. Here's a nice [map](https://www.google.nl/maps/dir/52.5132519,6.0774682/Meeuwenlaan+2,+8011+BZ+Zwolle/52.5152065,6.0828772/@52.5144459,6.0785749,17z/data=!4m10!4m9!1m0!1m5!1m1!1s0x47c7df329fe03bc1:0xdcd78115e0808c1!2m2!1d6.0832403!2d52.5145937!1m0!3e0).

Park at the back or the side of the building, go in through the back door
(or the main door, no worries), take the stairs to the second floor, keep
left and walk past the foosball table into the 2B wing. 

Hacking will take place in the blaze spaces at the end of the 2B wing,
the two main conference rooms on the right, and (very probably) the space
on the left currently used by another team.

Parking is free so please ignore any parking meters you might see; those
are for evenings only.


## Projects
The following projects will be worked on. For a list of other ideas and
suggestions, see the next section.

---------------------------------------------------------------
**Project**
Visual product matching and recommendations

**Description**
Use image interpretation and matching algorithms to build cool stuff on top
of the Wehkamp product catalog.

**Contact person(s)**
- Ivo (GDD)
- Friso (GDD)

**Team members**
- Joshua (XSD)
- Misja (XSD)

---------------------------------------------------------------
**Project**
Clickstream data analysis, product recommendations, and more.

**Description**
Use the existing clickstream data gathered in production by GDD's
Divolte to grou/classify users, generate product recommendations, etc.
Lots of work has been done in this field already so you can have a
flying start and go straight for the interesting stuff.

**Contact person(s)**
- Kris (GDD)
- Vincent (GDD)

**Team members**

- Constantijn (XSD)
- Tünde (GDD)
- Marjolijn (Wehkamp)

---------------------------------------------------------------
**Project**
Akka/Spray metrics

**Description**
We are currently not collecting any kind of metrics on average, mean, minimum, maximum response times, number of requests per time period, actor mailbox bottlenecks, etc. These would be very useful indeed so we want to play with akka-monitor and kamon and connect those to our existing (or new) SAAS metrics services (mainly New Relic).

**Contact person(s)**
- Age

**Team members**
- Jan Toebes (XSD)

---------------------------------------------------------------
**Project**
Single/Multi Page AngularJs Apps and SEO

**Description**
The current implementation of the Wehkamp Belgium platform uses AngularJs in a complicated combination with some server-side generated pages, all in order to be able to deliver correct SEO behavior. This is a dead end and its time we fix it so the plan is to replace all server-side generated pages with a proper API and AngularJs frontend. 

But what about SEO? We want to play with several ways to generate static google pages in a way that is compatible with an e-commerce company that heavily depends on Google for income. We have looked at prerender.io or simply building our own separate app that serves those few special pages in a serverside rendered way specifically for search spider bots. Help us figure this out!

**Contact person(s)**
- Ruben
- Age (backup)

**Team members**
- Jochem (Wehkamp)
- Vincent (wehkamp.com)



---------------------------------------------------------------
**Project**
XSD CV Generator

**Description**
Quote from a recent mail thread: 

> *"Als we dan toch bezig zijn, kunnen we het cv niet gewoon aanleveren in een template
onafhankelijk formaat zoals bijvoorbeeld JSON? Een tooltje zoals Jasper reports erbij
om inhoud in een template te gooien en er komt vanzelf een nette PDF uit. Zodra de
template gemaakt is kan iedereen zijn eigen CV in json omzetten en ziet het er altijd
hetzelfde uit."*

We'll be doing this :smiley:

**Contact person(s)**
- Constantijn
- Ruben

**Team members**

---------------------------------------------------------------
**Project**
Explore solutions to common problems in different languages, etc.

**Description**
We want to start with trying to compare solutions for simple problems using Clojure, Scala and Go. The goal is to see if significant differences in effort and complexicity are incountered

**Contact person(s)**
- Joost
- Daniel

**Team members**
- Joost
- Daniel
- Marc
- Jesse

---------------------------------------------------------------
**Project**
Distributed Akka Persistence!

**Description**
The original guy behind Akka Persistence, Martin Krasser, has started a new project that takes those original ideas to the next level. It might be cool to experiment with this technology in the context of an Aka cluster. Check it out: [Eventuate](https://github.com/RBMHTechnology/eventuate). One of the most interesting things for Wehkamp would be sharded/replicated persistent actors that use CRDTs and distributed pub-sub behind the scenes to stay in sync. Goal: run a clustered akka app where the same persistent actor runs on every node and stays in sync without producing conflicts.

**Contact person(s)**
- Age

**Team members**
- Arnout


---------------------------------------------------------------
**Project**
Deploying apps & micro-services to AWS: towards Docker!

**Description**
At Wehkamp we are currently using a large Ansible codebase to completely configure and deploy our AWS landscape. This contains everything from setting up virtual private networks, security roles, load balancers (ELB and HAproxy), etc to deploying our actual software (Scala/Akka/Spray services) and the stuff around it (Cassandra, Elasticsearch, Kafka, Hadoop). All of this is currently run in three environments (dev, accept, production) and kicked off from Bamboo.

The teams are currently looking at migrating towards Docker and (probably) Consul but no final decisions have been made so there is a lot of room left for experimentation.

What Wehkamp needs is some direction/options of how to organize this entire stack into easier to reuse and layer chunks. Docker is an obvious target for the apps and services (although clustering makes it a little harder) and perhaps also for the Cassandra, etc. But how do we better separate the AWS setup stuff from the deployment stuff? Should we go for Mesos? Should we use Consul? How do we network docker containers together? How does this interact with our (HAProxy) load balancers?

**Contact person(s)**
- Jurjan Woltman
- Paul Frederix

**Team members**
- Armin (XSD)
- Jaap ter Woerds




---------------------------------------------------------------
**Project**
**Description**
**Contact person(s)**
**Team members**


## Proposed Projects/Ideas

### Mobile / Responsive / UX
Some rough ideas:

- **Play with Google Glass**
- **"speak to search"**: a web/app button that translates spoken word into a Wehkamp product search
- **Fancy native app UX showcases** (iOS8 or Android material design) for searching Wehkamp and browsing through products, etc.
 
---------------------------------------------------------------
**Project**
Something WatchKit

**Description**
To be added

**Contact person(s)**
Jeroen Leenarts

**Team members**

---------------------------------------------------------------
**Project**
Fancy 3D product image browser

**Description**
Jeroen W. and Roy were working on something cool like this during an XKE before they left the project.

**Contact person(s)**
Jeroen Willemsen, Roy

**Team members**


### Scala / Akka / Spray

---------------------------------------------------------------
**Project**
Akka cluster upgrade madness

**Description**
At Wehkamp we are using Akka cluster in combination with persistent cluster singletons and persistent cluster sharding. This is awesome for development but it does make continuous deployment slightly harder because there is no good way to upgrade the running cluster node-by-node while guaranteeing backwards compatibility (like incompatible serialization or an Akka version upgrade). Currently we do indeed upgrade node by node but there must be a way to setup two clusters with one in read-only mode. The Akka dev team has hinted in that direction. Let's see what we can come up with...

**Contact person(s)**
Age

**Team members**


---------------------------------------------------------------
**Project**
Akka remoting and guaranteed message delivery over Http?
**Description**
All of our Wehkamp apps and services are developed on top of Akka and Spray but at the moment we need to explicitly build Http REST APIs to communicate between services. Wouldn't it be nice if we have some kind of bridge library to tunnel Akka messages over Http? It would make connecting service a lot simpler without directly tying them together by sharing domain code, which we would have to do if we would use the existing Akka remoting stack. 

Alternative: build a simple http client library wrapper around spray-client that takes care of retries with incremental backoff
**Contact person(s)**
Age
**Team members**


### Very rough ideas

- **feature switches**: how to (de)activate code/features/behavior at runtime or deployment (or any) time while keeping the code clean?
- how to integrate **A/B testing** into a micro-services architecture

