<div align="center">

### failclosed

**I build self-hosted systems that have to keep running when nobody is watching.**

Backend and automation, mostly Python. Trading infrastructure and the
unglamorous layer underneath: the part that decides what happens when the
network drops, the API lies, or the strategy is simply wrong.

</div>

---

### What I'm working on

**A trading bot where the safety layer is the product.**
Circuit breakers, a kill switch that stays reachable when the dashboard isn't,
position reconciliation against the exchange, and a dead-man's switch that
fires precisely when the bot has broken badly enough that it can no longer
report anything itself. The staged rollout from simulation to live capital is
enforced by code, not by a README.

The backtester is built to be disappointing on purpose — grid search guarded
against curve fitting, walk-forward analysis that only reports out-of-sample
results, and a matrix that scores every strategy across four market regimes
side by side. It ran 336 backtests and the honest answer was that most
plausible-looking strategies are noise. One strategy came out of that finding
rather than out of a textbook.

*Python · FastAPI · SQLAlchemy 2 async · PostgreSQL · Docker · APScheduler*

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

<sub>Automated trading can lose real money. Nothing I publish is investment advice.</sub>

</div>
