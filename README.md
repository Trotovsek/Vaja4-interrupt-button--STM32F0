# Vaja4-interrupt-button--STM32F0

Cube MX

b) Glede na vašo razvojno ploščico in razširitveno vezje s tipkami, izberite ustrezen digitalni vhod kot
interrupt (GPIO_EXT…) in izhod za zeleno LED. Zapišite izbrana pina:
GPIO_EXTI0 -> PA0 ter zelena led PC9 in modra led PC8


kyleV5


c) Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED (pomagajte si z metodo toggle, glej vaja0a).
HAL_GPIO_TogglePin(GPIOC,GPIO_PIN_9).


d) Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala:
for(uint32_t i=0; i&lt;10000; i++);
Koliko znaša (v mili sekundah) zapisana zakasnitev? 500ms.

e) V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED (metoda toggle, glej vaja0a):
HAL_GPIO_TogglePin(GPIOC,GPIO_PIN8); .


f) V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde (glej vaja0a):
HAL_Delay(500).

b) Opazujte delovanje (utripanje modre LED). Kaj se zgodi, ko pritisnemo na modro tipko na STM32F0?
Ko pritisnemo modro tipko se prižge/ugasne zelena in obdrži to stanje. modra ves čas utripa.

c) Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj?
Ne. ker pogram poteka proitisk na tipko pa je samo interput za zeleno led luč. je tudi napisan v drugem user code begin .

Komentar
vaja dela brez napak. navodila so pravilno napisana in z vajo ni težav.
