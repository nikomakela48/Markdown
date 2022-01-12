# GIT tärkeimmät 
[![GIT](/640px-Git-logo.svg.png)](/640px-Git-logo.svg.png)
## Markdown tehtävä tässä samalla sitten

---

GIT on hyödyllinen versionhallintaohjelma, jonka käyttö kannattaa opetella. Kerron tässä tärkeimmät komennot, jotta ehkä opit (tai et).

## Peruskomennot
GITissä on muutama ns. "peruskomento"
- Jokaisen komennon eteen laitetaan "git". Tällä määritellään, mille ohjelmalle lähetetään käskyjä.
- init, add, commit, status, push ja branch

Näillä komennoilla tehdään ne tavallisimmat asiat GITtiä käytetettäessä.

>*git init*

- init-komennolla määritellään GITille työhakemisto, jota sen tulisi seurata.

>*git add*

- add-komennolla lisätään joku tiedosto versiohallinnan (GIT) seurantaan. 

>*git commit*

- commit-komennolla saadaan "kuitattua" tiedostoihin tulleet muutokset, jotta muutokset voidaan julkaista esim. GitHubiin tarvittaessa

>*git status*

- status-komennolla voidaan kysyä GITiltä, että kuinka sujuu. Vastaukseksi tulee, että onko johonkin tiedostoon tullut muokkauksia, onko työhakemistossa uusia tiedostoja yms.

>*git push*

- push-komennolla voidaan työntää työhakemistossa olevat tavarat ulkopuoliseen palveluun, esim GitHubiin

>*git branch*

- branch-komennolla voidaan tarkastella, onko projektissa eri haaroja, voidaan myös tehdä uusia haaroja projektiin, jotta voidaan tehdä erilaisia mahdollisesti kokeellisia muutoksia ilman että ne sotkee päähaaran tiedostoja

## Mitäs sitten kun menee perseelleen, ja muutoksia pitäisi perua?

Sitten kun kaikki ei mene niinkuin strömsössä, niin saattaa tulla mieleen, että tiedostosta pitäisi saada tehdyt muutokset pois. Tämä onnistuu *git checkout*, *git revert* ja *git reset*-komennoilla.

>*git checkout*

- tällä komennolla voidaan palauttaa tiedosto edelliseen tilaansa, jos muutoksia ei ole vielä kuitattu *commit* komennolla.
- Esim. *git checkout -- hujanhajan.txt*

>*git revert*

- tällä komennolla voidaan palauttaa tiedostot, mutta se tallentaa myös sen "pilalle menneen" osan, jotta mitään tietoja ei häviäisi
- Esim *git revert -e*-komennolla voidaan vielä jättää viesti, jotta ei jää epäselväksi, mitä on tehty.

>*git reset*

- Tällä komennolla saadaan palautettua kaikkien haarojen muutokset taakse päin

## Työhakemiston liittäminen Ulkopuoliseen palveluun, esim GitHub

Työhakemiston liittäminen GitHubiin on helppoa. Kun GitHub-repositorio luodaan, se antaa suoraan komennon, jonka voi kertoa GITille.

Esim. 
>*git remote add origin https://github.com/......* lisätään ulkoinen lähde
>*git push -u origin master* "työnnetään" master-haaran sisältö ulkoiseen lähteeseen

Ulkoisesta lähteestä saa haettua tietoa paikalliseen työhakemistoon käyttämällä *git fetch*, tai *git pull* -komentoa.

- Näiden kahden ero on se, että *git fetch* ei ylikirjoita paikallisen kansion tiedostoja. *git pull* hakee kaikki muutokset ja erilaisuudet verkkohakemistosta

## Toisen henkilön repositorion forkkaaminen ja kloonaaminen

Forkkaus tapahtuu helpoiten GitHubin kautta toisen henkilön repositoriossa painamalla Fork-nappulaa. Tämä kopioi repositorion omalle käyttäjälle, jolloin voidaan tehdä muokkauksia.

Fork voidaan kloonata itselle koneelle käyttämällä *git clone*-toimintoa.

Esim. 
>*git clone https://github.com/.......* määritellään repositorion linkki

Paikallisessa työhakemistossa olevaan forkkiin voidaan lisätä upstream esim komennolla:
> git push --set-upstream origin <branch>
  
Linkki GITin ohjeisiin:
  https://git-scm.com/book/en/v2


![](https://miro.medium.com/max/719/1*26XR2RfPsSmFd_Q6EA0SrA.png)
