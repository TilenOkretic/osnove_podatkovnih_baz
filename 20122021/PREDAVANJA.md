# Funkcijske omejtive
* osnovni namen studija funkcijskih odvisnosti je ta, da si zelimo izognili problemom REDUNDANCE
* **dekompozicija relacije** - neko relacijo razdelimo na vec relacij, ni vec funkcijskih odvisnosti znotraj relacij

## Funkcijske odvisnosti (FDs)
* X -> Y over relation R
* je poiyvedba (o vseh / nad vsemi) DOVOLJENIH relacijah
* Axiomi v FD (Armstrong-ovi axiomi)
  * **Refelksivnost**: X podmnozica Y potem Y -> X
  * **Augmentacija**: ce X -> Y potem XZ ->YZ za vsak Z
  * **Transitivnost**: ce X -> Y in Y -> Z potem X -> Z
* Pravilo **UNIJE**: X -> Y in X -> Z potem X -> YZ
* Pravilo **DEKOMPOZICIJE**: X -> YZ potem X -> Y in X -> Z    

# Normalne oblike
* temeljijo na funkcijskih odvisnostih
* ce je relacija v neki normalni obliki potem ima dolocene lastosti

## Boyce-Codd Noramalna Oblika (BCNF)
* refeleksivnost za dolocanje odvisnosti