
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
* Sudip Mukherjee (CodeThink)

### Attended in the past

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
  * Thoughts?
* ks-nav topics
  * MR for documentation: https://github.com/dnjean/ks-nav/tree/demo-upload
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
  * We know have a Discord Channel!
    * We have a BASIL Channel
* Catch-up
  * 2-3 meetings with Andrew but then we had a string of 3-4 where no one showed up
  * Mostly status of what we are doing.
* ks-nav topics
* BASIL topics
  * LP: Some new features developed
    * Support for Lava
    * Configure your Lava instance
    * Can trace requirements -> procedures -> results all through Lava
    * MK: What is Lava?
      * Linaro Automated Validation Architecture
      * Can configure it with physical hardware or virtual machine
      * Takes care of provisioning the hardware
    * Request to be able to use Jinja template for the contribution file that you need for Lava
    * Request to have automated notifications
    * Support from Linux Foundation created an email account to use in our public instance to send notification
      * This helps us reset our passwords
    * Merged request to request permissions from within BASIL to give write permission for certain software components
    * Request to specify username instead of email in the public instance
    * InfoMagnos is working on a continuous certification framework built on top of BASIL
      * Able to diff SBOM based on SPDX (which can be exported from BASIL today)
      * Presented this concept at the OSS Summit NA: https://www.youtube.com/watch?v=VPwTrn5MZ9I
      * We should see if we can get InfoMagnus instrested in the ELISA work and get them participating in the tools group
    * OSS Europe (Amsterdam) talk accepted about BASIL
* 2025 Objectives
  * MK: I'll prepare more to talk about this next time,
  * LP: Kate / Gab working on YAML definition into KernelCI to link requirements to test case and test results
    * That's really good because within BASIL we can trace what is done in KernelCI
    * MK: What forum are they working in?
      * LP: Not really sure, but there will be a presentation at OSS Europe on it
* Boeing/UIUC llvm-cov
  * This group is now working on a new tool (tentatively called ocov) to address object code coverage
  * DO-178C Software Level-A has an objective to ensure coverage of code added by the compiler that is not representing in source
  * Group has now shifted it's focus from llvm-cov to this new tool/objective
  * Trying to execute this process on the kernel, but even kernel init generates many gigabytes of data
  * Looking at how to make this capture practical / useful
* DeltaKernel topics
  * No movement here
* stress-ng Investigation

## Round Table

## Action Items

* [ ] Matt: Update the repo with Discord channel details
* [ ] Matt: Add link to the kconfig visualization the GitHub front page
* [ ] Matt: Investigation leveraging stress-ng (send example for LP's talk)
* [ ] Matt K/Matt W: Talk about possible addition of complexity metrics
