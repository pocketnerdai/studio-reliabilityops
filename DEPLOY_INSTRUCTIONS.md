# Deploy Sanity Studio

Your studio is now ready to deploy! Follow these steps:

## 1. Login to Sanity

```bash
npx sanity login
```

Choose your preferred login method (Google, GitHub, or Email).

## 2. Deploy the Studio

```bash
npm run deploy
```

When prompted for a hostname, you can:
- Press Enter to accept the default (1xy15psx)
- Or choose a custom name

## 3. Access Your Studio

After deployment, your studio will be available at:
- https://1xy15psx.sanity.studio (or your custom hostname)

## Studio Structure

```
studio-reliabilityops/
├── schemas/           # Content schemas
│   ├── post.ts       # Blog post schema
│   ├── author.ts     # Author schema
│   ├── category.ts   # Category schema
│   └── blockContent.ts # Rich text schema
├── sanity.config.ts  # Studio configuration
└── package.json      # Dependencies
```

## Next Steps

1. Access your studio at the deployed URL
2. Create an author (yourself)
3. Create some categories (SRE, AI, etc.)
4. Create your first blog post!

Your ReliabilityOps site will automatically fetch and display this content.