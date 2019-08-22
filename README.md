# Jupyter notebook test repository

dit is een test repository om te kijken hoe jupyter notebook in combinatie met github bevalt.

Functionele eisen voor een datascience omgeving.
1.  Delen binnen een team hoe een bepaalde berekening was gedaan en wat de uitkomst was.
2.  Idealiter zou de berekening interactief moeten zijn, zodat iemand die toegang heeft tot het notebook ook kan varieren met de inputs/parameters en zien hoe dat de resultaten beinvloedt.
3.  Datasets delen in een team.

## Hoe is dit uitgewerkt als je github i.c.m. jupyter gebruikt.

Eis 1: Github heeft een ingebouwde previewer voor jupyter notebooks. Dus om resultaten van een berekening te bekijken, incl de opbouw van de berekening, is het voldoende om naar github te gaan.  Jupyter notebooks hebben extensie .ipynb. Als je de .ipynb file aanklikt in github zie je hetzelfde als wat je ziet als je hem opent in jupyter notebook. PR's (dus diffs van de notebooks) zijn helaas wel wat slechter leesbaar dan normale PRs dus om een PR te beoordelen moet je locaal jupyter notebook draaien en het notebook openen op je eigen machine.

Eis 2: Helaas levert github geen interactieve omgeving, dus deze eis is niet opgelost met deze opzet. Voor het doen van berekeningen moet je jupyter notebook locaal installeren. Het komt meegeleverd met de anaconda distributie van python dus dit is niet veel werk. Het is mogelijk met aanvullende software (binderhub) om automatisch kubernetis images te maken voor jupyter notebooks, en het notebook dan ook op te starten op Google Cloud, Azure of Amazon. Maar dat lijkt me voor eerst een optie die we nog niet hoeven uit te proberen.

Eis 3: Datasets delen. Github repositories zijn gelimiteerd tot 100MB maar er is een API om grote bestanden aan github toe te voegen, git-lfs. Hiervoor moet je git-lfs installeren op je computer.
Vervolgens 

```
   git lfs init 
```

Als voorbeeld heb ik een test.json bestand toegevoegd aan de data directory. de hele data directory is ingesteld via `git lfs track "data/**"`. Deze setting is bewaard in de .gitattributes file dus die hoeft een nieuw teamlid niet opnieuw te draaien. Wel moet ieder teamlid git-lfs geinstalleerd hebben. Ik vermoed ook dat iedereen `git lfs init` opnieuw moet draaien omdat er git hooks geinstalleerd moeten worden in de repo.


