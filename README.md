<div align="center">

### failclosed

**I build self-hosted systems that have to keep running when nobody is watching.**

Backend and automation, mostly Python — and the unglamorous layer underneath:
the part that decides what happens when the network drops or an API lies.

</div>

---

### How I work

- **Fail closed.** When a dependency is unreachable, the answer is "don't act",
  never "assume it's fine". This is cheap to build in from the start and nearly
  impossible to retrofit.
- **A restart must not erase a decision.** If something stopped the system,
  a human decides when that reason has passed — not the next boot.
- **Measure before believing.** A number that only exists in-sample is not
  evidence, and a peak surrounded by cliffs is a curve fit.
- **Constrained hardware is a good teacher.** A tight memory budget makes you
  honest about what a service actually needs.

---

### Also

Container stacks with real resource limits, workflow automation, private
networking, and backups that have been restored at least once — because an
untested backup isn't a backup.

<div align="center">

<sub>What I build is private and stays that way.</sub>

</div>
