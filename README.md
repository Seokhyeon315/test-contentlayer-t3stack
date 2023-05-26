# T3 Stack with Contentlayer

## Step 1

```bash
npm create t3-app@latest
```

Including:

- [Next.js](https://nextjs.org) with pages directory
- [NextAuth.js](https://next-auth.js.org)
- [Prisma](https://prisma.io)
- [Tailwind CSS](https://tailwindcss.com)
- [tRPC](https://trpc.io)

Run following commands:

1. `npx prisma db push`
2. `npm run dev`

After commit and push to github repo, install following packages:

```bash
npm install contentlayer next-contentlayer rehype-autolink-headings rehype-slug rehype-pretty-code shiki concurrently remark-gfm
```

## Step2

1. Edit tsconfig.json
2. Edit next.config.js
3. Edit package.json's scripts to following:

```json
"dev": "concurrently \"contentlayer dev\" \"next dev\"",
"build": "contentlayer build && next build",
```

4. Create contentlayer.config.js and edit it. I refer this repository: https://github.com/shadcn/taxonomy/tree/main
5. Create a sample1.mdx file in src/content/notes directory. The sample file includes English and Korean language.
6. Run `npm run dev`
7. Here is where problem occurs. After I run `npm run dev`, the terminal got fronzen. I didn't include `.contentlayer` directory to show it only creates caches.
