<div align="center">

<h1 align="center">Kitab Cloudflare ⛅️ 🇮🇩<br><sub>(Stack Nol Rupiah)</sub></h1>

Kumpulan alat, *starter kit*, panduan, dan proyek *open-source* terbaik yang berjalan di atas infrastruktur Cloudflare (Workers, Pages, D1, R2, KV). 
Dibangun untuk membantu developer dan *indie hacker* Indonesia meluncurkan produk SaaS atau *microservices* dengan arsitektur *serverless* dan biaya server Rp 0.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

</div>

Cloudflare saat ini bukan sekadar CDN atau proteksi DDoS, melainkan ekosistem komputasi *Edge* yang sangat *powerful*. Untuk fase validasi ide atau *bootstrapping*, ekosistem ini memberikan batas gratis (Free Tier) yang sangat longgar sehingga kita bisa membangun sistem kompleks tanpa perlu menyewa VPS.

**Kriteria Kurasi:**
- Bermanfaat untuk mempercepat *development* SaaS / Web App.
- Membantu menekan biaya infrastruktur (sedekat mungkin dengan Rp 0).
- Mudah di-deploy (mendukung Terraform/Wrangler atau 1-click deploy).
- *Open-source* dan masih aktif di-*maintain*.

---

## Daftar Isi
- [🚀 Boilerplate & SaaS Starter Kit](#-boilerplate--saas-starter-kit)
- [🗄️ Database & ORM](#️-database--orm)
- [🖼️ Hosting Gambar (Image Hosting)](#️-hosting-gambar-image-hosting)
- [📧 Email Sementara & Routing](#-email-sementara--routing)
- [📈 Analytics & Marketing](#-analytics--marketing)
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
| [create-microservices-app](https://github.com/microservices-sh/microservices-sh) | Starter kit SaaS komplit. SvelteKit/Hono + D1 + Workers. Fitur bawaan: modul Auth, *booking*, pembayaran, dan email. |
| [cloudflare-workers-nextjs-saas-template](https://github.com/LubomirGeorgiev/cloudflare-workers-nextjs-saas-template) | Template SaaS modern menggunakan Next.js App Router dan Cloudflare Workers. |
| [nextflare](https://github.com/ccbikai/nextflare) | Template Next.js App yang sudah terintegrasi dengan Lemon Squeezy (pembayaran) dan berjalan mulus di Cloudflare Pages. |
| [lunora](https://github.com/anolilab/lunora) | *Framework backend real-time* yang memberikan *Developer Experience* senyaman Firebase/Convex, tapi datanya murni di akun Cloudflare Anda (D1, R2, DO). |

## 🗄️ Database & ORM
Alat untuk mengelola database Edge (D1, KV) dengan lebih mudah.

| Nama | Deskripsi |
|------|-----------|
| [Cloudflare-KV-Manager](https://github.com/som3canadian/Cloudflare-KV-Manager) | Solusi Web UI (Dashboard) dan Pustaka Python untuk manajemen Cloudflare KV yang jauh lebih lengkap dibanding bawaan *dashboard* Cloudflare. |
| [Prisma with D1](https://www.prisma.io/docs/orm/overview/databases/cloudflare-d1) | Dokumentasi dan *adapter* resmi untuk menggunakan ORM Prisma di atas database Cloudflare D1. |

## 🖼️ Hosting Gambar (Image Hosting)
Buat Imgur-mu sendiri. Simpan gambar tanpa batas *bandwidth*.

| Nama | Deskripsi |
|------|-----------|
| [CloudFlare-ImgBed](https://github.com/MarSeventh/CloudFlare-ImgBed) | TuChuang/Image Hosting modern. Bisa simpan file ke R2, Telegram, S3, atau WebDAV. Tidak membatasi ukuran atau format file. |
| [imgUU](https://github.com/yestool/imgUU) | Aplikasi *upload* gambar gratis berbasis Cloudflare D1 dan R2. Terintegrasi dengan GitHub Login untuk panel adminnya. |
| [cf-image-hosting](https://github.com/ifyour/cf-image-hosting) | Hosting gambar menggunakan layanan Telegraph (Telegram) di-*proxy* lewat Cloudflare. Gratis tanpa batas (Catatan: Hati-hati dengan privasi gambar). |

## 📧 Email Sementara & Routing
Layanan untuk menerima atau meneruskan email, sangat berguna untuk fitur validasi (OTP) akun dummy atau CRM sederhana.

| Nama | Deskripsi |
|------|-----------|
| [vmail](https://github.com/oiov/vmail) | Layanan Temp-Mail (*Disposable Email*) yang di-deploy murni di Cloudflare Worker dan D1. Mendukung banyak domain. |
| [cloudflare_temp_email](https://github.com/dreamhunter2333/cloudflare_temp_email) | Temp-mail lengkap dengan antarmuka UI. Menggunakan D1 sebagai database, mendukung *auto-reply*, banyak bahasa, dan bahkan IMAP/SMTP via lampiran. |
| [agentic-inbox](https://github.com/cloudflare/agentic-inbox) | Proyek resmi dari Cloudflare: Klien email *self-hosted* dengan asisten AI terintegrasi, murni berjalan di Workers. AI bisa membaca dan membalas email Anda. |

## 📈 Analytics & Marketing
Ganti langganan *tools* pemasaran yang mahal (seperti Mailchimp atau Plausible) dengan infrastruktur *edge* milik Anda sendiri.

| Nama | Deskripsi |
|------|-----------|
| [LetterDrop](https://github.com/i365dev/LetterDrop) | Sistem manajemen *Newsletter* (Email Blast) yang berjalan 100% di Cloudflare Workers. Mendukung fitur *subscribe/unsubscribe* dan *compose* email. |
| [analytics_with_cloudflare](https://github.com/yestool/analytics_with_cloudflare) | Analitik web *open-source* (pengganti Google Analytics) yang menjaga privasi pengunjung. Berbasis Hono dan D1 lengkap dengan antarmuka dasbor. |
| [relay](https://github.com/YuriCrystal/relay) | *Link shortener* khusus pemasaran dengan analitik klik, *A/B split*, penargetan geolokasi, dan integrasi FB Pixel / GA4 untuk *retargeting* tanpa *cookie*. Berjalan di D1. |
| [cloudflare-workers-async-google-analytics](https://github.com/SukkaW/cloudflare-workers-async-google-analytics) | Percepat *loading* situs web Anda dengan memindahkan eksekusi skrip pelacakan Google Analytics ke sisi *server* (di Cloudflare Worker) alih-alih di *browser* pengunjung. |

## 📝 Blogging & CMS
Alternatif gratis untuk WordPress yang lari secepat kilat di infrastruktur Edge.

| Nama | Deskripsi |
|------|-----------|
| [Rin](https://github.com/openRin/Rin/) | Sistem blog berbasis Cloudflare Pages + Workers + D1 + R2. Tanpa server tradisional, cukup sambungkan domain Anda. |
| [microfeed](https://github.com/microfeed/microfeed) | CMS mandiri (*self-hosted*) super ringan. Bisa mempublikasikan audio, video, teks, dokumen via RSS dan JSON. Ideal untuk *podcast* atau *changelog*. |
| [Gins-Blog](https://github.com/IchimaruGin728/Gins-Blog) | Platform blog berperforma tinggi dengan pendekatan *Agentic-First*. Mendukung protokol MCP (Model Context Protocol). |
| [cwd](https://github.com/anghunk/cwd) | Sistem komentar *serverless* pengganti Disqus. Kecepatan maksimal dan privasi terjaga karena *database* ditaruh di D1 milik Anda sendiri. |

## 🤖 AI & Agen (MCP)
Eksperimen kecerdasan buatan, Model Context Protocol (MCP), dan Agen Otonom di *Edge*.

| Nama | Deskripsi |
|------|-----------|
| [CloudFlare-AI-Insight-Daily](https://github.com/justlovemaki/CloudFlare-AI-Insight-Daily) | *Aggregator* AI otomatis. Menarik berita GitHub, riset, dan Twitter lalu di-summary pakai Gemini dan di-push jadi koran harian ke GitHub Pages. |
| [second-brain-cloudflare](https://github.com/rahilp/second-brain-cloudflare) | Lapis memori / RAG untuk AI. Simpan catatan sekali, ingat kembali saat Anda mengobrol dengan Claude, Cursor, atau ChatGPT via API MCP. |
| [MetaReview](https://github.com/TerryFYL/metareview) | Platform meta-analisis medis/data. Menggunakan Llama 3.1 8B via Workers AI untuk ekstraksi dan pembuatan grafik (D3.js) dari PDF riset. |
| [edgeever](https://github.com/tianma-if/edgeever) | Alternatif Evernote tanpa server dengan dukungan *native* AI Agent / MCP. |
| [web2gem](https://github.com/Guardinary/web2gem) | Gateway ringan yang menerjemahkan API Google Gemini menjadi format yang kompatibel dengan API OpenAI. Deploy ke Cloudflare cukup dengan 1 file. |
| [mcp-memory](https://github.com/Puliczek/mcp-memory) | Server MCP (*Model Context Protocol*) untuk menyimpan memori dan preferensi user secara persisten di Cloudflare D1 & Vectorize. |
| [my-ax](https://github.com/acoyfellow/my-ax) | "Sistem Operasi Agen Pribadi" yang di-*self-hosted* penuh di atas Cloudflare Workers, Durable Objects, D1, dan MCP. |
| [tutorial-cloudflare-agents-bot](https://github.com/Celebez/tutorial-cloudflare-agents-bot) | Tutorial langkah demi langkah membuat Bot Telegram yang ditenagai AI Agent (Cloudflare Workers + Pages + Bindings) tanpa API Keys eksternal. |
| [codra](https://github.com/devarshishimpi/codra) | Sistem *AI Code Review* mandiri untuk *Pull Request* GitHub Anda. Menggunakan arsitektur serverless (Workers, Queues, Hyperdrive, Workers AI). |
| [zenith-image-generator](https://github.com/WuMingDao/zenith-image-generator) | Antarmuka web (UI) untuk *AI Image Generator* multi-provider yang bisa langsung di-deploy ke Cloudflare Pages. |

## 🔗 Shortlink & Pastebin
Ganti Bitly atau Pastebin berbayar dengan milik Anda sendiri yang tidak membatasi fitur kustomisasi.

| Nama | Deskripsi |
|------|-----------|
| [Sink](https://github.com/ccbikai/Sink) | Pemendek tautan (*URL Shortener*) lengkap dengan dasbor analitik dan statistik trafik. Berjalan sepenuhnya secara *serverless*. |
| [pastebin-worker](https://github.com/SharzyL/pastebin-worker) | Aplikasi *Pastebin* (berbagi teks/kode) *open-source*. Mendukung kata sandi pelindung dan fitur hapus otomatis setelah dibaca (*burn after reading*). |
| [r2-explorer](https://github.com/G4brym/r2-explorer) | File Manager / *Browser* Web yang cantik untuk mengelola (melihat, *upload*, hapus) *bucket* Cloudflare R2 Anda dengan dukungan *password*. |
| [wr.do](https://github.com/oiov/wr.do) | Sistem distribusi DNS dan pemendek tautan multi-penyewa (multi-tenant) berbasis Workers. |

## 🌐 Proxy, DNS & Utilitas
Kumpulan alat untuk *networking*, manajemen sistem, dan produktivitas harian.

| Nama | Deskripsi |
|------|-----------|
| [CF-Server-Monitor](https://github.com/huilang-me/CF-Server-Monitor) | Dasbor *uptime monitor* ala UptimeKuma. Menggunakan Worker, D1, dan Durable Objects untuk melacak ping & *latency* banyak VPS secara real-time. |
| [cloudflare-doh-proxy](https://github.com/4n0nymou3/cloudflare-doh-proxy) | Proxy DNS over HTTPS (DoH) untuk *load balancing* dan menembus sensor internet (misal: Internet Positif). |
| [ternssh](https://github.com/HaradaKashiwa/ternssh) | Klien SSH berbasis Web yang berjalan di atas Cloudflare Workers. Remot VPS Anda langsung dari *browser* dari mana saja. |
| [cf-manager](https://github.com/hefy2027/cf-manager) | Dasbor *all-in-one* untuk manajemen banyak akun Cloudflare sekaligus (DNS, Workers, D1, R2, AI). |
| [ip-api](https://github.com/ccbikai/ip-api) | API super sederhana untuk cek IP Address pengunjung beserta geolokasi-nya menggunakan header bawaan Cloudflare. |
| [cloudflare-block-bad-bot-ruleset](https://github.com/SukkaW/cloudflare-block-bad-bot-ruleset) | Koleksi aturan *Firewall* (WAF) siap pakai untuk memblokir *crawler/scraper* nakal yang menghabiskan bandwidth situs Anda. |
| [docker-cloudflare-ddns](https://github.com/oznu/docker-cloudflare-ddns) | Docker *image* untuk menyambungkan IP internet rumah (Indihome/Biznet yang IP-nya dinamis) ke domain Cloudflare secara otomatis (DDNS). |
| [cloudflare-workers-basic-auth](https://github.com/dommmel/cloudflare-workers-basic-auth) | Beri perlindungan *password* (Basic Auth) pada situs statis apa pun hanya bermodal skrip Worker sederhana. |
| [airtable-proxy-worker](https://github.com/portable-cto/airtable-proxy-worker) | Proxy aman untuk menggunakan Airtable sebagai database *backend* tanpa membocorkan API Key Airtable Anda ke publik. |

## 🎁 Domain Gratis
Layanan komunitas yang dikelola di atas Cloudflare untuk membagikan subdomain gratis bagi developer.

| Nama | Deskripsi |
|------|-----------|
| [js.cool](https://github.com/willin/js.cool) | Layanan bagi-bagi subdomain `.js.cool` gratis selamanya untuk developer. Pendaftaran via *Pull Request* GitHub. |
| [domain](https://github.com/willin/domain) | Proyek saudari dari `js.cool`, memberikan variasi subdomain `.sh.gg` dan lainnya gratis. Di-*serve* via Cloudflare DNS API. |

---

## 🤝 Kontribusi
Jika Anda menemukan *tools* menarik lainnya atau sedang membangun *side project* berbasis Cloudflare, silakan buat *Pull Request*!

## 📜 Lisensi
Lisensi MIT - [Ridlo Abelian](https://github.com/ridloabelian)

---
*Kredit: Diadaptasi dan dikurasi dari [zhuima/awesome-cloudflare](https://github.com/zhuima/awesome-cloudflare), [Ezeafk/awesome-cloudflare-ai](https://github.com/Ezeafk/awesome-cloudflare-ai), dan [irazasyed/awesome-cloudflare](https://github.com/irazasyed/awesome-cloudflare) dengan penyesuaian untuk ekosistem developer Indonesia.*
