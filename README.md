# Rekall discontinuation

This project is no longer maintained.

In December 2011, a new branch within the Volatility project was created to explore how to make the code base more modular, improve performance, and increase usability. This branch was later forked to become Rekall. The modularity allowed physical memory analysis functionality to be used in [GRR](https://github.com/google/grr) to enable remote live in-memory analysis.

## Lessons learned:

* Rekall has introduced many improvements to memory analysis methodology over the years. For more information see: http://blog.rekall-forensic.com/ 
* Rekall framework allowed for limited modularization due to the nature of interdependent in-memory structure and early architectural decisions.
* Increasing RAM sizes and security measures like memory encryption are making traditional physical memory analysis more cumbersome.
* Physical memory analysis is fragile and maintenance heavy. Most physical memory analysis tools are basically kernel debuggers, without access to the source and debug symbols. Most memory analysis therefore can be a costly process of debugging / reverse engineering and keeping debug symbols / structure definitions up to date.

Active development on Rekall has been halted for a while. GRR has switched from using Rekall to [YARA](https://grr-doc.readthedocs.io/en/v3.2.0/release-notes.html) supporting a limited set of memory analysis capabilities that requires significantly less maintenance.

Core developers / maintainers for Rekall have other priorities and no one has stepped up to help out with maintenance. Therefore the Rekall project is discontinued. The project will be archived, and you are free to fork it and continue to make [changes](https://en.wikipedia.org/wiki/Free_and_open-source_software).

Winpmem will be continued as a separate project currently maintained at https://github.com/Velocidex/WinPmem. 

rekall-profiles
===============

This is the repository of Rekall profiles ( http://www.rekall-forensic.com/
). To use this repository, edit the file ~/.rekallrc to contain the lines:

```
profile_path:
  - https://raw.githubusercontent.com/google/rekall-profiles
```
