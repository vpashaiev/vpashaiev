### Viktor Pashaiev

Senior Linux Systems & Kernel Engineer based in Poland.  
Focused on Linux kernel diagnostics, drivers, core userspace daemons, and Canonical / Debian packaging.

- **Launchpad**: [~steelf](https://launchpad.net/~steelf)
- **Ubuntu Discourse**: [steelf](https://discourse.ubuntu.com/u/steelf)
- **Email**: w.paszajew@gmail.com

---

### Selected Upstream & Core Systems Contributions

#### OpenSSH
- **[openssh-portable PR #712](https://github.com/openssh/openssh-portable/pull/712)**: Fix untrusted `force_command` and `cert_principals` serialization in `auth-options.c`. Prevents fatal monitor crash (`unexpected authentication from 102`) under `PermitRootLogin forced-commands-only` + `UsePAM yes`.
- **Launchpad**: [Bug #2166842](https://bugs.launchpad.net/bugs/2166842)

#### Canonical Netplan
- **[netplan PR #614](https://github.com/canonical/netplan/pull/614)**: Enforce permissions with explicit `chmod()` on generated networkd configuration files under restrictive caller umasks (e.g. `0077`).
- **Launchpad**: [Bug #2164636](https://bugs.launchpad.net/bugs/2164636)

#### Canonical Landscape Client
- **[landscape-client PR #456](https://github.com/canonical/landscape-client/pull/456)**: Reject unrecognized positional arguments in `landscape-config` ([Bug #2028517](https://bugs.launchpad.net/bugs/2028517)).
- **[landscape-client PR #457](https://github.com/canonical/landscape-client/pull/457)**: Route Ubuntu Pro status operations to `data_path` instead of `$HOME` ([Bug #2146793](https://bugs.launchpad.net/bugs/2146793)).

#### Linux Kernel & Drivers
- **`igb` driver**: Queue reconfiguration race assertion fix ([Bug #2083151](https://bugs.launchpad.net/bugs/2083151)).
- **`ntfs3` / `iomap`**: Root cause analysis of buffered I/O write regression in `fs/iomap/buffered-io.c` ([Bug #2165844](https://bugs.launchpad.net/bugs/2165844)).
- **`mt7925e` driver**: Driver reset NULL pointer dereference patch in `mt76_connac_mcu_uni_add_dev` ([Bug #2137291](https://bugs.launchpad.net/bugs/2137291)).
- **KVM / NUMA**: Kernel panic bisection on multi-node AMD Opteron hardware ([Bug #2163642](https://bugs.launchpad.net/bugs/2163642)).

#### Packaging & Core Libraries
- **`v4l2-relayd`**: Debdiff providing SoftISP and libcamerasrc support via dma-buf allocator ([Bug #2166611](https://bugs.launchpad.net/bugs/2166611)).
- **`util-linux`**: Fix dynamic PAM linkage for `pam_lastlog2` loaded by systemd-executor ([Bug #2167039](https://bugs.launchpad.net/bugs/2167039)).
- **`cpupower-gui`**: Polkit rules update for non-seat user services and Python 3.14 syntax fixes ([PR #151](https://github.com/vagnum08/cpupower-gui/pull/151), [PR #153](https://github.com/vagnum08/cpupower-gui/pull/153), [Bug #2151790](https://bugs.launchpad.net/bugs/2151790)).

---

### Technical Focus
- **Languages**: C, Python, Bash
- **Core Systems**: Linux kernel internals, driver debugging, systemd, GDB, IPC, eBPF
- **Packaging**: Debian/Ubuntu packaging (DEP-3 patch headers, clean debdiffs, quilt, pbuilder/sbuild)
