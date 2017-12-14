- Start Date: (fill me in with today's date, YYYY-MM-DD)
- RFC PR: (leave this empty)
- Ember Issue: (leave this empty)

# RFC Process Update

## Summary

Introduce the idea of Core Champion to the Ember.js RFC process, merge Ember.js and Ember CLI processes and repositories,
and update process to ease authoring of RFCs for core projects, especially cross-project ones.

## Motivation

> Why are we doing this? What use cases does it support? What is the expected
outcome?

The RFC process is the backbone of Ember.js development.
Community empowerment.
Diversity of thought/responsibilities/use cases.

### RFC Lifecycle

RFCs can languish. Two ways to address this, FCP to Close and Core Champion.

FCP to close [research Rust wording] does not necessarily mean that the idea is rejected out-right.
The idea might need further iteration [named blocks], might be too early [glimmer components?], the direction of the project might have changed meanwhile [routable components [there are others]], or the scope of the RFC should be reduced [let rfc].

Core champion.

Reduce confusion of having two repositories.
Sometimes RFCs span multiple projects and it isn't clear how to communicate that, or where it would go.

## Detailed design

> This is the bulk of the RFC. Explain the design in enough detail for somebody
familiar with the framework to understand, and for somebody familiar with the
implementation to implement. This should get into specifics and corner-cases,
and include examples of how the feature is used. Any new terminology should be
defined here.

* Add Core Champion to process
* Add FCP to close
* Add front matter to RFCs
    * teams array
* Merge ember-cli/rfcs
    * remove active/complete concepts
    * keep names as there should be no clash

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

> Why should we *not* do this? Please consider the impact on teaching Ember,
on the integration of this feature with other existing and planned features,
on the impact of the API churn on existing apps, etc.

> There are tradeoffs to choosing any path, please attempt to identify them here.

## Alternatives

> What other designs have been considered? What is the impact of not doing this?

> This section could also include prior art, that is, how other frameworks in the same domain have solved this problem.

## Unresolved questions

> Optional, but suggested for first drafts. What parts of the design are still
TBD?
