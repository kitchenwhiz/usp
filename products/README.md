# Kitchenwhiz Work Table – Product Page

A single-page product configurator for the Kitchenwhiz stainless steel work table.

- Pick a depth (600 / 700 / 750 / 900 mm) and length (400–2100 mm). The EQ code, price and L×D×H labels update.
- Tick any of the 10 add-ons (U1, U2, B, G, O1, O2, SK\*, 3S, D, C\*\*). The drawing and the running total update.
- Rules: U2 needs U1, and O2 needs O1.

Everything is in `index.html`: no build step, and no other files are needed. Prices come from `Kitchen_Whiz_Catalogue.xlsx` and are stored inside the page's script (`const TABLES`).

## Put it online with GitHub Pages

1. Create a new repository on GitHub and upload `index.html` (and this README).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. After a minute the page is live at `https://<your-username>.github.io/<repo-name>/`.

## Updating prices

In `index.html`, find `const TABLES = [...]`. Each entry is one table size:

```
{"l":750,"d":600,"code":"WT7H6","p":13950,"a":[1735,3350,695,5580,2795,5580,8000,5860,5580,1500]}
```

`l` = length, `d` = depth, `p` = base price, and `a` = add-on prices in this order: U1, U2, B, G, O1, O2, SK\*, 3S, D, C\*\*.

## Still to fill in

- `[GRADE]` (steel grade) and `[TOP MATERIAL]` in the specs.
- The "Add to cart" and "Request a quote" buttons are not connected yet.
