# Zaklepanje v B+ drevesih
* preko protokola
* zaklenemo vedno koren in nato naslednje vozlisce in to ponavljamo vse do lista
* Visji nivoji drevesa samo usmirjajo iskanje 
* Zaklepanje vozlisc ~ poglej na slajde ~     

---

## Enostaven algoritem za zaklepanje dreves
* zaklenemo vozlisca v paru (stars in otrok)
* Iskanje
* Vstavlanje/Brisanje: Zacni pri korenu in potuj navzdol...
* **Varno vozlisce** je tako ki ob spremembi ne siri spremembe navzgor na starse 

---

## Boljsi algoritem za zaklepanje
* Boljsi pri obdelovanju z mnogo vozlisci

---

### Se boljsi algoritem
* Uporabimo dodaten protokol za vstavljanje/brisanje
* Ko je list zaklenjen prevedi vse IX zaklepe v X zaklepe **od zgoraj navzdol**
* **Problem** je z smrtnimi objemi

---

### Kontrola vzporednosti~KV brez zaklepanjania
* KV s casovnimi znackami (Timestamp CC)
* Multiverzijska KV s casovnimi znackami (Multiversion Timestamp CC)

---

### Optimisticna Kontrola Vzporednosti~KV
* izvedemo trasnakcijo na kopijah:
  * vsako stran preberemo in naredimo lokalno kopijo
  * preverimo ce se kdo dostopa na transakcijo
  * ce ne zakljucimo trasnakcijo
* Problem **smrtnih objemov** pri zaklepanju
* Redki konflikti --> preverimo konflikte pred transkacijo
* Ce imamo malo konfliktov je ta **Optimisticna KV** hitrejsa

---

### Validacija
* casovni zigi (timesamp) ~> numericna vrednost
* vsaka transakcija dobi casovni zig~id na koncu faze BERI, tik pred validacijo
* Za vsako transakcijo rabimo imet **mnozico objektv, ki jih bere** in **mnozico objektov, ki jih spremeni** ~ to predstavlja problem
* razlicni **TESTI** (poglej na slajde)

---

### Zaporedna Validacija
* problem ker rabimo kriticno sekcijo
* aplicira se Test 2
* ce samo beremo lahko spustimo kriticno sekcijo -> pohitritev
* razbijemo na pod-mnozice, izkaze se da reabimo v kriticni sekciji imet samo zadnjo podmnozico  -> pohitritev !!

---


