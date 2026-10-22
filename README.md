# Rackview edge releases

Signed release tarballs for the Rackview edge appliance, one GitHub release per version (tag `edge-vX.Y.Z`). This repository holds release assets only; the source is private.

Each release carries, per architecture (`linux_amd64`, `linux_arm64`):

- `rackview-edge_<version>_linux_<arch>.tar.gz` and its minisign signature `.minisig`
- `SHA256SUMS` over the tarballs, and `SHA256SUMS.minisig`

Verify before installing:

```sh
minisign -Vm rackview-edge_<version>_linux_amd64.tar.gz -P RWSPexohIkU/joEhZUO/mBr1C8nF+XOL2JAeHHl24IBLKeHVtiepv3Ln
```

Public key (key id 8E3F4522211A7B8F):

```
untrusted comment: minisign public key 8E3F4522211A7B8F
RWSPexohIkU/joEhZUO/mBr1C8nF+XOL2JAeHHl24IBLKeHVtiepv3Ln
```

An installed appliance verifies updates against `/etc/rackview-edge/release.pub` and refuses anything else.
