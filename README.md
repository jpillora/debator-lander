:warning: This is a placeholder project. The project name and these ideas are subject to change.

---

# Debator

**Interactive and transparent debates online**

Join the chat room to discuss this planned project:

[![Join the chat at https://gitter.im/jpillora/debator](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/jpillora/debator?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

### Overall Idea

Debates are made up of three concepts: **Claims**, **Arguments** and **Evidence**.

**Claims**

* A Claim represents a debate and comes in the form of a true or false statement.
* A Claim contains Arguments:

![claim diagram](https://docs.google.com/drawings/d/1ROGqx_iZ9OwUmS57BVzWs9Hno2jEppSmwGN725Sf-5U/pub?w=517&h=442)

* In public debates, anyone may present their own Argument.
* Users may then review each Argument and add a vote any of the arguments.
* Users must be allowed to add or remove their vote from any Argument over time.
* The status of a claim is calculated from its arguments (Calculation method is currently undefined)
* The status of a claim will be one of:
	* `True`
	* `False`
	* `Undecided`
* Since status' can change over time changed, these changes can lead to cascading status changes across other claims. This is good as it forces existing claims to be re-evaluated.

**Arguments**

* An Argument represents an answer to its parent Claim
* An Argument must be either `For` and `Against` the Claim
* Within an a Argument, each sentence must be backed up by one or more prior Claims or pieces Evidence. If a claim is `Undecided`, then *that* debate must be had in order for it affect the Claim.

![argument diagram](https://docs.google.com/drawings/d/1i-IKMR9W1n_3xHnfmiabU8vRpQ12qHt7wEWQbx4HDrk/pub?w=548&h=495)

**Evidence**

A piece of evidence is a single document or group of documents. It could be a photo, a quote from a peer-reviewed paper, a statistic with an accompanying experimental and observational study. In order to be accepted as evidence, each document **must** include a valid link or a copy of the original material.

Users must be able to rate evidence quality. So, if anecdotal evidence or pseudo-scientific evidence is provided, it can be flagged as such by users (at some threshold it will be invalidated and will not count towards any Claims).

---

### Questions

* Are these good foundational concepts?
* Making a case for something in purely factual statements is optimal, though is it realistic?
* What should users vote on?
* What are acceptable sources of evidence?

---

### Ideas

* Debate types
	* **Objective** (Factual)
		* E.g. *The sky is blue due to light diffraction in the atmosphere* is universally true or false
		* Only scientifically verifiable Claims can be used
	* **Subjective** (Opinion)
		* E.g. *Hotdogs are better than Hamburgers* is true or false depending on who you ask
* Claim color coding
	* Traffic-light theme
		* False claims are red
		* True claims are green
		* Undecided claims are orange
	* Intermediate colors
		* 70% accepted might still a shade of orange with the green
* Markdown style text input
	* Additions for citation (attaching **Evidence** to sentences)
* Duplicate claims are good
	* Duplicates are linked to each other
	* Promote choice when citing another “previous” claim
	* Allows inverse-duplicates, where one claim proves claim C1 and another claim disproves claim C2, where C1 and C2 are the inverse of each other.
	* **Issue** – If one duplicate is true and another is false. Must allow for some way for users to rectify this.
* Navigation
	* Shortcuts to "dive into" arguments and "go back" to previous claims
* Comments
	* May help to improve content
	* May be used to troll
* Gamify
	* Badges, Trophies, Coins (StackOverflow style)
* Example use-cases
	* Scientific debates
	* Political debates
	* Religious debates

---

### Dangers

* Trolling and Quality issues
	* Needs to be moderated
		* Determine clean method of expert/moderator verification
	* Poor quality of arguments
		* How does Wikipedia do it?
* Scale Issues (*more than 1000 users*)
	* Fight botnets
		* New single-click captcha on sign-up
	* Fight social media zombie rally cries (mass uninformed votes)
		* Must contribute before you are able to vote

---

### Future

* Private groups
	* Universities / Schools
		* Students are participants
		* Teachers and Tutors are moderators
* Auto fetch source to validate link integrity and material quality
* High profile public debates
* Time/Post-length constrained-live debates
