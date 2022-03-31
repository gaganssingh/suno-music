#### Prisma Workflow

1. Generate the prisma schema config file: `npx prisma init`
2. Create db connections and schema in `/prisma/schema.prisma` file
3. Generate prisma types/client `npx prisma db push`. [This is what it does](https://www.prisma.io/docs/concepts/components/prisma-migrate/db-push)
4. Perform dev db migration `npx prisma migrate dev`. These are saved in `/prisma/migrations/`
5. Create seed file `/prisma/seed.ts`
6. Add the prisma seed script in `package.json`
   ```
   "prisma": {
     "seed": "ts-node --compiler-options {\"module\":\"CommonJS\"} prisma/seed.ts"
   }
   ```
7. Seed the db `npx prisma db seed` & check open the prisma db explorer `npx prisma studio`
