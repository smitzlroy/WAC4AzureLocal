# WAC for Azure Local — Mid/Low-Level Design

A short, opinionated design for running **Windows Admin Center (WAC)** at scale to manage **Azure Local** across many sites and regions.

## What's in here

| File | Purpose |
| --- | --- |
| [`WAC-AzureLocal-Design.html`](WAC-AzureLocal-Design.html) | The design document. Open in Edge or Chrome — sticky TOC, dark-mode aware, modern Mermaid diagrams with inline icons. |
| [`WAC-AzureLocal-Design.pdf`](WAC-AzureLocal-Design.pdf) | Print-ready PDF rendered from the HTML. Best for email / SharePoint review. |
| [`WAC-AzureLocal-Design.zip`](WAC-AzureLocal-Design.zip) | Both files together for distribution. |

## What it covers

- **Three first-class deployment patterns** — pick the one that fits your operating model:
  - **Pattern A** — On-prem HA WAC (regional)
  - **Pattern B** — WAC in Azure VMs (regional HA, over ExpressRoute / S2S)
  - **Pattern C** — WAC in Azure portal (service, currently preview for Azure Local)
- **Per-site break-glass WAC (Tier 2)** — common to all three patterns; activated only when the regional Tier 1 is unreachable.
- **Run modes** — Always-on / Cold-standby / JIT for cost-aware Pattern B deployments.
- **Reference architecture** diagrams per pattern, plus a decision tree that lands on A / B / C.
- **Dev/Test pattern** (single VM).
- **Shared baseline** — network, firewall, OT, security, operations, lifecycle and out-of-band / VM-console guidance that applies to every pattern.
- **Open questions** to drive the network and OT conversations.

## Sources

Microsoft Learn only. Every reference is linked inline and listed in §10 of the document.

## How to view / share

- **View**: open `WAC-AzureLocal-Design.html` in any modern browser.
- **Print to PDF**: `Ctrl+P` → *Save as PDF* (the navigation sidebar is hidden in print).
- **Share**: send the `.zip`, or just the `.pdf`.

> Status: Draft for review. Update the document-control block at the top of the HTML before circulating.
