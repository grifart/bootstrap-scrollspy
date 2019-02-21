# grifart-bootstrap-scrollspy

Toto repo vzniklo na základě potřeby poupravit originální bootstrap scrollspy. Scrollspy jsme potřebovali upravit tak, aby nezávisel na globálním kontextu a byl funkční například i v Tinymce editoru.

## Vývoj

Momentálně jsou zde dvě větve `master` a `original-bootstrap-scrollspy`.

`Original-bootstrap-scrollspy` obsahuje původní zdrojové soubory pluginu scrollspy. 

`Master` slouží pro vlastní vývoj custom scrollspy.

Před vývojem je potřeba spustit příkaz `yarn install`. Poté upravit kód v `src` složce. Potom spustit příkaz `yarn build`. Tím se vytvoří vybuilděný script, který je uveden jako `main` v `package.json`. Není konvencí spouštět nad `node-modules` v projektu `babel-loader`, protože je pomalý. Proto se build souborů řeší zde a ne až v projektu a v projektu se využívají vybuilděné soubory. 

## Upgrading originálního bootstrap-scrollspy

Pomocí větve `original-bootstrap-scrollspy`. Bootstrap vydá novou verzi, člověk díky téhle větvi se může podívat, co se změnilo v pluginu scrollspy a upravit, co je potřeba a změny promítnout i do našeho custom scrollspy.

## Použití v projektu

V `package.json` v projektu přidáme tento balíček přes `yarn add git://github.com/grifart/bootstrap-scrollspy.git#master`. V případě změny masteru tohoto balíčku, je pak potřeba v projektu, ve kterém je tento balíček využíván, spustit příkaz `yarn upgrade grifart-bootstrap-scrollspy`.
