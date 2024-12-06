# Introduction to Continuous Integration (CI)
* Automated ways to make sure code works / automated testing system
	--> Like a "raincheck" for code
* Always making sure that **software is in known state**
* Two things to remember about CI:
	1. Software is always **knowable** -- what software is -- and whether it is working or not
	2. **Saves time** instead of costs time

# What is CI?
1. First, do **local scaffolding**
	(See [this graph](https://github.com/maryjess/cloud/issues/14))
	`maketest` --> ensures that code is working locally

2. Second, make sure that **SaaS Build Server** (aka GH Actions) is ready, to automatically test code
	* Everytime change to environment is made, **Event** will be triggered that checks code -- CO (Check Out)

Essentially, CI is process of replicating local to SaaS (Software as a Service) Build Server available in the Cloud
--> Just like **Testing Factory** who is always there to test your code