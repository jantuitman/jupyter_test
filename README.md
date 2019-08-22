# Jupyter notebook test repository

dit is een test repository om te kijken hoe jupyter notebook in combinatie met github bevalt.

Functionele eisen voor een datascience omgeving.
1.  Delen binnen een team hoe een bepaalde berekening was gedaan en wat de uitkomst was.
2.  Idealiter zou de berekening interactief moeten zijn, zodat iemand die toegang heeft tot het notebook ook kan varieren met de inputs/parameters en zien hoe dat de resultaten beinvloedt.
3.  Datasets delen in een team.

## Hoe is dit uitgewerkt als je github i.c.m. jupyter gebruikt.

Eis 1: Github heeft een ingebouwde previewer voor jupyter notebooks. Dus om resultaten van een berekening te bekijken, incl de opbouw van de berekening, is het voldoende om naar github te gaan.  Jupyter notebooks hebben extensie .ipynb. Als je de .ipynb file aanklikt in github zie je hetzelfde als wat je ziet als je hem opent in jupyter notebook. PR's (dus diffs van de notebooks) zijn helaas wel wat slechter leesbaar dan normale PRs dus om een PR te beoordelen moet je locaal jupyter notebook draaien en het notebook openen op je eigen machine.

Eis 2: Helaas levert github geen interactieve omgeving.