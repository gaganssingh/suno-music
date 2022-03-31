#### Prisma Workflow

1. Generate the prisma schema config file: `npx prisma init`
2. Create db connections and schema in `/prisma/schema.prisma` file
3. Generate prisma types/client `npx prisma db push`. [This is what it does](https://www.prisma.io/docs/concepts/components/prisma-migrate/db-push)
4. Perform db migration `npx prisma migrate dev`. These are saved in `/prisma/migrations/`
