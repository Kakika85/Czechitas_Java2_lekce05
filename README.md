# Lekce 5 – HTML formuláře

Zatím jsme jen zobrazovali data, dnes je konečně začneme také upravovat. Použijeme k tomu HTML formuláře. 

1. Použij toto repository jako šablonu (Use this template), ze které si vytvoříš repository ve svém účtu na GitHubu.
1. Naklonuj si repository **ze svého účtu** na GitHubu na lokální počítač.

## Zadání pro lekci
1. Z `div`u pod nadpisem *Append new person* udělej formulář (tag `form`). Třídy zůstanou stejné, formulář bude mít akci `/` a metoda bude `post`.
1. Vytvoř v controlleru metodu `append`. Metoda bude mapována na metodu `POST` a jako parametr bude přijímat entitu `Person`.
1. V metodě controlleru `append` použij metodu `append` ze služby `service` pro přidání nové osoby do seznamu osob.
1. Na konci controlleru proveď přesměrování zpět na úvodní stránku aplikace (POST-redirect-GET), aby se zobrazil seznam osob. Seznam se zobrazí už s nově přidanou osobou.

## Zadání pro cvičení v breakoutroomech
1. Uprav stránku s detailem tak, že kolem prvků `input` vytvoříte formulář (můžete z `div`u udělat `form`. Třídy zůstanou stejné, formulář bude mít akci `/{id}` a metoda bude `post`. Za `{id}` je potřeba dosadit identifikátor konkrétního záznamu.
1. Vytvoř v controlleru metodu `edit`. Metoda bude mapována na metodu `POST` a jako parametr bude přijímat entitu `Person` a také `@PathVariable` `id` (která přijde v URL).
1. Ve službě `FamousPeopleService` přidej metodu `edit`, která jako parametr dostane `id` záznamu (index v seznamu) a entitu `Person`. Metoda uloží danou osobu na zadaný index v seznamu (tj. přepíše konkrétní záznam).
1. V metodě controlleru `edit` zavolej metodu `edit` ze služby a předej jí správné parametry.
1. Na konci metody controlleru `edit` proveď přesměrování zpět na úvodní stránku aplikace (POST-redirect-GET), aby se zobrazil seznam osob. Seznam se zobrazí s upravenou osobou.
1. Uprav stránku se seznamem osob tak, že kolem tlačítka pro smazání záznamu vytvoříš formulář. Tento formulář nebude vidět, bude v něm ale `input` typu `hidden`, ve kterém bude uložené `id` záznamu, který chceme smazat.
1. Formulář se bude odesílat metodou `post` na adresu `/delete`.
1. Implementuj metodu controlleru pro metodu `POST` napojenou na adresu `/delete`, jako parametr bude očekávat číselný identifikátor záznamu, který se má smazat.
1. V metodě controlleru použij metodu `FamousPeopleService.deletById`, která už je ve službě implementovaná.
1. Na konci metody controlleru opět proveď přesměrování zpět na úvodní stránku aplikace (POST-redirect-GET), aby se zobrazil seznam osob. Seznam se zobrazí už bez smazané osoby.

## Odkazy
* [Lekce 5](https://java.czechitas.cz/2024-jaro/java-2-online/lekce-5.html)
