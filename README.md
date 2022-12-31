# Pixos

## třídní fotky na jednom místě

Průvodní text k první verzi:

Tato verze obsahuje jakýsi minimální funkční produkt - od přidání fotek, přes uživatelský výběr, po zadání poptávky. Důležité části ještě chybí a 
jsou popsány níže v sekci TODO - co je ještě potřeba dodělat. 

## Backend

Do backendu je možné přihlásit se na veřejné adrese: https://pixos-backend.herokuapp.com/admin/auth/login, 
**přihlašovací údaje k backendu** ti posíláme v messengeru.
V backendu v složce "content manager" a podsložce "skola" můžeš přidat / smazat / upravit školu. Každá škola má třídy a každá třída má
svůj kód a fotky. Zde si můžeš zkusit nahrávání fotek, které se bez ztráty na kvalitě nahrajou automaticky na servery Amazonu - Amazon S3
jsme zde zvolili proto, že by měl být ještě levnější než Bunny, dokonce pokud v systému v každý moment bude <5 GB fotek, tak bude běžet zdarma.

Ke každé třídě je také potřeba přiřadit kód, který se vytiskne na lístečky a pod kterým se studenti dostanou k fotkám. Vytvářečka kódů pro tisk ještě 
není hotová, do budoucna se kód vygeneruje sám.

## Frontend

Frontend si můžeš prohlédnout na https://sobotka-frontend.herokuapp.com/. Zadání kódu zatím funkční není, ale tlačítko "Ukázat fotky"
nás vezme na stránku detailu, která by se nám správně ukázala po zadání kódu. Zde vidíme fotky, které se automaticky berou z backendu - nyní
se berou natvrdo od první školy a první třídy téhle školy. Můžu si navolit, kolik fotek od každé chci, dole vyplnit jméno a formulář odeslat.
Výsledek se už automaticky zapíše do Google Sheets tabulky: https://docs.google.com/spreadsheets/d/1NcB51lvzhnulWYeyNBpRKBeATvXm6G7lMTcWpCc7i4o/edit?usp=sharing
ve formátu jméno | vytvořeno | název souboru fotky: počet této fotky, název souboru fotky: počet této fotky,...

## Co je potřeba dodělat

Stránku "Fotky ještě nebyly zveřejněny, očekáváné datum:" po zadání kódu příliš brzy. Propojít zadání kódu s backendem. Vytvořit automatický
generátor kódu + příprava podkladu pro tisk. Rozčlenit Google Sheets tabulku podle tříd a škol. Zlepšít formátování tabulky po domluvě nejlepšího formátu.
Grafická "fasáda" celého webu :). Automatické maily studentům.
