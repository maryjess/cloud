# Quarterly Plan
* Project Schedule mapped out week-by-week for an entire Q (ie 12 months/4 = 3-monthly-plan)
* To outline goals and plan development
* Gets the idea flowing

```
plan = {
	"Q1" : {
		"W1" : ["Goal 1", "Goal 2"],
		"W2" : ["Goal 3"],
		# ...
	}
}

```

---

# Ticket Tracking
* use System to Track Progress on (tasks) and (action items)
* can see Status in Progress w/o Excessive Meetings
* can do using GitHub Issue

## [Useful CLI Command](https://cli.github.com/manual/gh_issue)
See [Issue #6](https://github.com/maryjess/cloud/issues/6)
```
gh issue create --title "Configure database" --label "Priority: High" --web
```

---

# Continuous Delivery (ie CD)
* SWE practices to Build, Test, and Release softwares rapidly, reliably, and sustainably

## Python Package `ci_cd`
```
import ci_cd

pipeline = ci_cd.create_pipeline()

pipeline.build()
pipeline.test()
pipeline.deploy() # Continuous Delivery
```

---

# Automated Testing
* Runs automatically w/o human input to verify software functionality and correctness

## Python Package `unittest`
```
import unittest

class TestSum(unittest.TestCase):
	def test_sum(self):
		self.assertEqual(sum([1,2,3]), 6)

if __name__ == '__main__':
	unittest.main() # Automated test
```

---

# Kaizen
* Japanese philosophy focused on Continuous Improvement through gradual and incremental steps
* Basically Continuous improvements over time and To not be static