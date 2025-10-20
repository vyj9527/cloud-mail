
<p align="center">
  <img src="doc/demo/logo.png" width="80px" />
</p>

<div align="center">
<h1>Cloud Mail</h1>
</div>
<div align="center">
    <h4>A responsive email service built with Vue 3 that supports email sending and can be deployed on Cloudflare. 🎉</h4> 
</div>


## Project Showcase

- [Online Demo](https://skymail.ink)<br>
- [Deployment Guide](https://doc.skymail.ink/en/)<br>
- [Beginner’s Guide – UI Deployment](https://doc.skymail.ink/en/guide/via-ui.html)


| ![](/doc/demo/demo1.png) | ![](/doc/demo/demo2.png) |
|--------------------------|---------------------|
| ![](/doc/demo/demo3.png) | ![](/doc/demo/demo4.png) |
| ![](/doc/demo/demo5.png) | ![](/doc/demo/demo6.png) |
| ![](/doc/demo/demo7.png) | ![](/doc/demo/demo8.png) |

## Features

- **💰 Low-Cost Usage**: No server required — deploy to Cloudflare Workers to reduce costs.

- **💻 Responsive Design**: Automatically adapts to both desktop and most mobile browsers.

- **📧 Email Sending**: Integrated with Resend for bulk email sending, embedded images, attachments, and status tracking.

- **🛡️ Admin Features**: Admins can manage users and emails, with RBAC permission control to limit access to features and resources.

- **🔀 Multiple Accounts**: Users can add multiple email accounts. 

- **📦 Attachment Support**: Send and receive attachments, stored and downloaded via R2 object storage.

- **🔔 Email Push**: Forward received emails to Telegram bots or other email providers.

- **📡 Open API**: Supports batch user creation via API and multi-condition email queries

- **📈 Data Visualization**: Use Echarts to visualize system data, including user email growth.

- **⭐ Starred Emails**: Mark important emails for quick access.

- **🎨 Personalization**: Customize website title, login background, and transparency.

- **⚙️ Feature Settings**: Toggle on or off features like registration, email sending, and more, with the option to make the site private.

- **🤖 CAPTCHA**: Integrated with Turnstile CAPTCHA to prevent automated registration.

- **📜 More Features**: Under development...

## Tech Stack

- **Framework**: [Vue3](https://vuejs.org/) + [Element Plus](https://element-plus.org/)

- **Web Framework**: [Hono](https://hono.dev/)

- **ORM**: [Drizzle](https://orm.drizzle.team/)

- **Platform**: [Cloudflare Workers](https://developers.cloudflare.com/workers/)

- **Email Service**: [Resend](https://resend.com/)

- **Caching**: [Cloudflare KV](https://developers.cloudflare.com/kv/)

- **Database**: [Cloudflare D1](https://developers.cloudflare.com/d1/)

- **File Storage**: [Cloudflare R2](https://developers.cloudflare.com/r2/)


## Project Structure

- Root
  - mail-vue: Frontend web app (Vue 3 + Vite + Element Plus). Languages: JavaScript, Vue Single-File Components (.vue), CSS/SCSS/LESS. Key dirs: src/ (components, views, router, store, i18n, request/axios, utils, layout), entry main.js, built with Vite, env files .env.*
  - mail-worker: Backend on Cloudflare Workers (Hono + Drizzle ORM + Cloudflare D1/KV/R2 + Resend). Languages: JavaScript (ES Modules). Key dirs: src/api (routes), src/service (business logic), src/dao (data access), src/entity and src/model (entities/common results), src/hono (app and middleware), src/email (email receive handler), src/security (auth/context), src/utils (utilities); entry src/index.js; configs wrangler*.toml; tests in test/ with Vitest
  - doc: Documentation and demo assets
  - .github: CI/deployment workflows
  - Others: README.md/README-en.md, LICENSE

- Frontend–Backend integration
  - mail-worker serves both API and static assets. Requests starting with /api/ are routed to Hono, others are served from env.assets (see mail-worker/src/index.js).

- Languages summary
  - Frontend: JavaScript, Vue SFC (.vue), CSS/LESS/Sass
  - Backend: JavaScript (Cloudflare Workers ESM), SQL (Cloudflare D1 queries)


## Support


<a href="https://doc.skymail.ink/support.html">
<img width="170px" src="./doc/images/support.png" alt="">
</a><br><br>


**Special Sponsors**

[DartNode](https://dartnode.com)：Providing cloud computing service resource support.

[![Powered by DartNode](https://dartnode.com/branding/DN-Open-Source-sm.png)](https://dartnode.com "Powered by DartNode - Free VPS for Open Source")

## License

This project is licensed under the [MIT](LICENSE) license.

## Communication

[Telegram](https://t.me/cloud_mail_tg)
