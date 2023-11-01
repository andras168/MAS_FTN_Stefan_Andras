<h2> ULAZNI PIN: </h2>


- Primer postavke pina RB9 kao ulazni digitalni pin:
```
GPIO_Digital_Input(&PTB_PDIR, _GPIO_PINMASK_9);
```
- Primer postavke čitavog PORT-a B kao ulazni digitalni port:
```
GPIO_Digital_Input(&PTB_PDIR, _GPIO_PINMASK_ALL);
```
- Drugi način za postavljanje pina RB9 kao ulazni digitalni pin (direktnim upisom bita u registar PDDR):
```
GPIOB_PDDR &= ~(1 << 9);
```

<h2>IZLAZNI PIN: </h2>

- Primer postavke pina RD9 kao izlazni digitalni pin:
``` 
GPIO_Digital_Output(&PTD_PDOR, _GPIO_PINMASK_9);
```  
- Primer postavke čitavog PORT-a D kao izlazni digitalni port:

```
 GPIO_Digital_Output(&PTD_PDOR, _GPIO_PINMASK_ALL);
```
- Drugi način za postavljanje pina RD9 kao izlazni digitalni pin (direktnim upisom bita u registar PDDR ):
```
GPIOD_PDDR |= (1 << 9);
```
- Setovanje izlaznog pina RD9 (postavljanje izlaza na logičku jedinicu):

```
GPIOD_PSOR |= (1 << 9);
```
  
<h2> RAZNE OPERACIJE: </h2>

- Resetovanje izlaznog pina RD9 (postavljanje izlaza na logičku nulu):

```
GPIOD_PCOR |= (1 << 9);
```
- Ivertovanje izlaznog pina RD9 (postavljanje izlaza na logičku jedinicu):
```
GPIOD_PTOR |= (1 << 9);
```
- Ispitivanje stanja ulaznog pina RD9:
```
if(GPIOD_PDIR & (1 << 9)) 
```
*Zadati if() uslov ispituje da li pin 9 porta D nalazi na visokom nivou (nivou logičke jedinice)*
