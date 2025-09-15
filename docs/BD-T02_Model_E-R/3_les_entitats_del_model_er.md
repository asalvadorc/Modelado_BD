# 3. Les Entitats del Model E/R

Per a fer un esquema amb el Model Entitat-Relació, començarem sempre per les
primeres, per les entitats.

És a dir, a partir de les especificacions del problema, intentarem esbrinar
les entitats.
<!--
<video width="320" height="240" controls>
  <source src="T02_Peli1.mp4" type="video/mp4">
  Tu navegador no soporta la etiqueta de video.
</video>
-->
## 3.1 Entitats

Per a fer un esquema amb el Model Entitat-Relació, començarem sempre per les
primeres, per les entitats.

És a dir, a partir de les especificacions del problema, intentarem esbrinar
les entitats.

L'**ENTITAT** serà una persona, cosa, lloc, concepte o succés, amb existència
real o abstracta, que ens és d'interès.

Així per exemple, els empleats són entitats. Com tots els empleats tindran per
a nosaltres les mateixes característiques (nom, adreça,...), encara que
cadascú amb valors distints, els podem englobar en la mateixa estructura.

Definirem **TIPUS D'ENTITAT** a l'estructura genèrica (EMPLEAT) i **OCURRÈNCIA
D'ENTITAT** a cadascuna de les realitzacions concretes (cadascun dels
empleats, per exemple Joan Peris). Evidentment, en el disseny no ens
interessen les ocurrències, sinó el Tipus d'Entitat. El representarem per un
rectangle amb el nom de l'entitat a l'interior (preferiblement en singular).


### Aplicació a l'exemple



En el nostre exemple, el del punt 2, quedaran les següents Entitats:



![](entitats.png)

## 3.2 Atributs



Un **ATRIBUT** és cadascuna de les característiques d'una entitat que ens
interessen.

Per exemple en l'entitat EMPLEAT tindrem els atributs _nom, DNI, adreça,
telèfon, sou_ i _data de naixement_.

No considerarem atributs les característiques que no ens interessen (estatura,
talla pantalons, etc.)

Una ocurrència d'entitat tindrà un **VALOR** per a cada atribut, per exemple
_Joan Peris, 18.901.234, 964-22.33.44, 1.200,00€., 12-5-1960._

Però de vegades potser que el contingut d'un atribut siga el valor **NUL**
(per exemple si no té telèfon o el desconeixem).

Els atributs poden ser **SIMPLES** o **COMPOSTOS** , si estan formats per una
única informació o per més d'una. Així, un exemple d'atribut compost seria el
nom que podria estar format per: _nom=(nom de pila, primer cognom, segon
cognom)_.

Poden haver atributs **MULTIVALUATS** , que vol dir que poden agafar més d'un
valor. Per exemple suposem que en el cas anterior considerem el camp **altres telèfons** (per si en l'empresa hi ha moments que hem de localitzar
l'empleat urgentment). Potser un empleat no tinga cap valor en aquest camp. I
potser un altre en tinga dos (el mòbil i el d'una segona residència). En
general fugirem d'aquestos camps per comoditat, però el model ho accepta.

També poden haver atributs **DERIVATS** , és a dir, atributs que es poden
calcular a partir d'altres. Podria ser el cas del camp _edat_ , que es pot
calcular a partir de la data del sistema i de _data de naixement_.



El model necessita poder identificar cada ocurrència sense marge d'error. Hi
haurà algun atribut (o conjunt d'atributs) que acomplirà aquesta premisa
d'identificar unívocament. I per a que això siga possible, aquest atribut
haurà de tenir valors distints per a totes les ocurrències (sinó no podria
identificar-les); i al mateix temps no podrà tenir en cap cas el valor nul. En
l'exemple EMPLEAT, el _nom_ o el _DNI_ servirien per identificar. En canvi el
sou no serviria, ja que més d'un empleat pot tenir el mateix sou. El telèfon
tampoc, perquè potser siga nul.

Als atributs (o conjunts d'atributs) que acompleixen la condició anterior els
anomenarem **CLAUS CANDIDATES** , i d'entre totes les claus candidates triarem
una i l'anomenarem **CLAU PRINCIPAL**.

Totes les entitats han de tenir una clau principal. És una de les restriccions
del Model E/R.



Representarem els atributs amb un cercle unit a l'entitat per una línia, i en
l'interior o al costat posarem el nom de l'atribut. La clau principal
l'assenyalarem subratllant-la, o amb el cercle negre.

Per als atributs multivaluats posarem **_n_** en la línia. I els derivats els
representarem amb línies discontínues.

Ací tindríem dues maneres (absolutament equivalents) de representar l'entitat
EMPLEAT amb els seus atributs.  

![](atributs1.png) |   | ![](atributs2.png)  
---|---|---  

### Aplicació a l'exemple



En el nostre exemple del punt 2 quedarien les altres entitats amb els següents
atributs:



![](atributs3.png)

<!--
### 3.2.1 Dominis



És el conjunt de possibles valors que pot agafar un atribut. Així, per
exemple, el domini de l'atribut Dni són els números enters, i encara podríem
filar més prim, els enters de 8 xifres decimals (fins el 99.999.999). Això sí,
si preveem que potser ens convinga guardar també la lletra de NIF, aleshores
hauria de ser alfanumèric de 9 caràcters. El número identificatiu del
departament podria ser un número de l'1 al 10.

Més d'un atribut pot compartir el mateix domini, per exemple si incloem
l'atribut data d'incorporació a la companyia a l'entitat EMPLEAT tindria el
mateix domini que el camp data de naixement.

Quan treballem en el Model Relacional, en el tema següent, una de les
restriccions que farem serà definir clarament el domini de cada atribut, per a
no deixar introduir valors invàlids.

-->  

Llicenciat sota la  [Llicència Creative Commons Reconeixement NoComercial
CompartirIgual 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/)

