- Start Date: (fill me in with today's date, YYYY-MM-DD)
- RFC PR: (leave this empty)
- Ember Issue: (leave this empty)

# RFC Process Update

## Summary


Introduce the idea of Core Champion to the Ember.js RFC process, merge Ember.js and Ember CLI RFCs repositories,
and add metadata to make cross-project RFCs easier.

## Motivation

> The Ember project placed a high value on community since the beginning.
> This permeates all decisions related to the project, specifically the RFC process.
> The RFC process is the backbone of Ember.js development.
> Community empowerment.
> Diversity of thought/responsibilities/use cases.
> RFCs can languish. Two ways to address this, FCP to Close and Core Champion.
> Core champion.
> Reduce confusion of having two repositories.
> Sometimes RFCs span multiple projects and it isn't clear how to communicate that, or where it would go.

The Ember project has taken since its inception a communal approach to developing Open Source.
Inspired by Rust, Ember implemented a Request For Commits (RFC) process with the intent to involve the community in discussing the future of the framework. It has been proved highly successful, with community members both improving Core proposals by highlighting unaddressed problems and providing feedback, as well as making proposals themselves. Other projects like React also adopted an RFC process, lending external validation to this idea.
After having been involved with the RFC process for some time, and from feedback from the community, some issues with the current implementation of the process have been noted. These issues should be addressed, in order to make the process as easy to take part as possible, and as transparent as possible for everyone involved.

### Confusion about emberjs/rfcs and ember-cli/rfcs

The Ember project currently has two separate RFC processes for Ember.js and Ember CLI.
This split prompted two more prominent problems.

The first is that there are twice the places to keep track of RFCs.
This makes it significantly harder for community members to track progress on ongoing RFCs.

The other problem is that the RFC processes have diverged.
This makes it confusing to know where to submit a certain RFC, especially if the RFC touches on both projects.
The current solution is to submit two RFCs, each one with the more relevant details for the respective project.

### Unclear how to submit an RFC that isn’t for emberjs or ember-cli

Rust has RFCs for documentation, website, internals, tools.
We only have emberjs and ember-cli due to them having been implementesed separately.
This makes it so that a potential contributor does not know where to submit a proposal.

### Lingering RFCs

The emberjs/rfcs repository currently has [X issues and Y PRs] open. Of these, only a relatively small percentage has been active in the recent past.
We have kept PRs and issues open so people could more easily find the discussions, but it has also given a negative feeling of staleness.
RFCs linger open for ages. No feedback from the Core team.

FCP to close [research Rust wording] does not necessarily mean that the idea is rejected out-right.
The idea might need further iteration [named blocks], might be too early [glimmer components?], the direction of the project might have changed meanwhile [routable components [there are others]], or the scope of the RFC should be reduced [let rfc].
FCP to inactive.

## Detailed design

To address the issues raised in the “Motivation” section, I will propose changes to the current process.

### Implement Core Champion

From ember-cli/rfcs

### Augment FCP process

Learning from Rust once again, have a Final Comment Period (FCP) to close a proposal.
No “shame” in being rejected. Named blocks too several attempts.

### Implement tags as frontmatter

This allows the RFC to specify which projects will be affected by it. To be accepted, a member of each tagged team must approve the RFC.

### Merge emberjs/rfcs and ember-cli/rfcs

- Remove active/completed concepts from ember-cli/rfcs
- Introduce Core Champion to emberjs/rfcs
- Tag current RFCs
- Bring all merged ember-cli/rfcs into the text folder of emberjs/rfcs.

## How We Teach This

> What names and terminology work best for these concepts and why? How is this
idea best presented? As a continuation of existing Ember patterns, or as a
wholly new one?

> Would the acceptance of this proposal mean the Ember guides must be
re-organized or altered? Does it change how Ember is taught to new users
at any level?

> How should this feature be introduced and taught to existing Ember
users?

## Drawbacks

### Adjustment period

There are active RFCs in ember-cli/rfcs. Moving these discussions would be onerous, so they should be kept there until completion, and no new RFCs accepted.

### Permalinks to ember-cli/rfcs proposals

Moving the RFC files from ember-cli/rfcs (active or completed) to emberjs/rfcs can be seen as a breaking change, and could lead to someone linking to ember-cli/rfcs and then the RFC being updated in emberjs/rfcs. However, ember-cli/rfcs already suffers from a linking problem due to the active/completed folders, as RFCs need to be moved from one to the other even after being accepted.
This could be mitigated by introducing a warning in the RFC text directing people to the new source.

## Alternatives

To be determined.

## Unresolved questions

To be determined.

----------

## Glossary

- RFC: Request For Comments. Process by which a proposal is discussed by the community and then approved by an Ember team.
- FCP: Final Comment Period. Period of one week at the end of which an RFC is to be accepted or rejected by an Ember team. Extended in periods of one week if new concerns are raised.
- Ember Team:  The official core team and subteams represented in the [website’s Team page](https://emberjs.com/team).
