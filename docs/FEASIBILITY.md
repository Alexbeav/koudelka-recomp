# Koudelka release feasibility

Status: `bootstrap_verified`; Windows package pending R2 and R3

The operator confirmed that the promoted private Disc 1 build reaches
gameplay. This source-only pilot does not inherit that claim. It must pass the
exact-package setup, generation, build, and startup gates before it can claim
`bootstrap_verified`.

The owned PAL set contains four serials: `SLES-02897`, `SLES-12897`,
`SLES-22897`, and `SLES-32897`. Every disc has the same boot executable
SHA-256, `661bd13917e21032dcfe98ca012011d1021cb79f45688aa4c50a75e6d7d95390`.
The frozen verifier therefore classifies the set as one program on four data
images. One setup host is valid.

The package must validate and remember all four discs. Mid-session disc change
remains a separate gameplay seam. The public package must not contain a disc,
a BIOS, generated retail code, a save, a prebuilt title executable, or a
private absolute path.
