# Machine Learning Modell zur Vorhersage des Überlebens nach einer AIDS-Infektion und dem darauf folgenden Treatment

## Inhaltsverzeichnis
[Subheading 1](## Die üblichen Schritte im Teminal)
[Subheading 2](## Repository Struktur)
[Subheading 3](## Daten herunterladen)
[Subheading 4](## Publikation zu den Daten)
[Subheading 5](## Variablen-Beschreibung)

## Die üblichen Schritte im Teminal
`.\venv\Scripts\activate` aktiviert die virtuelle Umgebung

`git status` prüft Änderungen

`git add .` fügt Änderungen hinzu

`git commit -m "text"` commitet die Änderungen

`git push ` führt *push* aus

## Repository Struktur
Es wurden Ornder für Daten `data`, Code `src`, Modelle `models`, Grafiken `plots` und Tabellen `tables` angelegt. Für die zu verwendenden Pakete wurde File `requirements.txt` erstellt. Eine ausführliche Anleitung zum Handing von requirements-file findet man [hier](https://learnpython.com/blog/python-requirements-file/).

## Daten herunterladen
https://archive.ics.uci.edu/dataset/890/aids+clinical+trials+group+study+175

Die Anweisungen beinhalten einen veralteten Code. Das aktuelle Handing des `ucimlrepo` Pakets kann man [hier](https://github.com/uci-ml-repo/ucimlrepo?tab=readme-ov-file#ucimlrepo-package) nachvollziehen.

Die Daten für die Arbeit wurden noch vor den aktuellen Änderungen am 27.11.2024 herunter geladen. 

## Publikation zu den Daten
https://www.nejm.org/doi/10.1056/NEJM199610103351501?url_ver=Z39.88-2003&rfr_id=ori:rid:crossref.org&rfr_dat=cr_pub%20%200www.ncbi.nlm.nih.gov

## Variablen-Beschreibung

|Variable Name |	Role |	Type |	Demographic	| Description |	Units |	Missing Values |
|--------------|---------|-------|--------------|--------------|----|----------------|
pidnum	| ID	| Integer	||	Patient ID	| |	no |
cid	| Target |	Binary	||	censoring indicator (1 = failure, 0 = censoring)	||	no |
time |	Feature	| Integer	||	time to failure or censoring	||	no |
trt	| Feature |	Integer	||	treatment indicator (0 = ZDV only; 1 = ZDV + ddI, 2 = ZDV + Zal, 3 = ddI only)	||	no |
age	| Feature |	Integer	| Age |	age (yrs) at baseline	||	no |
wtkg |	Feature |	Continuous	||	weight (kg) at baseline	||	no |
hemo |	Feature	| Binary	||	hemophilia (0=no, 1=yes)	||	no |
homo |	Feature	| Binary	| Sexual Orientation |	homosexual activity (0=no, 1=yes)	||	no |
drugs |	Feature	| Binary	||	history of IV drug use (0=no, 1=yes)	||	no |
karnof |	Feature	| Integer ||		Karnofsky score (on a scale of 0-100)	||	no |
oprior |	Feature	| Binary	||	Non-ZDV antiretroviral therapy pre-175 (0=no, 1=yes)	||	no |
z30	| Feature	| Binary	||	ZDV in the 30 days prior to 175 (0=no, 1=yes)	||	no |
zprior |	Feature	| Binary	||	ZDV prior to 175 (0=no, 1=yes)	||	no |
preanti |	Feature	| Integer	||	# days pre-175 anti-retroviral therapy	||	no |
race |	Feature	| Integer |	Race |	race (0=White, 1=non-white)	||	no |
gender |	Feature	| Binary |	Gender |	gender (0=F, 1=M)	||	no |
str2 |	Feature	| Binary	||	antiretroviral history (0=naive, 1=experienced)	||	no |
strat |	Feature	| Integer	||	antiretroviral history stratification (1='Antiretroviral Naive',2='> 1 but <= 52 weeks of prior antiretroviral therapy',3='> 52 weeks)	||	no |
symptom |	Feature	| Binary	||	symptomatic indicator (0=asymp, 1=symp)	||	no |
treat |	Feature	| Binary	||	treatment indicator (0=ZDV only, 1=others)	||	no |
offtrt |	Feature	| Binary	||	indicator of off-trt before 96+/-5 weeks (0=no,1=yes)	||	no |
cd40 |	Feature	| Integer	||	CD4 at baseline	||	no |
cd420 |	Feature	| Integer	||	CD4 at 20+/-5 weeks	||	no |
cd80 |	Feature	| Integer	||	CD8 at baseline	||	no |
cd820 |	Feature	| Integer	||	CD8 at 20+/-5 weeks	||	no |


