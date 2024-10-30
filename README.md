# TuotekuvastoApp-sovellus
<br>
Sovellus sisältää seuraavia moduuleja:<br>

- Product.cs, joka siältää Product-luokan. Luokka määrittelee, mitä tietoja/ominaisuuksia tuotteeseen liittyy.<br>
- products.json, jossa on listattu kaikki katalogin tuotteet Product-olioina json-muodossa.<br>
- site.css, joka sisältää muotoilutyylien tiedot<br>
- Product.cshtml, joka on websovelluksen tuotekataloginäkymä. Näkymän html-koodi näyttää tuotetiedot, jotka perustuvat sen model-ominaisuuteen sijoitettuun näkymän näyttämien (Product-olioiden) luetteloon. Näkymän muotoilu taas perustuu site.css-tiedostossa oleviin tyyliluokkiin product-card (kutakin tuotetta esittelevä laatikko) ja product-grid (edellisten muodostama ruudukko näkymässä).<br>
- HomeController.cs-rajapinta, joka ottaa vastaan asiakassovelluksen (esim. selain) pyyntöjä ja palauttaa niiden pohjalta dataa. Kun käyttäjä valitsee käyttöliitymästä Products-välilehden, rajapinta suorittaa ensin GetProducts()-metodin, joka lukee products.json-tiedostosta tuotteet ja muuttaa ne Product-olioiden listaksi. Tämän jälkeen se palauttaa näkymän (Product.cshtml), jolle se on antanut tuoteoliolistan.
