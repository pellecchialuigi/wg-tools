
![logo](logo_elisa_small.png)

# ELISA Tool Investigation & Code Improvement Working Group

## Date: 25-07-24

## Agenda

* Roll Call
* Announcements
* Discussion Items
  * Logistics
  * Prioritize Discussion Topics
* Closing
  * Action Items
  * Round Table

## Roll Call

### Attended this meeting

* Matt Kelly (Boeing)
* Luigi Pellecchia (Red Hat)

### Attended in the past

* Sudip Mukherjee (CodeThink)
* Matt Weber (Boeing)
* Muhammad Qasim (Seimens)
* Chuck Wolber (Boeing)
* Jeannette N. (Boeing)
* Shefali Sharma (Nextleap Aeronautics).
* Jeannette N. (Boeing)
* Steve VanderLeest (Boeing)
* Youssef Hajjiouri (Hurn3t S3c)
* Lukas Bulwahn (Elektrobit Automotive)
* Phillip Ahmann (Bosch)
* Thomas Mittlestadt (Bosch)
* Gabriele Paoloni (Red Hat)

## Announcements

### Brief Notices

* ELISA Project meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in, any activities that are prohibited under applicable US state, federal, or foreign antitrust and competition laws.
  * [Linux Foundation Antitrust Policy](http://www.linuxfoundation.org/antitrust*policy)
* Email communication will be treated as documentation and be received and made available by the Project under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0). Please refer to the ELISA Technical Charter section 7 subsection iv. for details.
* The discussions in these meetings are exploratory. The opinions expressed by participants are not necessarily the policy of the companies.
* No recordings of working group meetings are permitted. Special provisions may be arranged for recording in advance with explicit consent of the participants.
* The kernel and LF Code of Conduct applies to all communication with this project
  * [Linux Foundation Code of Conduct](https://www.linuxfoundation.org/code*of*conduct/)
  * Linux [Contributor Covenant Code of Conduct](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/Documentation/process/code*of*conduct.rst)
  * Linux Kernel Contributor Covenant [Code of Conduct Interpretation](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/Documentation/process/code*of*conduct*interpretation.rst)

### Upcoming Conferences

* OSS Europe (Amsterdam) - August
  * ELISA will have a booth!

## Agenda Items

### Current Topics

* Announcements
* 2025 Working Group Update
* ks-nav topics
* BASIL topics
* DeltaKernel topics
* Boeing/UIUC llvm-cov
* stress-ng Investigation

### Next Topics

* Kernel testing
  * Can we contribute to kernel testing in a systematic way?
  * Translating runtime test to kunit tests
* Tool Qualification
  * What are the similarities/differences of Tool Qualification across industries?
  * How we do approach qualification of OSS tools?
* clang compatibility
  * Can we use clang in Yocto as an alternative to GCC
* ELISA CI
  * How can we contribute to / expand the ELISA CI?
* Engagement
  * How do we increase engagement with this group?
  * How do we directly tie our work to Vertical WGs?
  * How do we directly help maintainers?
  * How do we engage on peoples *actual* daily problems?

## Discussion Notes

* Announcements
  * Matt has informed the TSC he is looking to hand off leadership of the Tools WG in the medium term
    * Need to get on the TSC agenda to discuss this in that forum and look for volunteers
    * May be able to find someone in Boeing is has the bandwidth to continue leading, not sure
* Catch-up
* ks-nav topics
* BASIL topics
  * LP: Do you know anything about SBOM generation?
    * MK: Only what Yocto does for SBOM generation
    * LP: Questione being asked about BASIL's SBOM processing
      * https://github.com/elisa-tech/BASIL/issues/188
    * MK: Other person Joshua Watt did most of the SDPX/SBOM implementation for Yocto Project
    * LP: This page list all the tools that use SPDX: https://spdx.dev/use/spdx-tools/
      * Python library claims validation for v2.2 and v2.3 but not yet for v3.0
      * Here is the actual spec: https://spdx.dev/use/specifications/
    * MK: Yocto is on 3.0 because of limitations in generating the SBOM with the 2.X specs
    * LP: MR pending that is about migrating from SQLite to PostgresSQL
      * Finally passing all the tests, merging soon
      * Better support for concurrency and more users, can have multiple test running the background with logs and data at the same time
    * No matter what you add, you get random questions at conferences
      * From Amsterdam: Does it generate PDFs?
    * Now supports suggestions from AI
      * Configuration file to an external LLM/AI agent
      * Will automatically fill out the GUI for you
      * Can be used to generate tests around a requirement
      * Demo'ed this with Llama in Amsterdam
* 2025 Objectives
* Boeing/UIUC llvm-cov
  * MK: This effort has always required a patch for kernel coverage
    * The patch was blocked by an llvm linker issue which is now resolved and the patch is moving again
  * MK: UIUC llvm-cov running on Xen
    * Working on a patch for Xen to add llvm-cov support
  * MK: Working on modifying the way llvm stores profile data such that downstream users (Xen/Kernel) don't require an update each time that a new version of llvm is released
* DeltaKernel topics
* stress-ng Investigation

## Round Table

## Action Items

* [ ] Matt: Update the repo with Discord channel details
* [ ] Matt: Add link to the kconfig visualization the GitHub front page
* [ ] Matt: Investigation leveraging stress-ng (send example for LP's talk)
* [ ] Matt K/Matt W: Talk about possible addition of complexity metrics
