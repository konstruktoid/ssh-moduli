# ssh-moduli

Merges offical SSH moduli files into one using GitHub Actions.

```sh
set -eu -o pipefail
curl -fsSL "https://raw.githubusercontent.com/openssh/openssh-portable/master/moduli" | grep -v '^#' > /tmp/moduli.tmp
curl -fsSL "https://cvsweb.openbsd.org/cgi-bin/cvsweb/~checkout~/src/usr.bin/ssh/moduli-gen/moduli.{3072,4096,6144,7680,8192}" >> /tmp/moduli.tmp
awk '$5 >= 3071' ./moduli.tmp | grep -vE '^$|#'| sort -u >> ./moduli
rm -v /tmp/moduli.tmp
```
