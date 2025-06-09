# Fortran Tooling Hack Week 2025

This repository contains resources for the Fortran Tooling Hack Week taking place between May
27th and May 30th 2025.

Building upon the success of the [Back to the Fortran Future](https://lu.ma/ao471jms) event at
[RSECon 2024](https://rsecon24.society-rse.org/), we're aiming to make contributions to the
open-source Fortran tooling ecosystem. This includes testing frameworks, documentation
generators, linters, debuggers, and more. Participation in this event will be flexible --
whether you can spare just an hour per day or want to contribute more, you're welcome to join.

The hack week will begin with short project pitches, after which attendees will be encouraged
to form teams. A dedicated Slack space will be provided to help coordinate activities, though
teams are welcome to use any communication tool they prefer. Throughout the week, we'll host
optional morning stand-up sessions for teams to share progress and raise any blockers, along
with afternoon check-in and co-working sessions, where attendees can collaborate and support
each other. The project organisers [@LiamPattinson](https://github.com/LiamPattinson) and
[@ZedThree](https://github.com/ZedThree) will be available at these sessions to help
troubleshoot any issues that arise.

While we would recommend attending each meeting, we understand that this may not always be
feasible. We will therefore make accommodations where possible, and no single meeting will be
mandatory, including the introduction, project pitches, and closing presentations. Recordings
will be made available for those who can't make the project pitches.

## Schedule

All timings are in British Summer Time (UTC+1)

- Tuesday 27th May -- Project Pitches and Team Formation
  - 10:00 -- 10:15: Welcome, introductions, code of conduct.
  - 10:15 -- 11:00: Project pitches (3-5 minutes each).
  - 11:00 -- 12:00: Team formation, initial planning.
  - 12:00 -- 16:00: Flexible working.
  - 16:00 -- 17:00: Afternoon check-in and co-working.

- Wednesday 28th May and Thursday 29th May -- Flexible working
  - 10:00 -- 10:30: Morning stand-up.
  - 10:30 -- 16:00: Flexible working.
  - 16:00 -- 17:00: Afternoon check-in and co-working.

- Friday 30th May -- Progress Reports and Wrap-Up
  - 10:00 -- 10:30: Final stand-up.
  - 10:30 -- 14:00: Flexible working.
  - 14:00 -- 16:00: Team presentations and closing remarks.
 
## Code of Conduct

We will be following the code of conduct of the Society of Research Software Engineering
throughout the event. Please see [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) for details.

## Contact

If you have any questions or wish to report a violation of the code of conduct, please
contact Liam Pattinson at [liam.pattinson@york.ac.uk](mailto:liam.pattinson@york.ac.uk).

---

# Outcomes

A huge thank you to all attendees!

- [@TomMelt](https://github.com/TomMelt) worked on the [Fortitude](https://github.com/PlasmaFAIR/fortitude) formatter, building upon previous efforts using the [Topiary](https://github.com/tweag/topiary) library to set whitespace and indentation. Made significant progress towards the reuse of select linting rule fixes as a post-processing step. Explored the Fortitude codebase in more depth, and learned some Rust in the process!

- [@ZedThree](https://github.com/ZedThree) also worked on the Fortitude formatter, fixing some errors in the Topiary grammar, converting Topiary errors into Fortitude errors, and improving the robustness of the formatter by requiring idempotency (this option can be switched off in exchange for higher performance). Additionally made fixes to the [tree-sitter-fortran](https://github.com/stadelmanma/tree-sitter-fortran) grammar to resolve a number of long-standing issues.

- [@connorair](https://github.com/connoraird) worked to add new Fortitude rules. As a first-time contributor, and without prior experience programming in Rust, was able to add two new rules (https://github.com/PlasmaFAIR/fortitude/pull/457 and https://github.com/PlasmaFAIR/fortitude/pull/460) and began work on a third (https://github.com/PlasmaFAIR/fortitude/pull/464). Also investigated the feasibility of hosting [pFUnit](https://github.com/Goddard-Fortran-Ecosystem/pFUnit) on [FPM](https://fpm.fortran-lang.org/index.html), finding that FPM support would need to be added to all of pFUnit’s dependencies and that major changes would be needed to pFUnit itself. It may be more feasible to add CMake support to FPM than to get pFUnit ready for FPM.

- [@LiamPattinson](https://github.com/LiamPattinson) worked on adding new rules to Fortitude and helped to on-board new contributors. Added two new 'correctness' rules (https://github.com/PlasmaFAIR/fortitude/pull/458 and https://github.com/PlasmaFAIR/fortitude/pull/466) which can catch major bugs, and is in a position to add a similar third rule without difficulty. Additionally gained experience organising events and running hackathons, and is hoping to take this forward to future projects.

- Worked towards a user-sortable reference of which features are offered by various compilers and tools in both the open-source and closed-source world (including free-for-academic-use commercial products). Made significant progress on developing a compiler test suite to better understand the variance between different compilers, and found an example web page containing a user-sortable table that could be adapted for use on Fortran-Lang’s pages.

- Made progress towards resolving licensing issues that would otherwise prevent the inclusion of the documentation generator [FORD](https://forddocs.readthedocs.io/en/stable/) in Fortran-Lang community projects. These discussions helped to inform a NumFOCUS grant submission (https://github.com/numfocus/small-development-grant-proposals/issues/31) to improve FORD/Sphinx compatibility.
