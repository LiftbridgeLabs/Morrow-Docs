# Hosting your own server

Morrow plays your library from a server you run yourself. This guide helps you pick where that server lives: a computer you already own, or a small server you rent online. Once it's running, the server's own guide covers the install and Morrow's setup pages cover connecting.

Morrow works with three free, self-hosted servers: [Audiobookshelf](https://www.audiobookshelf.org/docs), [BookOrbit](https://bookorbit.app/installation) and [Grimmory](https://grimmory.org/docs). They all run on the same kinds of machines, so everything below applies to whichever one you choose.

## At home or rented?

| | At home | Rented server (VPS) |
|---|---|---|
| Cost | Free if you already own the hardware | A few dollars a month, or less with a yearly plan |
| Storage | As much as your drives hold | Fixed by the plan; storage-focused plans cost the least per GB |
| Reaching it away from home | Needs a VPN or reverse proxy, and your home internet upload speed limits streaming | Already on the internet, with fast upload |
| Upkeep | You handle power, drives and updates | The host handles the hardware; you handle updates |
| Best for | People with a NAS, an always-on PC or a spare Raspberry Pi | People with no always-on machine at home, or a slow home connection |

## Running it at home

Any computer that stays on works: a NAS (Synology, Unraid, TrueNAS), an old laptop or desktop, a mini PC or a Raspberry Pi 4 or 5. Most people install the server with Docker, which all three projects document.

To listen away from home, you have two common choices:

- **A private network** such as [Tailscale](https://tailscale.com/), which puts your phone and your server on the same private network. Nothing is opened to the internet. Install it on the server and on each device that runs Morrow.
- **A reverse proxy** with your own domain name, which gives your server a normal `https://` address that works anywhere. Popular ones:
  - [Pangolin](https://github.com/fosrl/pangolin), which is what we use. It runs on a small rented VPS and reaches your home server through an encrypted tunnel, so you don't open any ports on your home network. Your audiobooks stay at home; the VPS only passes the traffic through.
  - [Caddy](https://caddyserver.com/) or Nginx Proxy Manager, which run at home. You open a port on your home router, so keep the server updated and use a strong password.

## Renting a server

A virtual private server (VPS) is a small computer in a data center that you rent by the month or year. You install the server on it just as you would at home.

What to look for:

- **Storage first.** An audiobook is usually 500 MB to over 1 GB, depending on its length and audio quality, so 100 books can take 50 to 120 GB. Look for "storage VPS" plans, which trade processing power for large disks at a low price. Audiobook and ebook servers need very little processing power.
- **At least 1 GB of memory.** 2 GB gives some room to spare.
- **Enough monthly bandwidth.** An hour of listening is roughly 30 to 100 MB, so most plans' bandwidth limits are more than enough for one household.
- **A refund window or monthly billing,** so you can try it without a long commitment.

Hosts we use for our own projects. We haven't tested an audiobook server on each one, but any of them can run one:

- **[GreenCloud](https://greencloudvps.com/billing/aff.php?aff=10131)** (commission link, see below). We run a small server there for another project. Their "Storage" plans are the ones to look at for an audiobook library: in November 2026 the smallest had 500 GB of disk and 2 GB of memory for $25 a year. Check their site for current plans and prices.
- **[Clouvider](https://console.clouvider.co.uk/?affid=671&oid=62&affplan=3)** (commission link, see below). We run our Pangolin server here. A small VPS plan is plenty for Pangolin, since your audiobooks stay at home.
- **[Oracle Cloud Free Tier](https://www.oracle.com/cloud/free/).** Morrow's own demo server runs here. The free tier's Arm servers are powerful, but free storage is limited, signup can be strict, and you should check the current free limits before you start. No commission.

A rented server is already on the internet, so you could connect to it by its IP address and port (like `http://203.0.113.10:13378`). Don't stop there: that address has no HTTPS, so your password travels unencrypted. Put a reverse proxy in front of it instead, and you get your own address (like `https://books.example.com`) with HTTPS. Pangolin, Caddy and Nginx Proxy Manager can all run on the same VPS as your audiobook server. Tailscale also works on a VPS if you'd rather keep the server private.

## Your audiobooks

Your server plays the audiobook files you put on it. Those can be DRM-free audiobooks you bought, or free public-domain recordings from [LibriVox](https://librivox.org/), like the ones in the demo on our home page. Morrow doesn't provide, sell or host audiobooks.

## Connecting Morrow

Once the server is running and has your audiobooks:

1. Open the server's web page in Safari (or your phone's browser) to confirm it loads and you can sign in.
2. In Morrow, go to **Settings > Add Server** and follow the setup page for your server: [Audiobookshelf](audiobookshelf-setup.md), [BookOrbit](bookorbit-setup.md) or [Grimmory](grimmory-setup.md).

If it doesn't connect, see [Troubleshooting](troubleshooting.md).

## About the commission links

The GreenCloud and Clouvider links above are referral links. If you buy a plan through one, Liftbridge Labs, the maker of Morrow, earns a small commission at no extra cost to you. We only list hosts we have used, and hosts without a referral program (like Oracle) are listed the same way. Morrow works the same no matter where your server runs.
