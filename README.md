# svelte-local-global

Illustrates this issue: https://github.com/sveltejs/kit/issues/628

The issue is resolved in Svelte 4 because transitions now default to |local
instead of |global.

Note: when switching between the main (i.e. svelte 3) and svelte4 branches,
make sure to run `pnpm i` to install the correct version of svelte.
