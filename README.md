# SRv6 Workshop — Netdev 0x1A (Rome, 2026)

## Live page

**https://netgroup.github.io/netdev-0x1A-srv6-workshop/**

- Workshop Introduction — interactive: <https://netgroup.github.io/netdev-0x1A-srv6-workshop/slides/01-workshop-intro/presentation.html>
- Workshop Introduction — PDF: <https://netgroup.github.io/netdev-0x1A-srv6-workshop/slides/01-workshop-intro/presentation.pdf>
- SRv6 for the AI Backend — interactive: <https://netgroup.github.io/netdev-0x1A-srv6-workshop/slides/02-srv6-ai-backend/presentation.html>
- SRv6 for the AI Backend — PDF: <https://netgroup.github.io/netdev-0x1A-srv6-workshop/slides/02-srv6-ai-backend/presentation.pdf>
- SRv6 Layer 2 Services support — interactive: <https://netgroup.github.io/netdev-0x1A-srv6-workshop/slides/03-srv6-l2-services/presentation.html>
- SRv6 Layer 2 Services support — PDF: <https://netgroup.github.io/netdev-0x1A-srv6-workshop/slides/03-srv6-l2-services/presentation.pdf>

GitHub Pages is served from branch `main`, folder `/docs`
(Settings → Pages → Deploy from a branch → `main` / `docs`).

## The workshop

Segment Routing over IPv6 (SRv6, RFC 8986) lets an application or operator encode a
packet-processing program directly in the IPv6 header. SRv6 has been supported in the
Linux kernel since release 4.10, and a rich open-source ecosystem (FRR, SONiC, Cilium,
VPP) has grown on top of it.

Following the SRv6 workshops at Netdev 0x16 (Lisbon 2022) and 0x19 (Zagreb 2025), this
edition covers three directions that directly impact the kernel datapath — source-routed
AI backends, L2 services beyond VXLAN, and provider-grade SRv6 deployment with service
protection — plus a short ecosystem update.

**Chair:** Stefano Salsano (University of Rome Tor Vergata / CNIT)
**When:** Monday 13 July 2026, 10:00–12:00 — at Netdev 0x1A (13–16 July 2026, Rome, Italy)

## Programme

| Time | Talk | Speaker |
|---|---|---|
| 10:00–10:05 | Workshop Introduction | Stefano Salsano (Univ. of Rome Tor Vergata) |
| 10:05–10:15 | SRv6 Introduction | Ahmed Abdelsalam (Cisco) |
| 10:15–10:25 | SRv6 for the AI Backend | Stefano Salsano (Univ. of Rome Tor Vergata) |
| 10:25–10:40 | SRv6 in SONiC — "Enabling AI Backend use-case and many others" | Ahmed Abdelsalam (Cisco) |
| 10:40–10:55 | SRv6 in FRR — "5 Years of mainline support" | Carmine Scarpitta (Cisco) |
| 10:55–11:15 | SRv6 for network providers and service protection | Ferenc Fejes (Ericsson) |
| 11:15–11:25 | SRv6 in Linux — "9 Years of mainline support" | Andrea Mayer (Univ. of Rome Tor Vergata) |
| 11:25–11:45 | SRv6 Layer 2 Services support | Andrea Mayer (Univ. of Rome Tor Vergata) |
| 11:45–12:00 | Recap and Discussion | all speakers |

## Repository layout

```
docs/                             ← GitHub Pages root (main / docs)
├── index.html                    ← workshop landing page (self-contained)
└── slides/
    ├── 01-workshop-intro/presentation.html
    ├── 02-srv6-ai-backend/presentation.html
    ├── 03-srv6-l2-services/presentation.html
    └── assets/
        ├── reveal/               ← Reveal.js 5.1.0, vendored locally (offline, MIT)
        ├── tor-vergata-logo.png, cnit-logo.png
        └── mur-logo.svg, italia-domani.svg   ← PRIN/PNRR funding banner (deck 3)
```

The "SRv6 Layer 2 Services support" deck is grounded on the RFC v2 branches:
[`srv6-linux-kernel-dev @ seg6_sr6_L2encap_rfc-v2`](https://github.com/netgroup/srv6-linux-kernel-dev/tree/seg6_sr6_L2encap_rfc-v2)
and [`srv6-linux-iproute2-dev @ seg6_sr6_L2encap_UAPI-v2`](https://github.com/netgroup/srv6-linux-iproute2-dev/tree/seg6_sr6_L2encap_UAPI-v2).

The decks are self-contained Reveal.js presentations: **no CDN, no network needed**.
They run from `file://` in any browser — a USB stick is enough.

Slides for the other talks will be added as the speakers provide them.

## Exporting a deck to PDF

1. Open the deck in Chrome.
2. On the title slide, click **Save as PDF** (bottom right). The deck reloads in
   `?print-pdf&autoprint=1` and the print dialog opens by itself.
3. In the dialog: destination **Save as PDF**, enable **Background graphics**, margins **None**.
4. Save as `presentation.pdf` next to the corresponding `presentation.html`.

Result: landscape PDF, one slide per page.

## License

Slides and landing page: [CC BY 4.0](LICENSE) — free to reuse with attribution.
Reveal.js is vendored under its own MIT license (`docs/slides/assets/reveal/LICENSE`).
Referenced papers remain © their respective publishers.
