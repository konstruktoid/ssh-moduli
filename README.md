# OpenSSH Moduli Generation Script

This repository contains a GitHub Action that fetches the moduli
files from OpenSSH on a weekly basis and merges them into one.

The file contains only moduli of size 4096 or larger.

See [.github/workflows/modulimerge.yml](https://github.com/konstruktoid/ssh-moduli/blob/main/.github/workflows/modulimerge.yml)
for details.

> NOTE
> If you have high security requirements, consider generating your own
> instead, see [man ssh-keygen](https://www.man7.org/linux/man-pages/man1/ssh-keygen.1.html#MODULI_GENERATION)


This repository is used by [konstruktoid/ansible-role-hardening](https://github.com/konstruktoid/ansible-role-hardening?tab=readme-ov-file#defaultsmainsshdyml)
