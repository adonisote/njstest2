1. Create github repository
2. Clone github repository
3. Create a next.js app
`npx create-next-app`

Config:
✔ What is your project named? … setup2
✔ Would you like to use TypeScript? … No / >Yes<
✔ Would you like to use ESLint? … No / >Yes<
✔ Would you like to use Tailwind CSS? … No / >Yes<
✔ Would you like to use `src/` directory? … >No< / Yes
✔ Would you like to use App Router? (recommended) … No / >Yes<
✔ Would you like to customize the default import alias (@/*)? … No / >Yes<
✔ What import alias would you like configured? … @/*

4. `git add . && git commit -m "setup"`

5. `git push`

6. [Install Prisma](https://www.prisma.io/docs/getting-started/quickstart)

 `npm install prisma --save-dev`
7. [Initialize Prisma](https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql)

`npx prisma init` 

8. Go to [versel](https://vercel.com/)
Create account, add Repository, import the correct Repository from Github

9. Select framework "Next.js"

10. Select Root Directory: "app-name"

11. Deploy
If it doesn't work. Make sure you selected the right app-folder

12. Continue to Dashboard
13. Click on Storage
14. Create new PostgresSQL & Add it to the Project
15. Click on Database
16. Click on Prisma
17. Copy Snipshepet to VSCODE "prisma/schema.prisma"

// This is your Prisma schema file,
// learn more about it in the docs: https://pris.ly/d/prisma-schema

datasource db {
  provider = "postgresql"
  url = env("POSTGRES_PRISMA_URL") // uses connection pooling
  directUrl = env("POSTGRES_URL_NON_POOLING") // uses a direct connection
}

18

18. Create file in  VSCODE "app-name" ".env.local"
19. Go back to versel, click on .env.local and copy snippet.
20. Paste in VSCODE ".env.local"
21. .env.local is in .gitignore and not uploaded to remote repository, if 
any change is made, it has to be made also in vercel ".env.local"
