<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/9/94/Cloudflare_Logo.png" alt="Cloudflare Logo" width="300" />

<h1 align="center">Kitab Cloudflare ⛅️ 🇮🇩<br><sub>(Stack Nol Rupiah)</sub></h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=F38020&center=true&vCenter=true&width=600&lines=Bangun+SaaS+Modal+Rp+0;Serverless+di+Cloudflare;Senjata+Indie+Hacker+Indonesia;Tinggalkan+VPS+Tradisional" alt="Typing SVG" />
</p>

Kumpulan alat, *starter kit*, panduan, dan proyek *open-source* terbaik yang berjalan di atas infrastruktur Cloudflare (Workers, Pages, D1, R2, KV). 
Dibangun untuk membantu developer dan *indie hacker* Indonesia meluncurkan produk SaaS atau *microservices* dengan arsitektur *serverless* dan biaya server Rp 0.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Stars](https://img.shields.io/github/stars/ridloabelian/awesome-cloudflare-id?style=flat&color=F38020)](https://github.com/ridloabelian/awesome-cloudflare-id/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/ridloabelian/awesome-cloudflare-id?style=flat&color=F38020)](https://github.com/ridloabelian/awesome-cloudflare-id/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

</div>

Cloudflare saat ini bukan sekadar CDN atau proteksi DDoS, melainkan ekosistem komputasi *Edge* yang sangat *powerful*. Untuk fase validasi ide atau *bootstrapping*, ekosistem ini memberikan batas gratis (Free Tier) yang sangat longgar sehingga Anda bisa membangun sistem kompleks tanpa perlu menyewa VPS.

**Kriteria Kurasi:**
- Bermanfaat untuk mempercepat *development* SaaS / Web App.
- Membantu menekan biaya infrastruktur (sedekat mungkin dengan Rp 0).
- Mudah di-deploy (mendukung Terraform/Wrangler atau 1-click deploy).
- *Open-source* dan masih aktif di-*maintain*.

---

## 💰 Batas Gratis (Free Tier) Cloudflare

Sebelum membangun, kenali dulu batas gratisnya. Angka di bawah adalah acuan umum paket **Free/Workers Paid** — selalu cek [halaman resmi](https://developers.cloudflare.com/workers/platform/limits/) karena kebijakan bisa berubah.

| Layanan | Batas Gratis (Free Tier) | Catatan |
|---------|--------------------------|---------|
| **Workers** | 100.000 request/hari | CPU time 10ms/request. Cukup untuk API kecil-menengah. |
| **Pages** | Unlimited request & bandwidth | 500 build/bulan. Ideal untuk hosting frontend statis. |
| **D1** (SQL) | 5 GB storage, 5 juta baris dibaca/hari | Database SQLite di Edge. |
| **R2** (Object Storage) | 10 GB storage, egress GRATIS | Pengganti AWS S3 tanpa biaya *bandwidth* keluar. |
| **KV** (Key-Value) | 100.000 baca & 1.000 tulis/hari | Cocok untuk cache & konfigurasi. |
| **Workers AI** | ~10.000 Neuron/hari (bervariasi) | Jalankan Llama, Whisper, dll gratis dalam kuota. |
| **Durable Objects** | Perlu paket Workers Paid ($5/bln) | Untuk state real-time (WebSocket, kolaborasi). |
| **Email Routing** | Unlimited | Buat alamat email custom & forwarding gratis. |

> ⚠️ **Penting:** Fitur seperti **Durable Objects** dan sebagian besar kuota **Workers AI** yang besar butuh paket berbayar **Workers Paid ($5/bulan)**. Perhatikan label pada tiap *tools* di bawah jika membutuhkannya.

---

## Daftar Isi
- [💰 Batas Gratis (Free Tier) Cloudflare](#-batas-gratis-free-tier-cloudflare)
- [🚀 Boilerplate & SaaS Starter Kit](#-boilerplate--saas-starter-kit)
- [🗄️ Database & ORM](#️-database--orm)
- [🖼️ Hosting Gambar (Image Hosting)](#️-hosting-gambar-image-hosting)
- [💬 Chatbot & Komunitas (Discord/WA/TG)](#-chatbot--komunitas-discordwatg)
- [📧 Email Sementara & Routing](#-email-sementara--routing)
- [📈 Analytics & Marketing](#-analytics--marketing)
- [📱 Social Media Automation](#-social-media-automation)
- [📝 Blogging & CMS](#-blogging--cms)
- [🤖 AI & Agen (MCP)](#-ai--agen-mcp)
- [🔗 Shortlink & Pastebin](#-shortlink--pastebin)
- [🌐 Proxy, DNS & Utilitas](#-proxy-dns--utilitas)
- [🎁 Domain Gratis](#-domain-gratis)

---

## 🚀 Boilerplate & SaaS Starter Kit
Kerangka kerja (*framework*) siap pakai untuk langsung mulai *coding* bisnis Anda tanpa pusing memikirkan setup awal.

| Nama | Deskripsi |
|------|-----------|
| [create-microservices-app](https://github.com/microservices-sh/microservices-sh) ![](https://img.shields.io/github/stars/microservices-sh/microservices-sh?style=flat&label=%E2%98%85&color=F38020) | Starter kit SaaS komplit. SvelteKit/Hono + D1 + Workers. Fitur bawaan: modul Auth, *booking*, pembayaran, dan email. |
| [cloudflare-workers-nextjs-saas-template](https://github.com/LubomirGeorgiev/cloudflare-workers-nextjs-saas-template) ![](https://img.shields.io/github/stars/LubomirGeorgiev/cloudflare-workers-nextjs-saas-template?style=flat&label=%E2%98%85&color=F38020) | Template SaaS modern menggunakan Next.js App Router dan Cloudflare Workers. |
| [nextflare](https://github.com/ccbikai/nextflare) ![](https://img.shields.io/github/stars/ccbikai/nextflare?style=flat&label=%E2%98%85&color=F38020) | Template Next.js App yang sudah terintegrasi dengan Lemon Squeezy (pembayaran) dan berjalan mulus di Cloudflare Pages. |
| [lunora](https://github.com/anolilab/lunora) ![](https://img.shields.io/github/stars/anolilab/lunora?style=flat&label=%E2%98%85&color=F38020) | *Framework backend real-time* yang memberikan *Developer Experience* senyaman Firebase/Convex, tapi datanya murni di akun Cloudflare Anda (D1, R2, DO). |

## 🗄️ Database & ORM
Alat untuk mengelola database Edge (D1, KV) dengan lebih mudah.

| Nama | Deskripsi |
|------|-----------|
| [Cloudflare-KV-Manager](https://github.com/som3canadian/Cloudflare-KV-Manager) ![](https://img.shields.io/github/stars/som3canadian/Cloudflare-KV-Manager?style=flat&label=%E2%98%85&color=F38020) | Solusi Web UI (Dashboard) dan Pustaka Python untuk manajemen Cloudflare KV yang jauh lebih lengkap dibanding bawaan *dashboard* Cloudflare. |
| [Prisma with D1](https://www.prisma.io/docs/orm/overview/databases/cloudflare-d1) | Dokumentasi dan *adapter* resmi untuk menggunakan ORM Prisma di atas database Cloudflare D1. |

## 🖼️ Hosting Gambar (Image Hosting)
Buat Imgur-mu sendiri. Simpan gambar tanpa batas *bandwidth*.

| Nama | Deskripsi |
|------|-----------|
| [CloudFlare-ImgBed](https://github.com/MarSeventh/CloudFlare-ImgBed) ![](https://img.shields.io/github/stars/MarSeventh/CloudFlare-ImgBed?style=flat&label=%E2%98%85&color=F38020) | TuChuang/Image Hosting modern. Bisa simpan file ke R2, Telegram, S3, atau WebDAV. Tidak membatasi ukuran atau format file. |
| [imgUU](https://github.com/yestool/imgUU) ![](https://img.shields.io/github/stars/yestool/imgUU?style=flat&label=%E2%98%85&color=F38020) | Aplikasi *upload* gambar gratis berbasis Cloudflare D1 dan R2. Terintegrasi dengan GitHub Login untuk panel adminnya. |
| [cf-image-hosting](https://github.com/ifyour/cf-image-hosting) ![](https://img.shields.io/github/stars/ifyour/cf-image-hosting?style=flat&label=%E2%98%85&color=F38020) | Hosting gambar menggunakan layanan Telegraph (Telegram) di-*proxy* lewat Cloudflare. Gratis tanpa batas (Catatan: Hati-hati dengan privasi gambar). |

## 💬 Chatbot & Komunitas (Discord/WA/TG)
Jalankan bot Discord, Telegram, atau *webhook* WhatsApp Business API yang stabil, tahan *traffic* tinggi, dan 100% *serverless* tanpa perlu menyewa VPS.

| Nama | Deskripsi |
|------|-----------|
| [whatsapp-mcp-server](https://github.com/spirit122/whatsapp-mcp-server) ![](https://img.shields.io/github/stars/spirit122/whatsapp-mcp-server?style=flat&label=%E2%98%85&color=F38020) | Server MCP untuk WhatsApp Business Cloud API. Memberikan 35+ alat bagi AI Agent Anda untuk membaca obrolan, membalas, dan mengirim *template message*. |
| [workers-whatsapp-transcription](https://github.com/jkpe/workers-whatsapp-transcription) ![](https://img.shields.io/github/stars/jkpe/workers-whatsapp-transcription?style=flat&label=%E2%98%85&color=F38020) | Mengubah *Voice Note* (Pesan Suara) WhatsApp menjadi teks secara otomatis menggunakan model Whisper via Workers AI, lalu membalas pesannya dengan hasil transkripsi. |
| [whatsapp-auth-service](https://github.com/leolicona/whatsapp-auth-service) ![](https://img.shields.io/github/stars/leolicona/whatsapp-auth-service?style=flat&label=%E2%98%85&color=F38020) | Layanan login *passwordless* atau OTP (One Time Password) menggunakan WhatsApp alih-alih SMS biasa. Berbasis Hono dan database D1. |
| [chat-ya-wam](https://github.com/leolicona/chat-ya-wam) ![](https://img.shields.io/github/stars/leolicona/chat-ya-wam?style=flat&label=%E2%98%85&color=F38020) | Template *webhook* ringan (berbasis Hono) untuk membangun asisten AI otomatis via WhatsApp Cloud API. |
| [cloudflare-sample-app](https://github.com/discord/cloudflare-sample-app) ![](https://img.shields.io/github/stars/discord/cloudflare-sample-app?style=flat&label=%E2%98%85&color=F38020) | Contoh aplikasi bot Discord resmi dari tim Discord untuk membangun *Slash Commands* yang ditenagai oleh Cloudflare Workers. |
| [discord-hono](https://github.com/luisfun/discord-hono) ![](https://img.shields.io/github/stars/luisfun/discord-hono?style=flat&label=%E2%98%85&color=F38020) | Pustaka (*library*) untuk mempermudah pembuatan bot Discord di Cloudflare Workers menggunakan *framework* web Hono. |
| [cloudflare-worker-emails-to-discord](https://github.com/Tyler-OBrien/cloudflare-worker-emails-to-discord) ![](https://img.shields.io/github/stars/Tyler-OBrien/cloudflare-worker-emails-to-discord?style=flat&label=%E2%98%85&color=F38020) | Teruskan email yang masuk (via Cloudflare Email Routing) langsung ke *channel* Discord Anda sebagai notifikasi. |
| [discord-oidc-worker](https://github.com/Erisa/discord-oidc-worker) ![](https://img.shields.io/github/stars/Erisa/discord-oidc-worker?style=flat&label=%E2%98%85&color=F38020) | Kunci aplikasi internal Anda dengan fitur "Login with Discord" melalui Cloudflare Access, pastikan hanya anggota *server* Discord Anda yang bisa masuk. |

## 📧 Email Sementara & Routing
Layanan untuk menerima atau meneruskan email, sangat berguna untuk fitur validasi (OTP) akun dummy atau CRM sederhana.

| Nama | Deskripsi |
|------|-----------|
| [vmail](https://github.com/oiov/vmail) ![](https://img.shields.io/github/stars/oiov/vmail?style=flat&label=%E2%98%85&color=F38020) | Layanan Temp-Mail (*Disposable Email*) yang di-deploy murni di Cloudflare Worker dan D1. Mendukung banyak domain. |
| [cloudflare_temp_email](https://github.com/dreamhunter2333/cloudflare_temp_email) ![](https://img.shields.io/github/stars/dreamhunter2333/cloudflare_temp_email?style=flat&label=%E2%98%85&color=F38020) | Temp-mail lengkap dengan antarmuka UI. Menggunakan D1 sebagai database, mendukung *auto-reply*, banyak bahasa, dan bahkan IMAP/SMTP via lampiran. |
| [agentic-inbox](https://github.com/cloudflare/agentic-inbox) ![](https://img.shields.io/github/stars/cloudflare/agentic-inbox?style=flat&label=%E2%98%85&color=F38020) | Proyek resmi dari Cloudflare: Klien email *self-hosted* dengan asisten AI terintegrasi, murni berjalan di Workers. AI bisa membaca dan membalas email Anda. |

## 📈 Analytics & Marketing
Ganti langganan *tools* pemasaran yang mahal (seperti Mailchimp atau Plausible) dengan infrastruktur *edge* milik Anda sendiri.

| Nama | Deskripsi |
|------|-----------|
| [LetterDrop](https://github.com/i365dev/LetterDrop) ![](https://img.shields.io/github/stars/i365dev/LetterDrop?style=flat&label=%E2%98%85&color=F38020) | Sistem manajemen *Newsletter* (Email Blast) yang berjalan 100% di Cloudflare Workers. Mendukung fitur *subscribe/unsubscribe* dan *compose* email. |
| [analytics_with_cloudflare](https://github.com/yestool/analytics_with_cloudflare) ![](https://img.shields.io/github/stars/yestool/analytics_with_cloudflare?style=flat&label=%E2%98%85&color=F38020) | Analitik web *open-source* (pengganti Google Analytics) yang menjaga privasi pengunjung. Berbasis Hono dan D1 lengkap dengan antarmuka dasbor. |
| [relay](https://github.com/YuriCrystal/relay) ![](https://img.shields.io/github/stars/YuriCrystal/relay?style=flat&label=%E2%98%85&color=F38020) | *Link shortener* khusus pemasaran dengan analitik klik, *A/B split*, penargetan geolokasi, dan integrasi FB Pixel / GA4 untuk *retargeting* tanpa *cookie*. Berjalan di D1. |
| [cloudflare-workers-async-google-analytics](https://github.com/SukkaW/cloudflare-workers-async-google-analytics) ![](https://img.shields.io/github/stars/SukkaW/cloudflare-workers-async-google-analytics?style=flat&label=%E2%98%85&color=F38020) | Percepat *loading* situs web Anda dengan memindahkan eksekusi skrip pelacakan Google Analytics ke sisi *server* (di Cloudflare Worker) alih-alih di *browser* pengunjung. |

## 📱 Social Media Automation
Alat bantu operasional *digital advertising*, automasi media sosial (pengganti ManyChat / Zapier), dan optimasi tautan untuk berbagai *platform*.

| Nama | Deskripsi |
|------|-----------|
| [inapp-escape](https://github.com/deepthix/inapp-escape) ![](https://img.shields.io/github/stars/deepthix/inapp-escape?style=flat&label=%E2%98%85&color=F38020) | Paksa tautan di bio TikTok/Instagram terbuka di *browser* asli pengunjung (Chrome/Safari), bukan di dalam *in-app browser* yang sering bermasalah. |
| [ig-harness-oss](https://github.com/Shudesu/ig-harness-oss) ![](https://img.shields.io/github/stars/Shudesu/ig-harness-oss?style=flat&label=%E2%98%85&color=F38020) | Alternatif *open-source* ManyChat. Otomatisasi DM Instagram untuk membalas komentar spesifik dan *follow-loop*, sepenuhnya *serverless*. |
| [ig_gallery_worker](https://github.com/lia-07/ig_gallery_worker) ![](https://img.shields.io/github/stars/lia-07/ig_gallery_worker?style=flat&label=%E2%98%85&color=F38020) | *Script background* (Cron) yang otomatis memperpanjang *token* Instagram API. Wajib dipakai jika Anda menampilkan *feed* IG klien di situs web agar tidak putus tiap 60 hari. |
| [tracklay](https://github.com/matheusmaiberg/tracklay) ![](https://img.shields.io/github/stars/matheusmaiberg/tracklay?style=flat&label=%E2%98%85&color=F38020) | *Proxy tracking* (1st-party) untuk Facebook Pixel, Google Analytics, dan GTM. Menyembunyikan skrip pelacak agar lolos dari *Ad-Blocker* (iOS/Safari). |
| [tiktok-ai-agent](https://github.com/stivenrosales/tiktok-ai-agent) ![](https://img.shields.io/github/stars/stivenrosales/tiktok-ai-agent?style=flat&label=%E2%98%85&color=F38020) | Asisten AI (Gemini) yang berjalan di Workers untuk membalas *Direct Message* (DM) TikTok secara otomatis, terintegrasi dengan ManyChat. |
| [yt-deeplink](https://github.com/Adam-s-Builder-Club/yt-deeplink) ![](https://img.shields.io/github/stars/Adam-s-Builder-Club/yt-deeplink?style=flat&label=%E2%98%85&color=F38020) | Pengganti *Smartlink* berbayar. Arahkan pengunjung dari TikTok/Instagram langsung ke aplikasi asli (contoh: YouTube) alih-alih membuka versi *web*. |
| [defuddle](https://github.com/thieung/defuddle) ![](https://img.shields.io/github/stars/thieung/defuddle?style=flat&label=%E2%98%85&color=F38020) | Alat untuk membaca tautan utas (thread) X/Twitter dan mengubahnya menjadi *Markdown* bersih. Sangat berguna sebagai *pipeline* bagi AI Agen Anda. |
| [tweets-to-discord](https://github.com/MattIPv4/tweets-to-discord) ![](https://img.shields.io/github/stars/MattIPv4/tweets-to-discord?style=flat&label=%E2%98%85&color=F38020) | Skrip *Cron* yang akan menyalin (*mirroring*) setiap cuitan (Tweet) baru Anda ke *channel* Discord komunitas. |
| [capi-gateway-template](https://github.com/pfranklinn/capi-gateway-template) ![](https://img.shields.io/github/stars/pfranklinn/capi-gateway-template?style=flat&label=%E2%98%85&color=F38020) | *Server-side Tracking* (CAPI Gateway) untuk Meta Ads dan Google Ads. Solusi menembus blokir Pixel di iOS/AdBlocker dengan mengirim *event* langsung dari *server* Edge. |
| [open-ads-report](https://github.com/clawnify/open-ads-report) ![](https://img.shields.io/github/stars/clawnify/open-ads-report?style=flat&label=%E2%98%85&color=F38020) | Dasbor analitik *cross-platform* (Meta + Google Ads) *open-source*. Menyediakan API JSON agar AI Agent Anda bisa memantau dan memberikan saran terkait performa iklan. |
| [media-parser-proxy](https://github.com/pekaboo/media-parser-proxy) ![](https://img.shields.io/github/stars/pekaboo/media-parser-proxy?style=flat&label=%E2%98%85&color=F38020) | API *Proxy* (berbasis Worker) untuk mengekstrak dan mengunduh video tanpa *watermark* dari platform seperti TikTok, Douyin, dan Bilibili. |

## 📝 Blogging & CMS
Alternatif gratis untuk WordPress yang lari secepat kilat di infrastruktur Edge.

| Nama | Deskripsi |
|------|-----------|
| [Rin](https://github.com/openRin/Rin/) ![](https://img.shields.io/github/stars/openRin/Rin?style=flat&label=%E2%98%85&color=F38020) | Sistem blog berbasis Cloudflare Pages + Workers + D1 + R2. Tanpa server tradisional, cukup sambungkan domain Anda. |
| [microfeed](https://github.com/microfeed/microfeed) ![](https://img.shields.io/github/stars/microfeed/microfeed?style=flat&label=%E2%98%85&color=F38020) | CMS mandiri (*self-hosted*) super ringan. Bisa mempublikasikan audio, video, teks, dokumen via RSS dan JSON. Ideal untuk *podcast* atau *changelog*. |
| [Gins-Blog](https://github.com/IchimaruGin728/Gins-Blog) ![](https://img.shields.io/github/stars/IchimaruGin728/Gins-Blog?style=flat&label=%E2%98%85&color=F38020) | Platform blog berperforma tinggi dengan pendekatan *Agentic-First*. Mendukung protokol MCP (Model Context Protocol). |
| [cwd](https://github.com/anghunk/cwd) ![](https://img.shields.io/github/stars/anghunk/cwd?style=flat&label=%E2%98%85&color=F38020) | Sistem komentar *serverless* pengganti Disqus. Kecepatan maksimal dan privasi terjaga karena *database* ditaruh di D1 milik Anda sendiri. |

## 🤖 AI & Agen (MCP)
Eksperimen kecerdasan buatan, Model Context Protocol (MCP), dan Agen Otonom di *Edge*.

| Nama | Deskripsi |
|------|-----------|
| [CloudFlare-AI-Insight-Daily](https://github.com/justlovemaki/CloudFlare-AI-Insight-Daily) ![](https://img.shields.io/github/stars/justlovemaki/CloudFlare-AI-Insight-Daily?style=flat&label=%E2%98%85&color=F38020) | *Aggregator* AI otomatis. Menarik berita GitHub, riset, dan Twitter lalu di-summary pakai Gemini dan di-push jadi koran harian ke GitHub Pages. |
| [second-brain-cloudflare](https://github.com/rahilp/second-brain-cloudflare) ![](https://img.shields.io/github/stars/rahilp/second-brain-cloudflare?style=flat&label=%E2%98%85&color=F38020) | Lapis memori / RAG untuk AI. Simpan catatan sekali, ingat kembali saat Anda mengobrol dengan Claude, Cursor, atau ChatGPT via API MCP. |
| [MetaReview](https://github.com/TerryFYL/metareview) ![](https://img.shields.io/github/stars/TerryFYL/metareview?style=flat&label=%E2%98%85&color=F38020) | Platform meta-analisis medis/data. Menggunakan Llama 3.1 8B via Workers AI untuk ekstraksi dan pembuatan grafik (D3.js) dari PDF riset. |
| [edgeever](https://github.com/tianma-if/edgeever) ![](https://img.shields.io/github/stars/tianma-if/edgeever?style=flat&label=%E2%98%85&color=F38020) | Alternatif Evernote tanpa server dengan dukungan *native* AI Agent / MCP. |
| [web2gem](https://github.com/Guardinary/web2gem) ![](https://img.shields.io/github/stars/Guardinary/web2gem?style=flat&label=%E2%98%85&color=F38020) | Gateway ringan yang menerjemahkan API Google Gemini menjadi format yang kompatibel dengan API OpenAI. Deploy ke Cloudflare cukup dengan 1 file. |
| [mcp-memory](https://github.com/Puliczek/mcp-memory) ![](https://img.shields.io/github/stars/Puliczek/mcp-memory?style=flat&label=%E2%98%85&color=F38020) | Server MCP (*Model Context Protocol*) untuk menyimpan memori dan preferensi user secara persisten di Cloudflare D1 & Vectorize. |
| [my-ax](https://github.com/acoyfellow/my-ax) ![](https://img.shields.io/github/stars/acoyfellow/my-ax?style=flat&label=%E2%98%85&color=F38020) | "Sistem Operasi Agen Pribadi" yang di-*self-hosted* penuh di atas Cloudflare Workers, Durable Objects, D1, dan MCP. |
| [tutorial-cloudflare-agents-bot](https://github.com/Celebez/tutorial-cloudflare-agents-bot) ![](https://img.shields.io/github/stars/Celebez/tutorial-cloudflare-agents-bot?style=flat&label=%E2%98%85&color=F38020) | Tutorial langkah demi langkah membuat Bot Telegram yang ditenagai AI Agent (Cloudflare Workers + Pages + Bindings) tanpa API Keys eksternal. |
| [codra](https://github.com/devarshishimpi/codra) ![](https://img.shields.io/github/stars/devarshishimpi/codra?style=flat&label=%E2%98%85&color=F38020) | Sistem *AI Code Review* mandiri untuk *Pull Request* GitHub Anda. Menggunakan arsitektur serverless (Workers, Queues, Hyperdrive, Workers AI). |
| [zenith-image-generator](https://github.com/WuMingDao/zenith-image-generator) ![](https://img.shields.io/github/stars/WuMingDao/zenith-image-generator?style=flat&label=%E2%98%85&color=F38020) | Antarmuka web (UI) untuk *AI Image Generator* multi-provider yang bisa langsung di-deploy ke Cloudflare Pages. |

## 🔗 Shortlink & Pastebin
Ganti Bitly atau Pastebin berbayar dengan milik Anda sendiri yang tidak membatasi fitur kustomisasi.

| Nama | Deskripsi |
|------|-----------|
| [Sink](https://github.com/ccbikai/Sink) ![](https://img.shields.io/github/stars/ccbikai/Sink?style=flat&label=%E2%98%85&color=F38020) | Pemendek tautan (*URL Shortener*) lengkap dengan dasbor analitik dan statistik trafik. Berjalan sepenuhnya secara *serverless*. |
| [pastebin-worker](https://github.com/SharzyL/pastebin-worker) ![](https://img.shields.io/github/stars/SharzyL/pastebin-worker?style=flat&label=%E2%98%85&color=F38020) | Aplikasi *Pastebin* (berbagi teks/kode) *open-source*. Mendukung kata sandi pelindung dan fitur hapus otomatis setelah dibaca (*burn after reading*). |
| [r2-explorer](https://github.com/G4brym/r2-explorer) ![](https://img.shields.io/github/stars/G4brym/r2-explorer?style=flat&label=%E2%98%85&color=F38020) | File Manager / *Browser* Web yang cantik untuk mengelola (melihat, *upload*, hapus) *bucket* Cloudflare R2 Anda dengan dukungan *password*. |
| [wr.do](https://github.com/oiov/wr.do) ![](https://img.shields.io/github/stars/oiov/wr.do?style=flat&label=%E2%98%85&color=F38020) | Sistem distribusi DNS dan pemendek tautan multi-penyewa (multi-tenant) berbasis Workers. |

## 🌐 Proxy, DNS & Utilitas
Kumpulan alat untuk *networking*, manajemen sistem, dan produktivitas harian.

| Nama | Deskripsi |
|------|-----------|
| [CF-Server-Monitor](https://github.com/huilang-me/CF-Server-Monitor) ![](https://img.shields.io/github/stars/huilang-me/CF-Server-Monitor?style=flat&label=%E2%98%85&color=F38020) | Dasbor *uptime monitor* ala UptimeKuma. Menggunakan Worker, D1, dan Durable Objects untuk melacak ping & *latency* banyak VPS secara real-time. |
| [cloudflare-doh-proxy](https://github.com/4n0nymou3/cloudflare-doh-proxy) ![](https://img.shields.io/github/stars/4n0nymou3/cloudflare-doh-proxy?style=flat&label=%E2%98%85&color=F38020) | Proxy DNS over HTTPS (DoH) untuk *load balancing* dan menembus sensor internet (misal: Internet Positif). |
| [ternssh](https://github.com/HaradaKashiwa/ternssh) ![](https://img.shields.io/github/stars/HaradaKashiwa/ternssh?style=flat&label=%E2%98%85&color=F38020) | Klien SSH berbasis Web yang berjalan di atas Cloudflare Workers. Remot VPS Anda langsung dari *browser* dari mana saja. |
| [cf-manager](https://github.com/hefy2027/cf-manager) ![](https://img.shields.io/github/stars/hefy2027/cf-manager?style=flat&label=%E2%98%85&color=F38020) | Dasbor *all-in-one* untuk manajemen banyak akun Cloudflare sekaligus (DNS, Workers, D1, R2, AI). |
| [ip-api](https://github.com/ccbikai/ip-api) ![](https://img.shields.io/github/stars/ccbikai/ip-api?style=flat&label=%E2%98%85&color=F38020) | API super sederhana untuk cek IP Address pengunjung beserta geolokasi-nya menggunakan header bawaan Cloudflare. |
| [cloudflare-block-bad-bot-ruleset](https://github.com/SukkaW/cloudflare-block-bad-bot-ruleset) ![](https://img.shields.io/github/stars/SukkaW/cloudflare-block-bad-bot-ruleset?style=flat&label=%E2%98%85&color=F38020) | Koleksi aturan *Firewall* (WAF) siap pakai untuk memblokir *crawler/scraper* nakal yang menghabiskan bandwidth situs Anda. |
| [docker-cloudflare-ddns](https://github.com/oznu/docker-cloudflare-ddns) ![](https://img.shields.io/github/stars/oznu/docker-cloudflare-ddns?style=flat&label=%E2%98%85&color=F38020) | Docker *image* untuk menyambungkan IP internet rumah (Indihome/Biznet yang IP-nya dinamis) ke domain Cloudflare secara otomatis (DDNS). |
| [cloudflare-workers-basic-auth](https://github.com/dommmel/cloudflare-workers-basic-auth) ![](https://img.shields.io/github/stars/dommmel/cloudflare-workers-basic-auth?style=flat&label=%E2%98%85&color=F38020) | Beri perlindungan *password* (Basic Auth) pada situs statis apa pun hanya bermodal skrip Worker sederhana. |
| [airtable-proxy-worker](https://github.com/portable-cto/airtable-proxy-worker) ![](https://img.shields.io/github/stars/portable-cto/airtable-proxy-worker?style=flat&label=%E2%98%85&color=F38020) | Proxy aman untuk menggunakan Airtable sebagai database *backend* tanpa membocorkan API Key Airtable Anda ke publik. |

## 🎁 Domain Gratis
Layanan komunitas yang dikelola di atas Cloudflare untuk membagikan subdomain gratis bagi developer.

| Nama | Deskripsi |
|------|-----------|
| [js.cool](https://github.com/willin/js.cool) ![](https://img.shields.io/github/stars/willin/js.cool?style=flat&label=%E2%98%85&color=F38020) | Layanan bagi-bagi subdomain `.js.cool` gratis selamanya untuk developer. Pendaftaran via *Pull Request* GitHub. |
| [domain](https://github.com/willin/domain) ![](https://img.shields.io/github/stars/willin/domain?style=flat&label=%E2%98%85&color=F38020) | Proyek saudari dari `js.cool`, memberikan variasi subdomain `.sh.gg` dan lainnya gratis. Di-*serve* via Cloudflare DNS API. |

---

## 🤝 Kontribusi
Jika Anda menemukan *tools* menarik lainnya atau sedang membangun *side project* berbasis Cloudflare, silakan buat *Pull Request*! Baca dulu [panduan kontribusi](CONTRIBUTING.md) kami.

<a href="https://github.com/ridloabelian/awesome-cloudflare-id/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ridloabelian/awesome-cloudflare-id" alt="Contributors" />
</a>

## 📜 Lisensi
Lisensi MIT - [Ridlo Abelian](https://github.com/ridloabelian)

---
*Kredit: Diadaptasi dan dikurasi dari [zhuima/awesome-cloudflare](https://github.com/zhuima/awesome-cloudflare), [Ezeafk/awesome-cloudflare-ai](https://github.com/Ezeafk/awesome-cloudflare-ai), dan [irazasyed/awesome-cloudflare](https://github.com/irazasyed/awesome-cloudflare) dengan penyesuaian untuk ekosistem developer Indonesia.*

<div align="center">

<a href="#kitab-cloudflare-️-">⬆️ Kembali ke Atas</a>

</div>
