# Manual Steps Required

## 1. Push Changes to GitHub
Since there's a permission issue with the repository, you'll need to:

Option A: Add your GitHub user to the pocketnerdai organization with write access
Option B: Fork the repository and push to your fork
Option C: Create the repository under your personal account instead

To push the changes:
```bash
git push origin master
```

## 2. Create Sanity Deploy Token
1. Go to https://www.sanity.io/manage
2. Select your project (ID: 1xy15psx)
3. Navigate to API → Tokens
4. Click "Add API token"
5. Give it a name like "GitHub Actions Deploy"
6. Select "Deploy" permission
7. Copy the token

## 3. Add Token to GitHub Secrets
1. Go to your GitHub repository: https://github.com/pocketnerdai/studio-reliabilityops
2. Go to Settings → Secrets and variables → Actions
3. Click "New repository secret"
4. Name: `SANITY_AUTH_TOKEN`
5. Value: Paste the token from step 2
6. Click "Add secret"

## 4. Update CORS Origins in Sanity
1. Go to https://www.sanity.io/manage
2. Select your project
3. Navigate to API → CORS Origins
4. Add these origins with "Allow credentials" checked:
   - https://studio-reliabilityops.sanity.studio
   - https://reliabilityops.dev
   - https://reliabilityops-dev.pages.dev
   - http://localhost:4321
   - http://localhost:3333

## Summary of What's Been Done:
✅ Fixed schema error in code block configuration
✅ Created GitHub repository (https://github.com/pocketnerdai/studio-reliabilityops)
✅ Created CI/CD workflow (.github/workflows/deploy-sanity.yml)
✅ Deployed studio with fixes to https://studio-reliabilityops.sanity.studio

## Studio Access:
- Production: https://studio-reliabilityops.sanity.studio
- Via redirect: https://reliabilityops.dev/studio

Once you complete the manual steps above, the CI/CD pipeline will automatically deploy your studio whenever you push changes to schemas or configuration files.