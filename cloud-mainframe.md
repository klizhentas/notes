# Breaking out of a cloud mainframe

## The endless loop

History often repeats itself, in 70s advances in microcomputers gave hippies and hackers a freedom 
to create their own personal computers and break the IBM monopoly on the innovation in the space.

Further down the road, open source software forced the seemingly unbreakable closed source monopoly, 
the benevolent dictator Microsoft to reinvent itself and embrace Linux.

It seems like we are observing the third installment of the same David vs Goliath story, this time AWS is the 
monopoly to slay, but no Woz in sight yet.

## Coding against the closed system

PG famously wrote in “Beating the averages” that one of his motivations to create a web based application 
versus a desktop one was to avoid writing C on Windows - the idea that he and friends absolutely loathed. 

Writing against a closed system is a tedious task - every software in the world has it quirks and at some point, 
any hacker will hit a block - why this thing does not work? In an open system, anyone can dig in, 
dig through the library code, language runtime, kernel and drivers, and get some great answers and experience as a result. 
When you encounter the same problem on a closed system it feels like you hit a wall, and there is no way to climb over it. 

First time I got this feeling when starting my first job as a systems engineer on Windows. 
Compared to the Linux, MSDN was very polished and robust piece of documentation (that you had to pirate if you are a poor 
student in Russia), but it had one great omission - source code. Linux docs sometimes were terrible, but with code 
and patience, you can get all the answers you want.

Fast forward 15 years, and I’m getting the same vibe writing against the AWS SDK, but this time docs get nowhere near MSDN 
in terms of quality. Do you know off the top of your head if AWS EKS supports CSR API? The answer is “NO”, but you’d have to ask the EKS team. Any thoughts on how DynamoDB submits the event to the shards in special cases? Try getting the answer by 
asking them, or digging the forums, you would find nothing specific in the official docs. 

In 90s you got a benevolent dictator, but at least a good architect running the show. 
This time, it’s 100 teams rolling their own API and throwing results at you. It’s even worse, as instead of one, you get the big three - AWS, Azure and GCP to deal with, each with their own quirks, 
APIs and all closed from your view.

They are all created by friendly developers you would meet at the conferences and have a great time with, 
they are just like you, with one key difference - their org produces closed source, security is tight, 
and they are often powerless to do anything about it. 

## Playing the rigged game

Folks in the Microsoft era were scared to death that Big G will notice their invention and come after them. 
These days, folks who roll out any service on AWS will be constantly worried that AWS will copy their product. 
This time, AWS won’t even have to write too much code. They could just take your software from github and launch 
a managed service of it, all in the name of serving their customers. 

Try to compete with them on the margins? You have already lost -  you can’t make it cheaper on AWS than AWS itself. 

Many times people will use AWS services if it’s inferior to the alternative, after all, nobody got fired for buying AWS. 
Besides, this service is so conveniently integrated with the rest of the bill, and your finance and legal are happy.

This is the reality for many companies out there - lots of devs from small and big software shops I talk to in the 
private conversations admit that AWS is their concern and they are “keeping an eye on them” or are in “coopetition”.

## The cloud of equal opportunities

Should we blame AWS for our troubles? Not really, AWS, Azure and everyone else can do whatever the hell they want - 
private corporations are often key the drivers of the innovation and we should not worry too much about them. 
Sooner or later, the cloud will be commoditized by the open source and some years from now AWS will instill as little 
fear on the software developer as Microsoft does now. 

We should be blaming ourselves for not thinking enough about the “Plan B”. We need to get back to our roots and make 
the alternative that is based on the open protocols, collaboration and open source technologies - the timeless guiding 
principles that gave us all the opportunity to have the internet and personal computers. 

I think cloud and data center technology came to the stage where we can build fully open spec for th open source 
datacenter with common interfaces and APIs, where every software vendor can be on the level grounds with everyone else, 
using open networking protocols to define SDNs, picking hardware profiles that match their needs and using the same utility 
priced bandwidth.

Many players with big computing footprints like Facebook, Dropbox are not really thrilled to migrate to AWS at some point 
are are actively pushing for open source hardware specs and open source SDNs.

Thanks to them, linux open networking and "whitebox switches" already knocked on Cisco’s door.

We just need one last push, a new Compaq Pirates to blatantly clone the AWS API and launch a new fully open source IBM-PC 
compatible datacenter for everyone to tinker with. The one where main analytics software battle will be with ElasticSearch 
and Splunk, not ElasticSearch and ElasticSearch AWS.
