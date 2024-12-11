# Introduction to Testing
> When there is no way to fix the problem, other than to dig into it and figure out. 
## What are the 'figuring out' steps?
* **First step:** Get some tests working in a simulated environment
  * Can I take production and replicate somewhere?
  * Setup Continuous Delivery type environment
  * Once ran, can still verify that something's going on
* **Second step:** Add instrumentation and monitoring
  * Add logging
  * Add some dashboards -- showing what's going on


* Combination of these two things are **critical**

---

> It's easy to get caught up in the purity of testing
### Wisdom / Zealotry in Testing:
* Selectively choose WHEN to test something
* Sometimes don't need 100% test coverage, or don't need to have full functional tests
* Using JUST ENOUGH to solve a problem + having the test AUTOMATED
* Else, too much time wasted in testing :<
  * Unless it's a brownfield project (previously had been worked on)

---
# Testing Strategy
1. "Just right"
   * Have enough, that you know what you are doing works

2. Use judgment
   * Gotta have that Suspicion that a part of the app might have a problem --> that instinct to do testing

3. Save you time
   * Testing is not a time waster, instead it saves you time :>
   * So that don't need debug the same thing over and over again

4. Automation
   * Once the testing works, automate it
     * via Build Server (e.g. GitHub Actions) 