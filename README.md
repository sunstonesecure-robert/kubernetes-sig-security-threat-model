# Overview and Goals

This was forked from a public release of materials created by the ControlPlane team: [kubernetes-for-soc]() which was used by a small group
of threat analysists acting within the charter of the Kubernetes sig-security to "refresh" and update the previous efforts to define a 
Kubernetes threat model.

This group met for several months to first review the previous threat model efforts and audits, and 3 of the members had participated in
the [2023 Kubernetes 3rd Party Audit]() effort and wished to expand on this effort and to add context to future efforts.

In addition to reviewing and incorporating ideas from the previous models to reflect newer features and threats, 3 additional goals 
were defined at the onset:

1. Produce a methodology for ongoing threat modeling by the Kubernetes project (and sub-projects), and not simply a point-in-time snapshot
   of the threat model. Document the process, inputs and outputs, examples and tools and explicitly discuss ongoing reuse
   for future users.
1. Explicitly consider insider and supply chain threats - for staff at the IaaS cloud hosts themselves, operators of self-hosted or cloud-hosted Kubernetes,
   as well as the repository owners and developers of supply chain components. The previous audits had explicitly scoped OUT insider threats and cloud host threats,
   and supply chain risks were only casually noted and not thoroughly considered. While this refresh does not aim
   to explicitly remediate any or all of these privileged and insider threats, a "zero trust" (lowercase, non-specific to vendors or frameworks)
   approach was scoped IN for this effort.
1. Explicitly align threats to a Risk-based compliance framework.
   This threat model aims to review specific Kubernetes design choices, operational features and security capabilities
   within the context of regulatory and compliance risks. Kubernetes is no longer a niche platform, and is now widely adopted
   by enterprises and organizations large and small, and that these organizations must adhere to a growing body of local, provincial/state, national
   and international regulatory oversight. A system built on or using Kubernetes must adhere to these highly complex, and often contradictory
   regulatory requirements. Or, where Kubernetes is deemed succeptible to compliance risks, document the specific risks users are inheriting when relying on
   Kubernetes. This effort aims to explicitly map the designs, components, capabilities, runtime behavior, and configuration options
   implemented in Kubernetes to specific risks called out by regulatory frameworks, initially as exemplified
   in NIST 800-53 Revision 5. We encourage future contributors to add more frameworks and risks over time.
   Note that this is NOT an effort to map specific NIST 800-53 Revision 5 controls to a specific choice
   of Kubernetes deployment or configuration; it is merely an attempt to characterize how Kubernetes may or may
   not be succeptible to specific compliance risks.

## This Is **Not**

- This is **not** an audit.
- This is **not** a code review or fuzzing exercise.
- This is **not** a penetration test or assessment.
- This is **not** meant as a point-in-time threat model report that becomes stale quickly.
- This is **not** a guarantee or warranty of the security, privacy, safety, integrity, resiliency of Kubernetes or any data
  hosted by a Kubernets cluster, in the context of any attacker or malicious actor action, user or operator mistake.

## This Is

- This **is** a collaborative and community effort to increase knowledge through open documentation and open source code.
- This **is** a project that is expected to evolve and gain from others' inputs.
- This **is** meant to expand the responsible use of Kubernetes and serve the public good by surfacing threats and risks that all users
  and operators should carefully consider before designing any deployment of Kubernetes.
- This **is** meant to make future sig-security efforts and audits more documented and increase the awareness
  of the sig-security collaborators of threat modeling methods and examples.
- This **is** meant to create a code artifact and supporting documentation that can live on and be maintained.

## Deliverables

- Threat model (-as-code). All the following are meant to be contain the exact same data - and we hope to
  release the scripts and tools used to produce each from a single source of inputs:
  - a diagram format
  - markdown contents that explain the diagram content
  - a Google Sheet format 
- Methodology documentation in markdown in this repo
- Pre- and post- processing tooling and scripts in this repo
- OPTIONAL: Reports and data from actual use on components and sub-projects

## ASIDE: Responsible Disclosure

While this is not meant to be an audit or assessment, and is only meant to be an input to such
future activities, it is plausible that the additional scrutiny and consideration of Kubernetes
code, designs, features and capabilities during this effort may in fact surface novel 
latent vulnerabilities that could be used as zero day exploits.

If and when such flaws are discovered, data and observations will be discussed solely with 
sig-security leads for further guidance, presumably resulting in further consultation with the 
Kubernetes project and CNCF legal and disclosure SMEs.  

In any event, the team will embargo any actual or suspected vulnerability information until
directed by CNCF staff, or any valid governmental or law enforcement order within the EU or 
United States given the residence of the participants.

## Safe Harbor

By using, reviewing, or citing any of these materials you hold yourself, and any organization or government entity
you may be affiliated with, bound to an agreement of Safe Harbor for any contributors and reviewers as legitimate
security researchers performing a public service. No information contained herein shall be used for the purpose
of creating, distributing, or enabling illegal or unauthorized use of, or access to, any Kubernetes
cluster or project hosted on any Kubernetes cluster.

The contributors and reviewers assert their good faith effort to adhere to all known
legal requirements for academic and security research. Questions and concerns should be addressed
to the sig-security leads or CNCF legal representatives.

## Roadmap as of KubeCon NA 2023 wrap

- [ ] Host the roadmap in Github tasks and move the following there...
- [ ] Present initial framework to the Contributor Summit and gather feedback and
      create issues
- [ ] Present beta deliverables to sig-security for review and gather feedback
      and create issues
- [ ] Present GA deliverables to future CNCF event
- [ ] Hold "office hour" sessions at future CNCF event(s) for sub-projects to actually
      use the methodology and tools and refine the threat model
- [ ] Create blog post for GA with CNCF docs
- [ ] IF NECESSARY: Document and report vulnerabilities responsibly.
  
## Acknowledgements

- [Francesco Beltramini](https://twitter.com/d1gital_f)
- [@abdullahgarcia](https://twitter.com/abdullahgarcia)
- [Rory Raesene]()
- [Iain Smart]()
- [Alla Dewberry]()
- [Chris @ CNCF]()
- [@sunstonesecure-robert]()

## Getting Help

If you have any questions:

- File an issue.
- Attend a Kubernetes sig-security meeting.
- Post a message to the sig-security slack or mailing list.
