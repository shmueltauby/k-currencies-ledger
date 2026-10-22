# K Currencies Ledger

A shared tally for the two K Currencies partners: log transfers, deal profits, shared expenses and starting balances, and see who owes whom in shekels, dollars and any other currency.

- The site is a single static page (`index.html`) served by GitHub Pages.
- Entries are stored in Supabase (`kc_entries`, `kc_settings`, `kc_members`), not in this repository.
- Partners log in with an emailed login link. Only addresses listed in `kc_members` can read or write; row-level security enforces this in the database.

## Adding a partner's email

Run in the Supabase SQL editor:

```sql
insert into public.kc_members (email, display_name) values ('their@email.com', 'Beanie');
```
