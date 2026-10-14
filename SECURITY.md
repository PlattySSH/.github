# Security policy

Platty stores SSH keys, passwords and host keys, so we take security reports seriously.

## Reporting a vulnerability

Please **don't open a public issue**. Report it privately through [GitHub security advisories](https://github.com/PlattySSH/platty/security/advisories/new) instead.

Include what you can:

- the Platty version (Settings → About) and your Windows version;
- what an attacker could do, and what they need first (access to your PC, a malicious server, a crafted file...);
- steps or a proof of concept to reproduce it.

We'll answer within a week, keep you posted while we work on a fix, and credit you in the release notes unless you'd rather stay anonymous.

## Supported versions

Platty is in beta. Only the latest release gets security fixes.

## What we especially want to hear about

- The vault: anything that reads hosts, keys or passwords without the master password or the Windows user.
- Host key checks that can be skipped, or a changed key that isn't reported.
- A server or a program running in the terminal that can run commands on your PC, read your clipboard or write files you didn't ask for.
- `.platty` backups that leak secrets you didn't choose to include.
