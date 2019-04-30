# grifart-bootstrap-scrollspy

Originální bootstrap scrollspy nepodporuje situaci, kdy scrollovaný obsah je v iframe (například obsah TinyMCE). Scrollspy tedy bylo třeba upravit.

Tento repozitář obsahuje dvě větve hlavní větve:

- `original-bootstrap-scrollspy` - obsahuje původní neupravenou verzi scrollspy z [Bootstrap](https://getbootstrap.com)
- `master` - upravená verze podporující iframes

Repozitář zároveň obsahuje i zkompilované JavaScript soubory, které je třeba verzovat spolu s zdrojovým kódem. (díky tomu nemusíme nastavovat publikační proces balíku přes CI) Proto je třeba před commitem nezapomenout spustit `yarn build` (doporučuji nastavit jako `pre-commit-hook`).


## Instalace

Tento balíček zatím není v systému [npm](https://www.npmjs.com), proto je třeba přidat tento veřejný repozitář přímo do `package.json`.

Tento balíček používá [sémantické verzování 2.0](https://semver.org/spec/v2.0.0.html), je tedy možné používat `^` v version constaints.

```bash
yarn add git://github.com/grifart/bootstrap-scrollspy.git#^1.0.0
```

Upgrade balíčku provádíme standardně, jako každý jiný balíček přes `yarn upgrade`, či změnu constrain v `package.json`.


## Upgrade podkladové verze bootstrap-scrollspy

Ve větvi `original-bootstrap-scrollspy` přepíšeme soubory aktuálními. Poté již stačí se přepnout na master a udělat

```bash
git checkout original-bootstrap-scrollspy
```

Zde upravte soubory na aktuální bootstrap.

```bash
git add .
git commit -m "updated to bootstrap v. X.Y.Z"
git push
```

A teď je chvíle pro sloučení změn:

```bash
git checkout master
git merge --no-ff original-bootstrap-scrollspy
git push
```
