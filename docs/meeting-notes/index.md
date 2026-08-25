# Meeting Notes

Meeting notes and decisions.

---

## OBP Milestone 4 - Requirements alignment
**Date:** Aug 24, 2026 04:00 PM  
**Attendees:** Miguel Gomes, Ross White, Donough Regan  
**Format:** Shared screen with speaker view

### Summary
Clarification on Liability Engine requirements for Milestone 4, specifically:
1. **Max Stake Capping** - Ability to cap maximum stake when liability thresholds are exceeded
2. **Max Winnings Cap** - Apply max winnings cap on bet combinations
3. **Automated Kill Switch** - Ensure automated kill switch works for EMF and OBP combined bets

Key findings:
- The first two requirements appear to already be delivered in Milestone 2
- Work needed: Single endpoint to capture both selections and choices
- Automated kill switch is new work (not yet delivered)

### Action Items
- [ ] Check with Tiago on estimates and requirements clarity
- [ ] Create tickets to formalize the work
- [ ] Ross to walkthrough automated kill switch implementation with Miguel

<details>
<summary><strong>Full Meeting Transcript</strong></summary>

**Miguel Gomes:** Hello, everyone.

**Ross White:** Hey.

**Donough Regan:** What's going on?

**Ross White:** How you doing? So, I'm hoping this should be pretty straightforward, so I just wanted to catch up, because... Obviously, as we were capturing the requirements for Milestone 4, there was a few identified in lighter than the engine, and I think it was probably just a gap on the product side from taking those initial estimates, but actually then formalize that work on the backlog, so, even just creating the initiatives, etc. So, I just wanted to be really clear, Donner here, maybe you can help to clarify, just on the two liability ones, engine ones.

So it's essentially what we want is for... can you see the screen there okay?

**Donough Regan:** Yep.

**Ross White:** So, thank you for a lively engine to be compatible for a combined bet. I think just the confusion I have is, like, what are we getting in Milestone 2 versus 4 there? Yeah, so I guess, like, aside from, obviously, just extending it to work for the EMF and OBB combined, but just to actually outline those requirements, I'm just a little bit unclear for Milestone 4 specifically.

**Donough Regan:** Yeah, so they're... the way they're arithm, it's hard to...

**Ross White:** I don't know how these, like, I certainly didn't phrase these like this, so I'm not sure how... yeah. But essentially what it is, Dona, is, like, this is... Yeah, so to cap... to cap things the way we do for today, and then the sec... second one is to, Yeah, apply the... apply the actual max cap, or max, wage or value manually if you want.

So we can... I'll change the wording here, that's fine, but just... Yeah, so... I guess, like... sorry, go on.

**Donough Regan:** So, sorry, which one is the max winning, Scott? Like, the max winning.

**Ross White:** Oh, yeah, yeah.

**Donough Regan:** So that's the top one.

**Ross White:** Yeah.

**Donough Regan:** Yeah, so there's... that one is, Because that's not the liability, but, like, the max… so the top one is the thresholding, and the bottom one is the max winnings cap. Is that...

**Ross White:** Yeah, I think so. It is unclear, but essentially they're, yeah, they're the two things that we need, so we can probably just change the wording on this. I'll have a look at that, so…

**Donough Regan:** Okay, so, Like, the threshold on the liability engine would work the same as today, but it doesn't work down to singles level.

**Ross White:** Yeah, but that's gonna be Milestone 5 anyway.

**Donough Regan:** That's Milestone 5's, yeah. So that will just work, the top button, that's… that… If I'm understanding it correctly.

**Ross White:** I'm sorry, it'll work because of what we're doing in Milestone 2, right?

**Donough Regan:** Yeah.

**Ross White:** Okay.

**Donough Regan:** Yeah, exactly. And then the… the other one, which, It's so dirty. Expression and choice display… there's just multiple things wrong, like, we don't suspend a choice, but, Just a lot of things wrong with the phrasing.

**Ross White:** Again, I don't know where this phrasing came from, but…

**Donough Regan:** To be honest, I'm not… that one is… the phrasing is too far off, I mean, I'm not, like, I don't even… does this mean that we applied the max winnings? the max stake, and then you just wouldn't be able to… have the bet, I…

**Ross White:** Yeah, no, to me, this is… this should be, like, just the automated thresholds, like, where… yeah, you're changing the max stake to zero, the same way it works today, if you hit…

**Donough Regan:** Yeah, so neither of these involves any work.

**Ross White:** Yes, this is what confused me a little bit, like, so not sure then where these estimates would have come from. We probably need to check that with Tiago, I'd say.

**Miguel Gomes:** Look, sorry, I don't know exactly what has been done in the past, but from what I'm understanding, Donna, you're saying that this was already… these two are already delivered on Milestone two, is it?

**Donough Regan:** Well, they're already delivered today, like, the max winnings cap applies this bet level, so it doesn't care whether it's OBP or EMS. So, like, it's either the max winnings gap, or it's the threshold, the 5 million threshold that applies in the liability engine. And again, like, just from Milestone 2… That would be done today, so… perhaps it's just, an indication that, like. Onto that flow, we have to be able to use, selections and choices together. So you need a single endpoint to capture both of those. Which, maybe that's a small piece of work. I think we're covering it today, but there's some single endpoint stuff that needs to be covered. Which is probably a small, which might fall into the Amount of time that was suggested there. Sorry, Ross, I wish I could be more out, but…

**Ross White:** No, no, no, it's not, like, I just, to be honest, it is one, like, for, like, for the last few weeks, I was looking, like, at Milestone 4, and I was like. Yeah, just not really clear on what's actually required, if anything, here, if we're doing this work for Milestone 2. So, yeah, maybe it's as simple as that. Maybe we just need to double-check with Tiago then, On that one, Miguel?

**Miguel Gomes:** Sure thing, and just for me to understand if I get this straight, so this… should be for us to have a single endpoint to address both selections and expressions simultaneously. And we are under the impression that this was delivered, or is being delivered today, under Milestone 2, is it?

**Ross White:** Yeah, yeah, because it boils down to what we have for Liability Engine is essentially, yeah, like. to replicate how it works for DMS.

**Miguel Gomes:** Okay, and we have changed the wording there. Do we need to align with someone else besides Tiago?

**Ross White:** No, I don't think so, there's no, like, dependencies here.

**Miguel Gomes:** Okay, so for that first one, I can check with Tim.

And then for the second one, is it the same?

**Ross White:** No, so the sec… yeah, well, sorry, the second one, Don is also saying it's like, yeah. Oh, let's see…

**Miguel Gomes:** And sorry, guys, I'm just being dropped here. And I want to be sure that I fully understand where we are with the liability engine. So these two requirements, the first one was to make sure that we can cap the max stake, so basically whenever we build a number of bets. for a given expression, let's just say that the expression is player X, when we have an amount of, I don't know, 5 millions on using the expression Blair X, we want to be able to cap the max stake, and we want to be able to block new wagers, right? That is the first.

**Ross White:** Well, yes, but an important note there, that in your example, is just as straight, so we won't have that until Milestone 5. But it would be, like, if you were to do player A to score 10 plus points with player B to have 15 plus points with player C to have 10 rebounds. And that exact combination hits the threshold. 

**Miguel Gomes:** Okay, okay, got it. But just a question regarding that one. Are we talking about, choices as well, or just the expression? So, we are putting the limitation if the user uses a certain selection or a certain expression. So, it's regardless of the choice

That he makes, right?

**Donough Regan:** So, it can be selections, it's a pure EMS, or a choice, but in this case, it's not the choice itself, we're using aspects of it, so it's going to be the outcome definitions, the.

**Miguel Gomes:** Okay, exactly. So, basically, we would need to have a system where we can, let's just say, player X to score more than one goal, player A to have more than one yellow card. these two would both… let's just say that the first one is OBP, the second one is a selection. These two would have, controls on… just on the expression level and the selection level, regardless of the choice and the result that it selects, right?

**Donough Regan:** So the liability ending today, if you… if you go beyond… for… for a stated combination, if you go beyond it, you have to be able to manage it, so that's… it doesn't really matter where they come from, it's just, you've stated this is… this is the particular combination that you've taught things up on, and if you exceed it, you're able to adjust that threshold on the liability engine UI. That's all it's saying.

**Miguel Gomes:** Okay, okay, but the variables that we would monitor under this example would be expressions that have that player. And selections that have a number of.

**Donough Regan:** Yeah, so it's a mixture.

**Miguel Gomes:** Yeah.

**Donough Regan:** be able to capture a mixture, yeah.

**Miguel Gomes:** Okay. Got it, thanks. And for the second one, we have… we have ability for restoring to use expressions in choices to suspend liabilities.

**Ross White:** Yeah, well, no, what you're actually doing is you're just updating the max stake on a particular combination.

**Miguel Gomes:** Okay.

**Ross White:** Yeah, okay. I think, I think this should be hopefully straightforward, probably just some needless confusion, but, yeah, maybe we just check… Just check those estimates with Tiago, I would say. Just make sure that they're clear, and then we'll probably just have to… Create the, create the tickets then, etc, just to formalize that work, Miguel?

**Miguel Gomes:** Yeah, just to align both of these requirements, we're under Milestone 2, we have the NAPIC, just to help Tiago to look for…

**Ross White:** Yeah, I can stand on, yeah.

**Miguel Gomes:** Thanks, Ross.

**Ross White:** Cool. Anything else?

**Miguel Gomes:** Regarding the first one, sorry, the kill switch one.

**Ross White:** Yeah, I… well, that one should just be kind of straightforward. Again, we probably… we do still need to create the ticket, I would say, but Yeah, again, that's just, we have an automated kill switch today, so we just need to ensure that that works for, I'll be feedbacks as well.

**Miguel Gomes:** But for this one, we have no indication that this might already be delivered on…

**Ross White:** This one definitely isn't, hasn't been delivered. Or even captured.

**Miguel Gomes:** Okay, and just for me to create this work, because I've never seen or never work with the automated kill switch. I can fetch the current status of the automated kill switch, but can I have someone that helps me, show me the lay of the land, just for me to understand how we currently are? Okay.

**Ross White:** Yeah, I can go through that with you.

**Miguel Gomes:** Thanks, Ross.

**Ross White:** Cool. I'm happy to leave it there, then.

**Miguel Gomes:** Yeah, I'm going to touch base with Tiago, and then I'll ping you, Ross, for us to have 15 minutes, if you can, to show me the ultimate.

**Ross White:** Perfect. Perfect.

**Miguel Gomes:** Okay, good. Tell me if I can be of any more help.

**Ross White:** Yeah, we'll, we'll pick that up then. Alright.

**Donough Regan:** Okay, thanks for…

**Ross White:** Thank you, cheers.

**Miguel Gomes:** Thanks, guys.

</details>
