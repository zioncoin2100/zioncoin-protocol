# Zioncoin Ecosystem Proposals (SEPs)

## SEP Tracks
* **Informational** — A SEP on the `Informational` track is one that is open to adoption by the
  ecosystem, but has not been formally standardized by SDF, and is not endorsed by SDF for
  adoption. Typically a SEP can start as `Informational` to gain traction within the ecosystem
  before moving to the `Standards` track.
* **Standard** — A SEP on the `Standards` track is one that aims for formal standardization and
  endorsement by SDF for adoption. Typically a SEP Standard has a higher bar towards acceptance,
  and it requires approval by 2 SDF members of the SEP Team.

## SEP Status Terms
* **Draft** - A SEP that is currently open for consideration and actively being discussed.
* **Awaiting Decision** — A mature and ready SEP that is ready for approval by the SEP
  Team. If enough the approval requirements are met by SEP team members, the SEP will move towards 
  `FCP`. Otherwise, it'll regress to a `Draft`.
* **FCP** — A SEP that has entered a Final Comment Period (FCP). After one week has passed, during
  which any new concerns should be addressed, the SEP's status will become `Active` or `Final`,
  depending on the content of the SEP.
* **Active** - An actively maintained SEP that is intended for immediate adoption by the entire
  ecosystem by its author(s), and if it is a Standard, by SDF as well. Additional updates may be
  made without changing the SEP number.
* **Final** - A finalized SEP that is intended for immediate adoption by the entire
  ecosystem by its author(s), and if it is a Standard, by SDF as well. A final SEP should only be
  updated to correct errata.

### Additional Statuses
* **Rejected** - A Standards SEP that has been formally rejected by the SEP Team, and will not be
  implemented.
* **Superseded: [New Final SEP]** - A SEP that which was previously final but has been superseded
  by a new, final SEP. Both SEPs should reference each other.

## List of Proposals

| Number | Title | Author | Track | Status |
| --- | --- | --- | --- | --- |
| [SEP-0001](sep-0001.md) | zioncoin.toml specification | SDF | Standard | Active |
| [SEP-0002](sep-0002.md) | Federation Protocol | SDF | Standard | Final |
| [SEP-0003](sep-0003.md) | Compliance Protocol | SDF | Standard | Active |
| [SEP-0004](sep-0004.md) | Tx Status Endpoint | SDF | Standard | Final |
| [SEP-0005](sep-0005.md) | Key Derivation Methods for Zioncoin Accounts | SDF | Standard | Final |
| [SEP-0006](sep-0006.md) | Anchor/Client Interoperability | SDF | Standard | Active |
| [SEP-0007](sep-0007.md) | URI Scheme to facilitate delegated signing | Interzioncoin | Standard | Final |
| [SEP-0008](sep-0008.md) | Regulated Assets | Interzioncoin | Standard | Final |
| [SEP-0009](sep-0009.md) | Standard KYC / AML Fields | SDF | Standard | Active |
| [SEP-0010](sep-0010.md) | Zioncoin Web Authentication | Sergey Nebolsin, Tom Quisel | Standard | Active |
| [SEP-0011](sep-0011.md) | Txrep: Human-Readable Low-Level Representation of Zioncoin Transactions | David Mazières | Standard | Active |
| [SEP-0012](sep-0012.md) | Anchor/Client Customer Info Transfer | Interzioncoin | Standard | Active |
| [SEP-0020](sep-0020.md) | Self-verification of validator nodes | Johan Stén | Standard | Active |

### Draft Proposals

| Number | Title | Author | Track | Status |
| --- | --- | --- | --- | --- |
| [SEP-0013](sep-0013.md) | DEPOSIT_SERVER proposal | @no, @ant, @manran, @pacngfar | Informational | Draft |
| [SEP-0014](sep-0014.md) | Dynamic Asset Metadata | OrbitLens, Paul Tiplady | Standard | Draft |
| [SEP-0015](sep-0015.md) | Attachment Convention | Interzioncoin | Standard | Draft |
| [SEP-0016](sep-0016.md) | Account Transfer Permissionless Payment Protocol (@p2p) | Jeremy Rubin | Standard | Draft |
| [SEP-0017](sep-0017.md) | Issuer account funding protocol (CAP-13 Based) | Tom Quisel | Standard | Draft |
| [SEP-0018](sep-0018.md) | Data Entry Namespaces | Mister.Ticot | Standard | Draft |
| [SEP-0019](sep-0019.md) | Bootstrapping Multisig Transaction Submission | Paul Selden, Nikhil Saraf | Standard | Draft |
| [SEP-0021](sep-0021.md) | On-chain signature & transaction sharing | Mister.Ticot | Informational | Draft |
| [SEP-0022](sep-0022.md) | IPFS Support | Samuel B. Sendelbach | Informational | Draft |

# Contribution Process

The Zioncoin Ecosystem, like most software ecosystems in the world, continues to evolve over time to
meet the needs of our network's participants and to drive technology forward into new territory.

Unlike Zioncoin's Core development (CAPs), Zioncoin's Ecosystem Proposals are intended to be a more
dynamic way of introducing standards and protocols utilized in the ecosystem that are built on top
of the Zioncoin Network. It attempts to take a more lightweight process for approval, and much of
its process is inspired by the [IETF][ietf].

Before contributing, consider the following:

- Choose a track to propose your idea on. The bar for accepting an `Informational` SEP is much
  lower than one for a `Standard`, and allows you to promote the SEP independently to gain feedback
  and traction before creating a Standard out of it.
- Gather feedback from discussion on the dev mailing list and other forums, and utilize it to begin
  a draft proposal.
- Follow the proposal process listed below. If you're having difficulty moving the proposal
  forward, talk to the buddy that's assigned the SEP; they'll often have guidance on how to move
  things forward, as well as feedback regarding feasibility and how the proposal does or does not
  align with the Zioncoin Network's goals.

## SEP Process
### Pre-SEP (Initial Discussion)
Introduce your idea on the [zioncoin-dev mailing list](https://groups.google.com/forum/?utm_medium=email&utm_source=footer#!forum/zioncoin-dev)
and other community forums dedicated to Zioncoin.

- Make sure to gather feedback and alternative ideas — it's useful before putting together a
  formal draft!
- Consider contacting experts in a particular area for feedback while you're hashing out the
  details.

### Creating a SEP Draft
Draft a formal proposal using the [SEP Template](../sep-template.md), and submit a PR to this
repository. You should make sure to adhere to the following:

* Use the following format for the filename of your draft:
  `sep_{github_username}_{shortsha256sum}.md`
  * `shortsha256sum` is defined as the first 8 characters of the SHA-256 checksum.
  * For example, a SEP by Github user `happycoder` with a SHA-256 checksum of `a200f73c`
    would be titled `sep_happycoder_b274f73c.md`.
* Make sure to place your SEP in the `ecosystem/` folder.

Finally, submit a PR of your draft via your fork of this repository.

#### Additional Tips
* If your SEP requires images or other supporting files, they should be included in a subdirectory
  of the `contents` folder for that SEP, such as
  `contents/sep_happycoder_b274f73c/`. Links should be relative, for example a link to an image
  from SEP-X would be `../contents/sep_happycoder_b274f73c/image.png`.

### Draft: Merging & Further Iteration
From there, the following process will happen:
* A SEP buddy is assigned and will merge your PR if you properly followed the steps above.
  * They'll rename the above files to the latest SEP draft number before merging in the PR.
  * They'll provide initial feedback, and help pull in any subject matter experts that will help in
    pushing the SEP towards a final disposition.
* You should continue the discussion of the draft SEP on the mailing list to gather additional
  feedback. We welcome any additional PRs that iterate on the draft.

### Draft -> Awaiting Decision -> Final Comment Period (FCP)
* When you're ready, you should submit a PR changing the status in the draft to `Awaiting Decision`.
* A SEP buddy is assigned from the SEP team. They'll provide any additional feedback, and help pull
  in any subject matter experts and SEP team members that will help in pushing the SEP towards a
  final disposition.
  * For the Informational Track, the SEP enters FCP when 2 members of the SEP Team approve the pull
    request.
  * For the Standards Track, the SEP enters FCP when 3 members of the SEP team approve the pull
    request, 2 of whom must be representatives of SDF.
  * The SEP buddy (the PR assignee) is responsible for including members of the SEP team who are
    subject experts on the SEP being discussed; however, you are free to pull in feedback without
    going through your buddy. The SEP buddy may also bring it up at an upcoming protocol meeting.
  * If any SEP has major concerns (typically around security) from a SEP Team or CAP Core Team
    member, the concerns must be addressed before moving it forward; otherwise, it will be set back
    to `Draft`, or if fundamentally broken, to `Rejected`.
  * It should take no more than 2 weeks to move a SEP out of `Awaiting Decision`.
* Once a SEP has been approved, it goes into FCP which is broadcast to the protocol meeting members
  along with the mailing list.

### FCP -> Active/Final
* If no major concerns are brought up, the SEP is marked as `Active` or `Final` by your SEP buddy:
  * If the SEP requires active maintenance, such as having an open schema, it should be marked at
    `Active`.
  * Otherwise, the SEP should be marked as `Final`.

## SEP Team Members

**SEP Team**: Tomer (SDF), Nikhil (SDF) Tom Q. (SDF), Johnny (SDF), orbitlens, David (SDF), Jed
(SDF)

[ietf]: https://ietf.org/
