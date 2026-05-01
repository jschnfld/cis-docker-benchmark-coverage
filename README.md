# cis-docker-benchmark-coverage

# CIS Docker Benchmark Coverage by Open-Source Static Analysis Tools

> Bachelor thesis project (Frankfurt UAS, 2026): How well do Trivy, Dockle, and Hadolint cover the CIS Docker Benchmark v1.8.0, and where do gaps remain?

## Status

🚧 **Work in progress** – thesis runs from April to June 2026. This repository will be updated weekly.

- [x] Research question and scope defined
- [ ] SAST/DAST classification of all 114 CIS controls
- [ ] Test corpus (6–8 Docker images) built
- [ ] Tool runs and JSON output collected
- [ ] Coverage matrix completed
- [ ] Final thesis submitted

## Research Question

To what extent do common open-source static container security analysis tools (Trivy, Dockle, Hadolint) cover the security requirements of the CIS Docker Benchmark, and which gaps remain in automated detection?

## Approach

1. **SAST/DAST classification** – classify each of the 114 CIS controls as statically checkable, partially checkable, or runtime-only
2. **Test corpus** – build hardened, intentionally misconfigured, and realistic mixed Docker images
3. **Tool runs** – execute Trivy, Dockle, and Hadolint with consistent parameters, capture JSON output
4. **Mapping** – manually map each finding to a CIS control with a three-level coverage rating (covered / partial / not covered)
5. **Coverage matrix** – tool × CIS category, distinguishing structural (DAST) gaps from tool gaps

## Repository Structure

```
.
├── corpus/              # Test Dockerfiles and images
├── classification/      # SAST/DAST classification of CIS controls
├── scans/               # Raw JSON output from tool runs
├── mapping/             # Mapping of findings to CIS controls
├── results/             # Coverage matrix and analysis
└── docs/                # Methodology notes
```

(Folders will appear as work progresses.)

## Tools Under Test

| Tool     | Version | Scope                                    |
|----------|---------|------------------------------------------|
| Trivy    | TBD     | CVE detection, Dockerfile, CIS compliance |
| Dockle   | TBD     | Image best-practice linting              |
| Hadolint | TBD     | Dockerfile linting                       |

## Reproducibility

All scans are reproducible: tool versions, CVE database state, benchmark version, and test environment will be documented in `docs/environment.md`.

## Related Work

- Cruz et al. (2023), *Open Source Solutions for Vulnerability Assessment*, IEEE Access
- Bashun & Shadrunov (2024), *Quality Assessment of Static Analyzers for Containerized Applications*, IEEE
- Haq et al. (2024), *SoK: Docker Container Attack and Defense Mechanisms*, IEEE S&P
- CIS Docker Benchmark v1.8.0 (2025)
- Rice (2025), *Container Security*, 2nd Edition, O'Reilly

## Author

Jonathan Schönfeld – B.Sc. Computer Science, Frankfurt University of Applied Sciences

## License

Code: MIT. Thesis text and figures: CC BY-NC 4.0.
