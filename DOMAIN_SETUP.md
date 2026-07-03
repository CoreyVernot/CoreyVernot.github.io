# Domain Setup Notes

This site is in the process of moving from GitHub Pages at `CoreyVernot.github.io` to the custom domain `coreyvernot.com`.

Current repository:

- GitHub repo: `https://github.com/CoreyVernot/CoreyVernot.github.io`
- Local folder: `C:\Users\vernot\claude-workspace\Dropbox\00.Personal Projects\Academic Website`
- Custom domain file: not currently present
- Intended future domain in `CNAME`: `coreyvernot.com`

Important status:

- A `CNAME` file with `coreyvernot.com` was briefly added on 2026-07-03.
- Because Porkbun DNS was still parked at `uixie.porkbun.com`, GitHub redirected `CoreyVernot.github.io` to the parked Porkbun page.
- The `CNAME` file was removed so the existing `CoreyVernot.github.io` URL keeps working while DNS setup is unfinished.
- Re-add `CNAME` only after Porkbun DNS for `coreyvernot.com` points to GitHub Pages.

Domain registrar:

- Registrar: Porkbun
- Domain: `coreyvernot.com`
- DNS screen showed Porkbun default parking records before setup:
  - `ALIAS coreyvernot.com -> uixie.porkbun.com`
  - `CNAME *.coreyvernot.com -> uixie.porkbun.com`
  - Porkbun email forwarding records: `MX fwd1.porkbun.com`, `MX fwd2.porkbun.com`, and SPF TXT record

Planned DNS records for GitHub Pages:

```text
Type: A
Host: @
Answer: 185.199.108.153

Type: A
Host: @
Answer: 185.199.109.153

Type: A
Host: @
Answer: 185.199.110.153

Type: A
Host: @
Answer: 185.199.111.153

Type: CNAME
Host: www
Answer: CoreyVernot.github.io
```

Notes for whoever continues this:

- Delete the default Porkbun parking records before relying on GitHub Pages:
  - `ALIAS coreyvernot.com -> uixie.porkbun.com`
  - `CNAME *.coreyvernot.com -> uixie.porkbun.com`
- Keep the Porkbun `MX` and SPF `TXT` records only if Corey wants Porkbun email forwarding.
- After Porkbun DNS records are changed, add a `CNAME` file containing only `coreyvernot.com`, or set the custom domain in `Settings > Pages`.
- Once DNS verification passes in GitHub Pages, enable `Enforce HTTPS`.
