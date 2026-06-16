# adjudica-fixture-repo

This is a disposable test repository used solely to generate real Semgrep
Supply Chain (SCA) JSON output for validating Adjudica's scanner ingestion
parser against actual tool output rather than synthetic fixtures built from
documentation alone.

It deliberately pins known-vulnerable package versions:

- Pillow==9.0.0 (CVE-2022-22817, CVE-2022-45198)
- lodash@4.17.20 (CVE-2021-23337, CVE-2020-8203)
- axios@0.21.1 (CVE-2021-3749)

These match the packages/versions already used in Adjudica's synthetic test
fixtures, so the resulting real Semgrep Supply Chain output can be directly
compared against the synthetic version to confirm field-level parser
compatibility.

This repo contains no real application code and is not intended for any
other purpose.
