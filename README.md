# WAC for Azure Local — Mid/Low-Level Design

A short, opinionated design for running **Windows Admin Center (WAC)** at scale to manage **Azure Local** in a regulated, multi-site enterprise estate.

## What's in here

| File | Purpose |
| --- | --- |
| [`WAC-AzureLocal-Design.html`](WAC-AzureLocal-Design.html) | The design document. Open in Edge or Chrome — sticky TOC, dark-mode aware, modern Mermaid diagrams with inline icons. |
| [`WAC-AzureLocal-Design.pdf`](WAC-AzureLocal-Design.pdf) | Print-ready PDF rendered from the HTML. Best for email / SharePoint review. |
| [`WAC-AzureLocal-Design.zip`](WAC-AzureLocal-Design.zip) | Both files together for distribution. |

## What it covers

- **Recommended topology** — a two-tier pattern: regional HA WAC for daily use, plus a per-site break-glass WAC for WAN/ER outages and OT-mandated local-only operations.
- **Why WAC-in-Azure-VM is not recommended** for Azure Local at scale, with a pragmatic migration path.
- **Reference architecture** diagrams (global, single-region, port/protocol, decision tree, break-glass runbook).
- **Production** (HA failover-cluster) and **Dev/Test** (single VM) build patterns.
- **Network, firewall and OT requirements** with explicit port and FQDN tables.
- **Security baseline**, **operations & lifecycle**, and **out-of-band / VM-console** guidance.
- **Open questions** to drive the OT and network conversations.

## Sources

Microsoft Learn only. Every reference is linked inline and listed in §13 of the document.

## How to view / share

- **View**: open `WAC-AzureLocal-Design.html` in any modern browser.
- **Print to PDF**: `Ctrl+P` → *Save as PDF* (the navigation sidebar is hidden in print).
- **Share**: send the `.zip`, or just the `.pdf`.

> Status: Draft for review. Update the document-control block at the top of the HTML before circulating.
