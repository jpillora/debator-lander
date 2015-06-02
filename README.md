:warning: This is a placeholder project. The project name and these ideas are subject to change.

---

# Debator

**Interactive and transparent debates online**

Join the chat room to discuss this planned project:

[![Join the chat at https://gitter.im/jpillora/debator](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/jpillora/debator?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

### Overall Idea

Debates are made up of two concepts: Claims and Evidence.

**Claims**

A Claim is a true or false statement which is in the realm of scientific inquiry. Users optionally set their stance on claim to **For** or **Against** (Reddit style up/down/no-vote). Claims are made in the context of our current scientific understanding, so with new knowledge, Users must be allowed to change their vote over time.

The status of a claim is calculated from two sources, the prior claims that backup this claim and the number of votes For or Against. At any given time, the status of a claim will be one of:

* `True`
* `False`
* `Undecided`

An example calculation algorithm would require some threshold of prior agreement combined with some threshold of user agreement in either the positive `True` or the negative `Undecided`. Without this combined agreement, the Claim is `Undecided`.

Since vote can change over time, status changes can also occur over time. If new evidence is found and a claim is changed from `True` to `False`, this change can lead to cascading status changes across other claims. This is good as it forces pre-existing claims to be re-evaluated.

Users decide their vote by reviewing the Arguments and Evidence. 

![claim diagram](https://docs.google.com/drawings/d/1ROGqx_iZ9OwUmS57BVzWs9Hno2jEppSmwGN725Sf-5U/pub?w=517&h=442)

Within an a Claim, each sentence must be backed up by one or more prior claims or evidence. If a claim is `Undecided`, then *that* debate must be had in order for it to be considered `True` (or it may back fire and prove to be `False`).

![argument diagram](https://docs.google.com/drawings/d/1i-IKMR9W1n_3xHnfmiabU8vRpQ12qHt7wEWQbx4HDrk/pub?w=548&h=495)

**Evidence**

A piece of evidence is a single document or group of documents. It could be a photo, a peer-reviewed paper, a statistic with an accompanying experimental and observational study or a quote. In order to be accepted as evidence, each document **must** include a valid link or a copy of the original material.

Users must be able to rate evidence quality. So if anecdotal evidence or pseudo-scientific evidence is provided, it can be flagged as such by users (at some threshold it will be invalidated and will not count towards any Claims).

---

* Are these good foundational concepts?
* Maybe Arguments are also Claims?
* Speaking in purely factual statements is optimal, though is it realistic?
* What do users vote on? If a "fact" is true or false

---

### Ideas

* Debate types
	* **Objective** (Factual)
		* E.g. *The sky is blue due to light diffraction in the atmosphere* is universally true or false
		* **Focus of beta versions**
	* **Subjective** (Opinion)
		* E.g. *Hotdogs are better than Hamburgers* is true or false depending on who you ask
		* Drops the "which is in the realm of scientific inquiry" part of a claim definition
		* **Not catered for in beta versions**
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
		* New captcha on signup
	* Fight social media zombie rally cries (mass uninformed votes)
		* Must contribute before you are able to vote

---

### Future

* Private groups
	* Universities / Schools
		* Grant students are participants
		* Grant teachers/tutors are moderators
* Auto fetch source to validate link integrity and material quality
* High profile public debates
* Time/Post-length constrained-live debates
