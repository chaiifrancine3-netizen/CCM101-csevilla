# Security Audit Report — Chapter 8 Research

## Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving every user account only the
minimum permissions it needs to do its job, and nothing more. For cloud user
accounts this is important because if one account is compromised, the attacker
only gets that account's limited access instead of full control of the
environment. It also makes it easier to track who is allowed to do what.

## Attack Surface

When applied to a virtual machine, the attack surface is the total set of ways
an attacker could try to get in — open network ports, running services,
installed software, user accounts, and any exposed management interfaces. The
more services and entry points a VM exposes, the larger the attack surface and
the more an attacker has to work with. Reducing the attack surface means
disabling or removing anything the VM doesn't actually need.

## Default Deny Policy

A Default Deny policy means all traffic is blocked unless a rule explicitly
allows it. This is safer than trying to block specific hackers one by one
because attackers can change IP addresses, use new tools, and come from
anywhere — you can't predict or list every threat. By allowing only known-good
traffic, anything unknown is stopped automatically without needing to know who
the attacker is.
