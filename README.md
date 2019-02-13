# girfart-bootstrap-scrollspy
Toto repo vzniklo na základě potřeby poupravit originální bootstrap scrollspy.

Momentálně jsou zde dvě větve `master` a `original-bootstrap-scrollspy`.

`Original-bootstrap-scrollspy` obsahuje původní zdrojové soubory pluginu scrollspy. Do budoucna slouží pro jednoduché upgradování scrollspy. Bootstrap vydá novou verzi, člověk díky téhle větvi se může podívat, co se změnilo v pluginu scrollspy.

`Master` slouží pro vlastní vývoj custom scrollspy. Scrollspy jsme potřebovali upravit tak, aby nezávisel na globálním kontextu a byl funkční například i v Tinymce editoru.

## Vývoj

Před vývojem je potřeba spustit příkaz `yarn install`. Poté upravit kód v `src` složce. Potom spustit příkaz `yarn build`. Tím se vytvoří vybuilděný script, který je uveden jako `main` v `package.json`. 

## Použití v projektu

V `package.json` v projektu přidáme tento balíček přes `yarn add <adresa repozitáře>`. V případě změny masteru tohoto balíčku, je pak potřeba v projektu, ve kterém je tento balíček využíván, spustit příkaz `yarn upgrade <jmeno baličku>`.
