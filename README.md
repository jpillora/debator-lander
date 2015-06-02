:warning: This is a placeholder project. The project name and these ideas are subject to change.

---

# Debator

**Interactive and transparent debates online**

Join the chat room to discuss this planned project:

[![Join the chat at https://gitter.im/jpillora/debator](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/jpillora/debator?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

### Overall Idea

Debates are made up of three concepts: Claims, Arguments and Evidence.

**Claims**

A Claim is a true or false statement which is in the realm of scientific inquiry. Claims are made in the context of our current scientific understanding, which inherently means they may change over time. Users are required to evaluate the arguments and set their stance on each of the arguments (reddit-style voting). It’s important to note, users do not vote on the claim, only its arguments. Using an algorithm, the status of the claim is defined to be true, false or undecided (for example, one algorithm could say that 80% of votes in for arguments would set a claim to be true, 80% in against would set it to false). As in science, with new evidence, we should be able re-evaluate our claims. Status changes in one claim can have cascading effects to other claims which used it as an argument. Claims which are undecided contribute no points to other claims.

![claim diagram](https://docs.google.com/drawings/d/1ROGqx_iZ9OwUmS57BVzWs9Hno2jEppSmwGN725Sf-5U/pub?w=517&h=442)

Once widely accepted or rejected, it is considered settled and can then used to greater effect in arguments of future debates. If rejected, it may be used in the reverse.

**Arguments**

An argument is a contentious or complex claim which is not a true or false statement (if they do , then maybe they should be a claim). Will often include scientific evidence, such as experimentational and observational studies. If anecdotal evidence or pseudo-scientific evidence is provided, it should be flagged by users, and then also voted on, and at some threshold, it will be invalidated and will not count towards the final claim.

![argument diagram](https://docs.google.com/drawings/d/1i-IKMR9W1n_3xHnfmiabU8vRpQ12qHt7wEWQbx4HDrk/pub?w=548&h=495)

An Argument must be backed up by one or more claims. If a claim is undecided, then that debate must be had so it can be accepted or rejected. An argument score is the weighted sum of the votes, where the weight is determined by the acceptance of its claims.

An Argument has 3 states:

* Valid – One or more of claims make sense though are not proven
* Invalid – One or more of the claims do not make sense
* Sound – All of the claims are accepted

**Evidence**

A piece of evidence is a single document or group of documents. It could be a photo, a peer-reviewed paper, a statistic with an accompanying study or a quote. In order to be accepted as evidence, each document **must** include a valid link or a copy of the original material.

---

### Ideas

* Debate types
	* Factual - *The sky is blue because of light defraction* (**Focus of beta versions**)
	* Opinion - *Hotdogs are better than Hamburgers* (This type drops the "which is in the realm of scientific inquiry" part of a claim, **not catered for in beta versions**)
* Color coding
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
