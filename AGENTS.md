<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

# AgroGestor

- Farm data is stored in browser localStorage via `src/lib/store.ts` (`useCollection`); swap that module to move to a database without touching pages.
- Lovable Cloud is provisioned, but farm records remain local until an authenticated, explicitly confirmed import is implemented; preserve the storage adapter boundary to avoid destructive page-by-page migration.
- Simple record pages reuse `CrudPage` with a field config, to keep sections consistent.
- The AI assistant calls the Lovable AI Gateway through a server function, sending a JSON snapshot of the farm data as context.
