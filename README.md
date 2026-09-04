# SafeStack Validation Registry

This repository records SafeStack projects that have completed the declared validation process.

## Current status

`REGISTRY.json` currently contains no validated projects. An empty registry is not evidence that any repository, release or deployment is approved.

A project may be listed only when it:

- complies with the referenced Root and Technical Canons;
- provides artifact hashes and a verifiable detached signature;
- identifies the review evidence and approval date;
- passes independent review under the applicable release policy.

## Verification

```bash
sha256sum -c REGISTRY_HASH.txt
python -m json.tool REGISTRY.json >/dev/null
```

The checksum proves byte integrity only. Verify `REGISTRY.json.asc` with an independently trusted OpenPGP public key before relying on publisher identity.
