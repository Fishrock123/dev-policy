## Contributing

### Collaborators

The Node.js project is maintained by individual Collaborators. The Technical Steering Committee (TSC) membership consists of key Collaborators who have demonstrated both technical expertise critical to the ongoing maintenance and evolution of the project and a long term commitment to driving the project and community forward. (TODO: Need to document the process by which Collaborators are nominated to the TSC)

Individuals making ongoing significant and valuable contributions to the project can be nominated as Collaborators by TSC members. Once the nomination is approved by the TSC, the invitation to become a Collaborator is extended to the individual. The invitation must include a copy of the project Developer’s Certificate of Origin (DCO, see below). Assuming the individual accepts the invitation, they are granted commit-access to the project. 

Nominations for Collaborator Status happen through the typical TSC decision making process. That is, to nominate one or more Collaborators, an issue containing the names of all collaborators being nominated is created and put on the TSC meeting agenda. The issue is approved or rejected following the same Consensus Seeking Process used for any other issue or PR.

Individuals can self-nominate the TSC for Collaborator status by submitting an issue requesting to be put on the TSC meeting agenda. In order to be considered however, such self-nominations must be sponsored by an existing TSC member, after which it follows the same process as above. To sponsor a nomination, the TSC member must indicate consent within the issue text or associated comment thread.

Collaborators can be nominated to become members of the TSC following the same nomination and approval model. However, Collaborators cannot nominate themselves for TSC membership.

### Consensus Seeking Process

Like the TSC governance, all issues and pull requests follow a Consensus Seeking decision making model as described in the Project TSC Charter.

Collaborators may opt to elevate significant or controversial modifications, or modifications that have not found consensus to the TSC for discussion by assigning the tsc-agenda tag to a pull request or issue. The TSC should serve as the final arbiter where required.

If full TSC review is not required, and there is a Working Group whose charter covers the subject of the issue or pull request, then it can be tagged using a Working Group specific tag (to be selected by the Working Group itself). In such cases, the WG can decide whether to further elevate the item to the full tsc (using the *tsc-agenda* tag) or decide on the matter itself. 

In either case, issues or PR’s for which additional review is required should have the review-required tag added and removed only after either the Working Group or TSC decision has been made.

### Accepting Modifications

A “Contribution” to the project is any work that is voluntarily submitted to the project. These include not only source code in the form of bug fixes, code improvements, new functions, etc, but contributions to documentation, design etc that are intended for the overall improvement of the project.

Contributions to the Project are made on a collaborative basis. Any individual with a GitHub account may propose a contribution by submitting a Pull Request (PR). Contributions must be evaluated by project Collaborators with sufficient expertise and approved using the Consensus Seeking Process described above. 

Pull Requests submitted by individuals who are currently not Collaborators must be sponsored by an existing Collaborator before the PR will be considered. The sponsoring Collaborator becomes responsible for the PR.

Before any Pull Request can be accepted into the project, it must be signed-off by at least two Collaborators (the submitting / sponsoring Collaborator and one additional Collaborator with sufficient expertise to evaluate the specific PR). 

If any Collaborator feels that a particular PR is controversial and needs to be reviewed further, the Collaborator can tag the PR with a *review-required* tag in addition to attaching either the tsc-agenda tag (to put the PR on the TSC agenda) or a Working Group specific tag to indicate that the PR requires review from a specific Working Group. PR’s with the review-required tag cannot be accepted into the project until the review-required tag has been removed following either a WG or TSC review following the Consensus Seeking Model. (Note: The *review-required* tag is not currently within the io.js or node.js process. It is an addition suggested by @jasnell).

Specific Collaborators can be requested to review any PR by using an *@-mention* either within the PR text itself or the associated comment stream.

Collaborators sign off on a PR by explicitly stating their approval in the PR text or associated comment stream. If a Collaborator is unsure about the modification or is not prepared to take full responsibility for the change, they should defer to another Collaborator. 

Before landing a Pull Request, sufficient time should be given to receive input from other Collaborators. Specifically, at least 48 hours during the typical working week and 72 hours over weekends should be given to account for international time differences and work schedules. Trivial changes (e.g. those which fix minor bugs or improve performance without affecting API or causing other wide-reaching impact) may be landed after a shorter delay. 

For high priority changes that address security vulnerabilities, a shorter review period may be necessary depending on the nature of the change and severity of the issue. It is recommended that the TSC establish a special Security Working Group of Collaborators with recognized security expertise who can be tasked with reviewing security related Pull Requests.

Where there is no disagreement amongst Collaborators, a PR may be landed given appropriate review. Where there is disagreement amongst Collaborators, consensus should be sought if possible. The lack of consensus may indicate the need to elevate discussion to the either the full Working Group or TSC for resolution (see below).

All Pull Requests that either (a) fix bugs or (b) introduce new functionality require at least one test case demonstrating the defect or validating the intended functionality. For bug fixes, the test should fail before the change, and pass after the change. Pull Requests for changes intended to improve performance should contain a test case demonstrating the performance impact. The test should demonstrate improved performance after the change is applied.

### Branches

The Project source repository will be organized into a single *master* branch and multiple Release branches. All modifications intended for the current major release line must be made to the master branch. Modifications to Release branches are limited to bug fixes, with priority given to PR’s that address specific security vulnerabilities. Oversight of the Release branches belongs to the Long Term Support (LTS) Working Group. No PR can be landed within a Release Branch without approval from the LTS Working Group.

### Involving the TSC

Collaborators may opt to elevate pull requests or issues to the TSC for discussion by assigning the *tsc-agenda* tag. This should be done where a pull request:

* has a significant impact on the codebase,
* is inherently controversial; or
* has failed to reach consensus amongst the Collaborators who are actively participating in the discussion.

The TSC serves as the final arbiter where required but it is expected that most changes reach a lazy consensus are merged without TSC intervention.

### Landing Pull Requests

Always modify the original commit message to include additional meta information regarding the change process:

* A Reviewed-By: Name <email> line for yourself and any other Collaborators who have reviewed the change.
* A PR-URL: line that references the full GitHub URL of the original pull request being merged so it's easy to trace a commit back to the conversation that lead up to that change.
* A Fixes: X line, where X is either includes the full GitHub URL for an issue, and/or the hash and commit message if the commit fixes a bug in a previous commit. Multiple Fixes: lines may be added if appropriate.

See the commit log for examples such as this one if unsure exactly how to format your commit messages.

Additionally:

* Double check PR's to make sure the person's full name and email address are correct before merging.
* Except when updating dependencies, all commits should be self contained. Meaning, every commit should pass all tests. This makes it much easier when bisecting to find a breaking change.

### Issue and Pull Request Tagging

All issues and pull requests should be tagged with their respect feature areas. This helps organize issues and makes it easier for Collaborators to keep track of the items most relevant to them.

The labels *discuss*, *meta*, *future*, and *ideas* are used to label issues that are not bugs or features requests. 

The *help-wanted* tag is used to draw attention to issues and pull requests that need contributions.

When a pull request is not ready to merge and is still be iterated on and reviewed it should have the *in-progress* tag applied.

The *semver-minor* and *semver-major* tags are used for pull requests that will cause a version iteration other than patch once released.

The *tsc-agenda* tag is used to elevate items to the next TSC meeting. TSC meeting notes and announcements should have the *tsc-meeting* tag.

The *review-required* tag is used to indicate that a pull request cannot be landed without a decision from either a Working Group or the TSC.

## Release Process

### Release Branches

The *master* branch is the current major release branch. Most pull requests are sent to this branch and it is the default repo branch.

Before a new major release master is branched for LTS releases of the prior major. Example: `1.x`, `2.x`.

Additionally there are branches for stable release lines prior to 1.0 of minor versions. Example: `0.8.x`, `0.10.x`, `0.12.x`.

All release branches other than master are managed by the LTS Working Group and fall under their LTS release policy.

### Release Versioning

#### Patches

Patch releases are defined as bug, performance, and security fixes. They do not change or add any public interfaces. They do not change the expected behavior of a given interface. They are meant to correct behavior when it doesn't match the documentation, without also introducing a change that makes seamless upgrades impossible.

#### Minors

Minors are the addition and refinements of APIs or subsystems. They do not change APIs or introduce backwards compatible breaking changes. These are mostly completely additive releases.

#### Majors

Majors contain changes in behavior that could potentially break code that worked in prior releases. 

### Release Process for Master

Releases should not contain too many code changes and if the rate of code changes is high then it should correspond to an increase in the rate of releases. It is expected that there should be about one release per week.

Master must pass a full CI test run prior to release.

If master contains changes which are tagged *semver-minor* then the release should bump the minor version otherwise it is a patch release.

## Repository Reconciliation Plan

There are currently release lines in both node.js and io.js. Starting at the point from which io.js was created, the two repositories have diverged significantly. Bringing the two repositories back together under the Foundation TSC will not happen immediately.

```
                        now
       (io.js)    v1.6   :  v1.7    v1.x
          |         |    :    |       |      
 v0.10.x  /--------------:-----------------\   Node.js 2.0
____|____/               :                  \______|_____
         \               :                  /
          \--------------:-----------------/
          |         |    :     |       |
       (node.js) v0.12.x :  v0.13.x  v0.14.x
```

At the time of this writing, the current Node.js release is v0.12.2. The current io.js release is 1.6.3. 

Upon Foundation launch, both projects will come together under a single TSC, but the two distinct release lines will continue independently for the near term. Each subsequent release (“interim releases”) for each project should incrementally bring the two code bases closer together, allowing them to eventually merge back into a single Node.js 2.0 release line. For purposes of managing each separate release line, the TSC will charter an io.js WG and a node.js WG, each responsible for their respective release lines. The membership for each release line WG will be the current membership of each of the two separate projects TSC’s.

To avoid introducing unnecessary problems for users, the interim releases should not overlap versions. All prior versions of both io.js and node.js should be preserved. The interim Node.js releases will remain the v0.x version stream. Interim io.js releases will continue to follow their existing semver strategy. If Interim changes in io.js require a major version bump to 2.x, the first release of the Converged Project would be the next major version number (3.0). The Converged Project will use semver for release versioning. 

To facilitate and oversee the Convergence effort, the TSC will charter a Convergence Work Group. This WG will ensure that appropriate steps are being made in each of the two release lines to bring the projects back together. The Convergence WG will work directly with both release line WG’s. As soon as the release lines converge, the charters for the separate release line WG’s and the convergence WG will expire, and responsibility for the continued evolution of the converged release line will be with the project TSC itself. The initial membership of the Convergence WG will be a subset of members from each of the two release line WG’s. 

For the Converged Project, a new Github organization owned and managed by the Node.js Foundation will be created. Once the new Github organization is established, ownership of the existing iojs/io.js and joyent/node repositories should be transferred. From there, the Convergence WG will be responsible for determining the exact next steps for creating the Converged repository.

The Converged repository must contain release branches for all prior stable lines from both release lines.

### Long Term Support WG

All Interim and Post-Convergence Releases other than current automatically shift into the responsibility of the Long Term Support working group. The specific approach for determining the LTS strategy for specific releases is entirely in the LTS WG’s hands. 

TODO: Form LTS WG and create LTS policy.

## Developer's Certificate of Origin 1.0

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I have the right to submit it under the open source license indicated in the file; or

(b) The contribution is based upon previous work that, to the best of my knowledge, is covered under an appropriate open source license and I have the right under that license to submit that work with modifications, whether created in whole or in part by me, under the same open source license (unless I am permitted to submit under a different license), as indicated in the file; or

(c) The contribution was provided directly to me by some other person who certified (a), (b) or (c) and I have not modified it.

## A Few Open Questions

1. What about things like http_parser and libuv? Does it make sense to see about bringing each into the foundation as their own projects?
2. What about all the other repos under iojs/* and joyent/*, which of those will move over to the foundation?
3. The Node.js TC is working to introduce the notion of Release Candidates into the release cycle. It's not yet clear how this lines up with the semver release strategy used by io.js. This will need to be explored.
4. The Node.js TC has recently adopted a priority tagging strategy (e.g P-1, P-2, P-3, P-4) to indicate the priority of a given issue or PR. It's not yet clear how and if this will fit into the larger project strategy.