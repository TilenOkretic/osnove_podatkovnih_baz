# Optimizacija poizvedb

## Program v SUPB
* Je drevo operacij relacijske algebre 
* Vozlisca so oznacena z algoritmi za izvajanje posameznih operacij
* Naloga se poslje korenu in koren nato posreduje operacijo svojim otrokom

---
### Drevo iteratorjev
* Vsaka operacija je impleementirana z iteratorjem
* Vmesnik iteratorja: 
    - open()
    - next()
    - close()
---
* **drevesno strukturiran cevovod** =

## Optimizacija drevesa operacij
* Logicna optimizacija
    * Iskanje izrazov RA ki so ekvivalentni zacentni poizvedbi
    * Izrazi ki se jih da najhitreje implemntirat

* Fizicna optimizacija
    * Konkretna implementacija fizicnega logicnega pogleda operacij
    * Operacije:
        * **dostopna pot** - branje n-terk iz relacij
        * **stiki**
    * fizicna implementacija se prepleta z logicno implementacijo

## Prevajanje SQL v Relacijsko Algebro
* Dekompozicija poizvedbe v bloke
  * celoten SQL stavek se razdeli v bloke
  * bloke obravnavamo kot enote 
  * vgnezdeli bloki ~ procedure

## Ocena plana izvajanja
* rezultat je vedno priblizek
* Statisiko imamo shranjeno v sistemskih katalogih
* Dve naloge:
  * Koliko blokov bo prebranih iz diska ~ ocena hitrosti poizvedbe
  * Velikosti vmesnih rezultatov ~ ob vsakem vhodu kako velik bo izhod dane operacije
* **inedxni pregled**
* **stik z zanko**
* **stik z indexom**
* Spreminja se delovanje kot posledica zmoznosti imeti več pomnilnika

## Satistike in katalogih
* podatki o relacijah in indexis v podatkovni bazi

## Ocene seletkivnosti pogojev operacij RA
* uporabimo pri selekciji
* **selektivnost** je prednost med 0 in 1
* predpostavke:
  * Vrednosti atributov so enakomirno porazdeljene
  * pogoji so med seboj neodvisni
* **prvi kljuc** se stakne z **velikostjo table** deljeno z **stevilom kljucev danega attributa**
* **iskanje po podrocju** najvecji kljuc in najmanjsi kljc nekega atributa ~
  - selektivnost: najvecji kljuc - vrednost
* selektivnost projekcije je *SP = 1*
* **Stik**
  * R >< S, A1 e R in A e S
  * def: A1 - A2

## Ocene velikosti rezultatov operacij RA
* *poglej na slajde*
* Selekcija
* Projkcija
* Kartezicni produkt
* Stik
* Unija
* Razlika
