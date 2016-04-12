# [2016-04-12] RFC Process
## Summary
Many changes, including bug fixes and documentation improvements can be
implemented and reviewed via the normal GitHub pull request workflow. But some
ideas are substantial and require more design process. The "RFC" (request for
comment) process is intended to provide a centralized point of iteration before
implementation occurs.

Some ideas are substantial, and require a bit more design process. The "RFC"
(request for comments) process is intended to provide a consistent and
controlled path for ideas to be implemented, both to provide a backlog of
decision making and as a reference for implementations.

## Motivation
Any one person has more ideas than they can implement. Implementing new ideas
can be costly if the constraints aren't considered beforehand. Sometimes ideas
are greater than a single project, and cannot be specced out on the repo
itself. RFCs are written to iterate on ideas before they are built.

## Detailed design
Every time a large change, significant package or set of packages is built, it
should probably be specced out as an RFC first. That way a backlog of ideas is
created, which can be refered back to in later stages. An RFC should be created
using the script in `bin/create-rfc`.

Every RFC should have a title which starts with the date as `[YYYY-MM-DD]`,
followed by the title of the RFC.

The following headings are recommended for every RFC:
- __Summary:__ One paragraph explaining what the RFC does
- __Motivation:__ Explain why this RFC is written
- __Detailed Design:__ Bulk of the RFC. Explain in enough detail that someone
  with prior knowledge can understand. Cover corner cases and include examples.
- __Alternatives:__ What other designs have been considered? What is the impact
  of not adding this?
- __Unresolved questions:__ Which parts of the design are still TBD?
- __See Also:__ Links to prior art

Every RFC must be submitted as a pull-request before being merged.

When an RFC is succesfully merged, it can be acted upon. In the case of adding
a new feature to an existing code base, it should be clear enough to base tests
on. In the case of a new project, the initial scope of the project should be
clear.

## Alternatives
Often decisions are made in person. No formal process is established, and
people jump directly to implementation. I've found there's often a lot of
miscommunication, unless a summary was established. It also does not work
asynchronously, as people need to discuss things at the same time. It also
doesn't necessarily involve a single person taking charge, causing meetings to
be inefficient.

GitHub issues are often used for design process, but as discussion grows it can
be hard to keep track of. By creating, and updating an RFC the result of
discussion can be crystalized and only the result of lengthy threads is
preserved.

Similar to RFCs Gherkin features can sit on high level. Though where they
differ is that an RFC goes into the _why_ of a decision, whereas a Gherkin
feature is only concerned with the _what_. It would not seem unnatural to
progress from an RFC to Gherkin test.

Wikis act as living documents, usually keeping only tailing the latest. RFCs
are a backlog of ideas that is discussed and can either be rejected or
accepted.

## Unresolved questions
- When should an RFC be created? What is the threshold for when an RFC is the
  right method?
- Do RFCs have practical value if there's only a single contributor?
- Should rejected RFCs be added too?

## See Also
- https://github.com/rust-lang/rfcs
- https://github.com/jbenet/random-ideas
