(disclaimer: this is not very good)

### Where 2 start
1. [*KOMPLEKSE IKT-SYSTEMER*](#del1)
2. [*OPPSUMMERING AV NETTVERKSPROTOKOLLER OG OSI-MODELLENk*](#del2)
3. [*NETTVEKSTOPOLOGIER*](#del3)
4. [*KOMPLEKSE IKT-SYSTEMER (igjen??)*](#del4)
5. [*IKT-SYSTEM OG KRITISK INFRASTRUKTUR*](#del5)
6. [*TAKSONOMI*](#del6)
7. [*TRUSLER*](#del7)
8. [*TRUSLER OG TRENDER (GF)*](#del8)
9. [*MARITIM DIGITAL KOMMUNIKASJON*](#del9)
10. [*MOTTILTAK - SIKKERHET*](#del10)
11. [*MOTTILTAK - PÅLITELIGHET*](#del11)
12. [*RISIKOHÅNDTERING*](#del12)
13. [*GRAFTEORI*](#del13)



<a name="del1"></a>
# Komplekse IKT systemer

**IKT systemer:**

- Et IKT system består av informasjon, tjenester, nettverk, software, hardware og databaser. Mange ulike komponenter.

**Informasjon:**

- Informasjon er en viktig del av et IKT system.
- Data refererer vanligvis til rådata, eller ubehandlede data. Når dataen er analysert, regnes det som informasjon. Informasjon er “kunnskap formidlet eller mottatt angående et bestemt forhold”, aka ✨Informasjon er data satt sammen✨.

*Vital information, personal information, strategic information, high-cost information.*

> *Hvilken informasjon er viktig for deg?* 

**Tenester:** 

I dag bruker alle organisasjoner digitale tenester. Dette er en viktig del av et digitalt system. Tjenester benytter, produserer, leverer, etc… 🔥`INFORMASJON`🔥 Eksempler på tjenester; Sosiale medier, skylagring, dokumentredigering, videokonferanser, betalingstjenester, strømmetjenester, søkemotorer.

*Tjenester har ulike “formål”: Nødvendig pga juridiske krav, nødvendig for å beskytte målet og gjennomførelsen til organisasjonen. Tjenester som inneholder hemmelig info.* 

> *Hvilke tjenester er viktige for deg?* 

Menneskelige presentasjoner, tekniske systemer og organisatoriske forhold er alle relevante aspekter av et sikkert og robust IKT system.

> *But whyyyyyy?????*

Storytime: 

To personer snakker sammen via Skype (f.eks.). **Informasjonen** som transmitteres her kan være taletrafikk, filer, video, chattemeldinger, etc… Informasjonen sendes gjennom et datanettverk i form av *data* (bits og bytes). Skype er en digital **tjeneste** som tilbyr transimisjon av slik informasjon.  I bunn er det et **IKT system** som muliggjør dette.

Flere kombinasjoner:

- H2H
- H2M
- M2M

> **Hvilke kommunikasjonstjenester bruker du? Hvordan vil du klassifiserer/beskrive de ulike komboene?**


<a name="del2"></a>
# Oppsummering av nettverksprotokoller og OSI modellen

**Packets og routing**

Når du sender en melding blir den sendt via en forbindelse som er konstruert av faktiske fysiske komponenter (rutere, servere, fiberkabler, etc.) som er koblet sammen i et nettverk. Det er viktig å skjønne forskjellen mellom logiske og fysiske komponenter. Fysiske forbindelser (nettverk) gjør det mulig å opprette logiske forbindelser. 

Når du sender eller mottar informasjon på internett, sendes det “pakker” mellom mange maskiner (rutere). Før informasjonen sendes, deles den opp i pakker. Hver pakke er merket med avsender og mottakeradresse (IP adresse). Hver gang en pakke kommer til en ruter, ser ruteren hvilken adresse pakken skal sendes til. Deretter slår den opp i en routing tabell, og  finner beste vei frem til mottakeren. Ruteren vet ingenting om hvor din pakke ender opp, det eneste den vet er hva som er beste vei. 

De forskjellige pakkene trenger ikke å ta samme vei for å komme frem til målet. Det er ikke sikkert at pakkene kommer frem i samme rekkefølge som de ble sendt. Dersom en ruter “går ned”, kan man alltids sende pakkene en annen vei. Dette gjør at Internett er en svært robust kommunikasjonsinfrastruktur.

> **********************Hva er forskjellen mellom denne typen nettverk og et klassisk telefoni-nettverk fra “gamle dager”?********************** 

************************Protokoller************************

- En protokoll er et sett med regler som forteller hvordan man skal utveksle informasjon over ett nettverk.
- Nødvendig for å få forskjellige typer av utstyr å “snakke samme språk”.
- Eksempler på protokoller: TCP, IP, HTTP, TLS, ARP, BGD, DNS, DHCP, FTP, UDP, OSPF, SSH, SSL, SMTP, Telnet. Alle disse protokollene har sine egne styrker og svakheter. For å skjønne hvordan “ditt” digitale system er sårbart, må du vite hvordan det er konstruert. Altså, hvilke protokoller som er implementert.

******************************The layers of communication******************************

- OSI stacken er en konseptuell modell for digital kommunikasjon.
- Modellen beskriver hvordan forskjellige protokoller settes sammen for å transportere informasjon.
- Alle lagene tilbyr tjenester til det neste, (og mottar fra forrige).

************************************The layers of computing************************************

- Hardware omfatter fysiske komponenter
    - harddisk
    - I/O
    - printer
- Software omfatter programmer som “kjører på” hardwaren
    - Apper
    - Programmer
    - OS
    - Databaser
- Firmware er programvaren i minnet til maskinvaren


<a name="del3"></a>
# Nettverkstopologier

**********************************************************Peers connected to a network:**********************************************************

Et kommunikasjonsnettverk er vel ikke så komplisert? Når vi ser på hvordan det brukes,
og det som er synlig for oss, det ser superenkelt ut. Men, er det virkelig så enkelt....?

Vel, du vet allerede at det ikke er tilfelle.
Det er ikke bare to parter ("peers", dvs. maskiner og/eller mennesker) som snakker,
og det er ikke alltid de samme partene. Det kan godt være mange, veldig mange i en samtale, og partene skifter dynamisk selv om det er noen forbindelser som er mer i bruk enn andre.
Partene kan være tett eller langt fra hverandre (som strekker seg fra rett ved siden av hverandre på den andre siden av jorden).

Telekommunikasjon = tele: fjern, til eller på avstand.

Kommunikasjon: måter å utveksle informasjon mellom individ (her: peer) [av
teknologi]
Kommunikasjonsforbindelser mellom de ulike partene danner et mesh (mesh / grid).

Alle mulige forbindelser mellom parter danner en full mesh, men i et ekte nettverk der
vil alltid være mange koblinger som aldri vil bli brukt, slik at det blir en delvis maske.

Stikkord; noder(peers) , Bacon-tall, sentralitet, grafer,

`insert masse boring ass grafteori here`



<a name="del4"></a>
# Komplekse IKT-system
Som dere alle vet, er ikke telekommunikasjon (utveksling av informasjon over avstand).
mulig uten mye teknisk, fysisk utstyr. Dette er utstyr med maskinvare og programvare, med komplisert logikk, og med (strenge) kapasitetsbegrensninger, funksjonelle/funksjonsbegrensninger og feil. Det grunnleggende inkluderer teknisk utstyr, som sluttbrukerutstyr/terminaler, slik at informasjon kan kodes/dekodes til/fra datarepresentasjon, som må ha et format at det kan overføres elektronisk (elektrisk eller optisk) mellom slike
teknisk utstyr over lange avstander (utenfor synsvidde). 

**Kort sagt: telekommunikasjon gir midler for mennesker å snakke med mennesker og maskiner, og maskiner å snakke med maskiner også når de er langt fra hverandre.**

Det er viktig å skille mellom den logiske og fysiske topologien (topologi spesifiserer struktur, og typisk representert som en graf). Forholdet mellom den logiske og fysiske topologien er viktig for
forstå hvor robuste og sikre tilkoblinger er. 

Tilkoblingen og frakoblingen, er en kompleks operasjon, som involverer mye logikk og mye utstyr,
som skal kunne utføre alle nødvendige operasjoner, ha tilstrekkelig kapasitet, være trygge
og sikker, og må være tilgjengelig ved behov. 

**Kort sagt, det må være til å stole på.**

Du bør også merke deg at hvert av endepunktene ("terminaler) er koblet til et nettverkselement,
for eksempel et tilgangspunkt, basestasjon eller tilgangsruter. Disse nettverkselementene er lett synlige, og du har sikkert sett dem. Mellom terminalen og tilgangspunktet er det en tilgang
link. Denne koblingen kan være trådløs eller kablet, og delt mellom forskjellig utstyr og brukere eller dedikert til et spesifikt sett med utstyr, type bruker eller tjeneste. Tilgangslenker og tilgangspunkter er dermed en kritisk del av forbindelsen mellom sluttbrukerterminalene, med tanke på støy, mangel på kapasitet, ustabilitet og sikkerhet.

Husk at en forbindelse mellom endeterminaler (enhver kombinasjon av terminaler, servere) er virtuelle, eller logisk. Mellom endeterminalene har vi transportøkter (TCP / UDP) som har null
kunnskap om ruting og fysisk realisering i nettverket (inne i "nettverkskyen").
Dette kan betraktes som en virtuell forbindelse mellom endeterminalene. Dette betyr at
partene er koblet sammen uten å vite hvordan, og ofte vet ikke engang hvor de andre partene av
forbindelsen(e) er lokalisert.

Mellom AP-ene kan (semi-)permanente VPN-forbindelser (Virtual Private Network), f.eks.
ved hjelp av MPLS (Multiprotocol Label Switching), etableres. Dette gjøres typisk for
langsiktige forbindelser (f.eks. mellom bedriftskontorer) som har eksplisitt ytelse
og pålitelighetsgarantier. 

En VPN-forbindelse kan opprettes på mange måter, forutsatt at det finnes alternativer
stier/ruter gjennom nettverket. Kriterier for å velge den beste ruten for en VPN tar hensyn til
ta hensyn til lasten, koblings- og nodekapasiteten og stabiliteten. Også andre VPN-tilkoblinger
som er eller vil bli etablert må tas i betraktning. Hvis du tenker på at belastningen i et nettverk endrer seg raskt, og ressurser (noder / lenker) kan svikte og bli reparert, så forstår du at dette er en svært utfordrende oppgave. Dette er både fordi rammeverket for å velge den beste ruten inneholder mange, og til dels motstridende begrensninger og tilstand, men også at disse endringene noen ganger er raskere enn det er mulig å sette opp eller endre VPN-tilkoblinger.

En VPN-tilkobling er en logisk tilkobling. En VPN-tilkobling er realisert som en bane som
kan betraktes som en fysisk forbindelse siden den tar hensyn til ressursbegrensningene
og muligheten for feil og angrep av nodene og koblingene banen består av. Det er
ikke mulig å vite nøyaktig hvordan overbelastningen, feilene og angrepene på et (sett med)
fysisk nettverkselement (node), vil skje uten å vite hvordan de forskjellige logiske
tilkoblinger (VPN-er) er realisert. Nettverksoperatøren kan kontrollere VPN-ene som den
styrer i eget nettverk. Men, VPN-er og andre rutede økter, som går på tvers
ulike nettverksdomener, kontrollen og oversikten er kanskje umulig. Dette er kritisk
faktor for å kunne tilby et robust og sikkert nettverk, med tilhørende (kritisk)
virksomhet som er avhengig av disse nettverkene!

**********************A model of ICT systems**********************

> Hvorfor er disse systemene så komplekse? 

<div align='center'><img src="/img/model.png" width=700px></div>

**Fysisk infrastruktur** inkluderer alt utstyr som er nødvendig for å realisere nettverk, og til
sørge for lagring og behandling av tjenestene som leveres.

IKT-systemene er i stadig endring, og nye **tjenester** krever ofte mer utstyr,
som må være tilgjengelig og tilgjengelig på nettet.

En annen trend er at store mengder **offentlig informasjon** samles inn og er tilgjengelig
fra nettet, som kart, GIS, værdata. Informasjonen brukes som innhold i
tjenester bygget på toppen.

************************************************Networks are not static************************************************

For å komplisere jobben ytterligere, må vi huske at nettverk ikke er statiske, og at tilstanden til nettverksressursene (belastningsnivå, arbeider/ned) har en tendens til å endre seg (raskt) over tid. Dette har ført til innføring av delvis autonom drift av nettverk. Dette betyr at nettet drives uten manuelle inngrep og tilpasser seg til endringer basert kun i henhold til veldefinerte regler. Risikoen for feil implementering eller konfigurasjon (de nevnte reglene) er betydelig og med
potensielt alvorlige konsekvenser. Nettverket må også beskyttes mot tilfeldige feil og forsettlige angrep.
Eksempler

1. Koblinger mislykkes: når en kobling mislykkes, må feilen oppdages, riktig avgjørelse må bli tatt og deretter gjennomføres. 
2. Flere noder mislykkes: generelt øker konsekvensene jo mer nettverk
elementer som er berørt, flere feil på grunn av en felles årsak eller angrep, eller
sammenfallende feil vil ha store konsekvenser
3. Angrepsnoder: hvis en angriper med ondsinnede hensikter har både tilgang til
ressurser, og kunnskap om strukturen, et koordinert angrep med enorme
konsekvens kan utføres

**************************The broad perspective**************************

IKT systemene må beskyttes mot et vidt spekter av forskjellige trusler;

<div align='center'><img src="/img/trusler.png" width=700px></div>

******A network of networks******

koordinere byggingen, designet, styringen til nettverket ende til ende, det er ikke bare en nettverksoperatør, men mange og alle har ulike policyer. De forskjellige levrandørene må samarbeide for å kunne tilby den beste tjenesten, samtidig som de konkurrerer om de samme kundene (********************A digital ecosystem********************). Før stolte alle på hverandre, men slik lengre og derfor trenger vi å være mer obs på sikkerhet. I digitale økosystem kan tjenester bli levert som et samarbeid mellom flere parter med ulike roller. Her er det ekstra viktig at de følger opp på sikkerheten. SLA blir brukt for å koordinere de ulike sidene ved slike samarbeid. 

Outsourcing: Noen skaffer en tjeneste fra en ekstern leverandør i stedet for å implementere denne selv. En tjeneste leveres alltid av enn provider, og brukes av en user. SLA er en avtale mellom provider og user.

<a name="del5"></a>
# IKT-system og kritisk infrastruktur
*****✨Kritisk infrastruktur er de anlegg og systemer som helt nødvendige for å opprettholde samfunnets kritiske funksjoner som igjen dekker samfunnets grunnleggende behov og befolkningens trygghetsfølelse✨ -***** Direktoratet for samfunnssikkerhet og beredskap

Andre samfunnsfunksjoner kan være så avhengige av disse funksjonene, at svikt her vil forplante seg til andre deler av samfunnet, dette vil igjen gå på bekostning av befolkningen. EKS: svikt i forsyningen av elektrisk energi kan føre til bortfall av vann og avløp, finansielle tjenester, kommunikssjon, etc…

<div align='center'><img src="/img/kritisk.png" width=700px></div>

**********************************Elektronisk kommunikasjon (”Ekom”)**********************************

defineres som “kommunikasjon ved bruk av system for signaltransport som muliggjør overføring av lyd, tekst, bilder eller andre data vha elektromagnetiske signaler i fritt rom eller kabel der radioutstyr, svitsjer, annet koblings- og dirigeringsutstyr, tilhørende utstyr eller funksjoner inngår. 

Det eksisterer flere uavhengige ekomnett, som så og si er integrert med hverandre. 

I ekominfrastrukturen inngår; 
- kjernenett: løser trafikkbehoved mellom større byer og regioner 
- regionalnett: løser trafikkbehovet innad i større byer og regioner
- aksessnett: knytter utstyret hos brukeren til regionalnettet
- tjenestenett: en kombinasjon av kjernenett og regionalnett:
- drifts- og støttesystemer: IKT-systemer som overvåker og styrer ekomnett og tjenestenett

<div align='center'><img src="/img/ekom.png" width=700px></div>


<a name="del6"></a>
# Taksonomi

Når hele nettverket fungerer, hva mer trenger vi?

Det kan være lurt å tenke på:

- sikkerhet ⭐️
- personvern ⭐️
- funksjonalitet
- pålitelighet ⭐️
- vedlikehold
- brukervennlighet
- trygghet ⭐️
- ytelse ⭐️
- overlevelsesevne
- motstandsdyktighet
- etc

> **⭐️ - de fem kjennetegnene på et sikkert og robust system**

**********************************What is security?********************************** 

Betyr datasikkerhet, informasjonssikkerhet, IKT sykkerhet, cybersikkerhet, nettverkssikkerhet, computersikkerhet og IT-sikkerhet det samme? Nei

Vi har noen fundamentale sikkerhetsattributter; 

- Confidentiality: bare autoriserte personer/systemer kan se sensitiv eller gradert `informasjon`
- Integrity: forsikrer oss om at `informasjon (og tjenester)` ikke har blitt tuklet med
- Availability: nettverket skal være lett tilgjengelig for brukerne
- (Authenticity: handler om å få bekreftet at kilden er den du er ute etter)
- (Non-repudation: man kan ikke angre for det man har sendt)
- (Accountability: skal kunne spore alt tilbake til kilden)

EKSEMPEL: Skype-samtale

- Confidentiality: det skal ikke være mulig for utenforstående å lytte på samtalen
- Integrity: meldinger som blir sendt skal ikke tukles med
- Availability/Authenticity: søkefunksjonen kan kun brukes av registerte brukere
- Authenticity: brukere kan kun bli kontaktet av folk i kontaktlisten dems
- Non-repudation: brukere kan ikke slette meldinger de har sendt

*******Need to know vs need to share*******

Sikkerhet er en kompleks oppgave. Kravene er ofte rett frem, men måten å implementere de er vanskelige. 

************Personvern************

Hva er personvern? I denne sammenhengen innebærer personvern at individer/grupper selv har retten til å bestemme når, hvordan og i hvor stor grad informasjon som omhandler dem, blir kommunisert til andre. Det handler altså om å kunne kontrollere hva som blir gjort med dine personopplysninger. (***************************informasjon som kan brukes for å identifisere en person i en gruppe med mennesker).*************************** 

Vi har tre aktører innenfor dette:

- den registrerte
- behandlingsansvarlig
- databehandler

**************************Sikkerhet er ofte avhengig av en hemmelighet**************************

************************Sikkerhet vs brukervennlighet************************

Brukervennlighet er viktig, ellers vil brukerene finne snarveier for å unngå de tekniske problemene de opplever i forbindelse med sikkerheten. “PGP”

************************Sikkerhet vs personvern************************

Personvern handler om å beskytte informasjon om enkeltindivider. Sikkerhet handler om å beskytte all data, informasjon og generelt alle viktige komponenter i et IKT system.

************************Pålitelighet/Driftssikkerhet************************

Påliteligheten til et system er viktig slik at man med rette kan stole på tjenesten det leverer. 

Pålitelighet har tre hovedegenskaper: tilgjengelighet, pålitelighet(norsk har dårlig ordforråd) og vedlikeholdsvennlighet.

- Tilgjengelighet (availability) er evnen til å tilby tjenester på et gitt tidspunkt eller innenfor et gitt tidsintervall.
    - asymptotisk tilgjengelighet: sannsynligheten for at et system fungerer på et tilfeldig gitt tidspunkt
    - instantaneous tilgj.: sannsynligheten for at et system jobber på et gitt tidspunkt
    - interval tilgj.: gjennomsnittstilgjengeligheten over et gitt tidsintervall
- Pålitelighet (reliability) er evnen til å tilby uforstyrrede tjenester.
    - tiden til første gong et system svikter eller tiden til feil generelt
- Vedlikeholdsvennlighet (mailtainability) er evnen et system har til å bli gjenopprettet til en tilstand der det kan levere den nødvendige tjenesten.
    - modeller blir brukt for å beskrive den nødvendige tiden for å returnere et ureparerlig system til service

<div align='center'><img src="/img/dependability.png" width=700px></div>

**************Sikkerhet**************

- et systems manglende evne til å ha en uønsket effekt på sitt mijlø
- å unngå katastrofale feil

Sikkerhet vs pålitelighet: et pålitelig system vil neppe slutte å fungere, mens et trygt system sannsynligvis ikkje forårsaker katastrofale feil

Safety vs security:

- safety: beskyttelse mot utilsiktede hendelser
- security: beskyttelse mot bevisste hendelser
- safety + security = safe

> ******************Is it safe to fly?******************

************Ytelse************

Kan defineres som et systems evne til å tilby de ressursene som trengs for å levere dens tjenester. Ytelsen avhenger av mengden ressurser i systemet og deres utnyttelse.

- kapasitet: def. som den maksimale lasten et gitt system klarer å håndtere pr tidsenhet
- gjennomstrømning: den delen av kapasiteten som blir brukt av brukerene
- forsinkelse: tiden det tar å få fullføre en tjeneste
- andre ting som: pakketap, tilstopping, servicetid, etc…

Pålitelighet vs ytelse

Høy tilgjengelighet/pålitelighet er ikke mye verdt hvis ytelsen er treg. Et system der feil aldri oppstår, men uten tilstrekkelige ressurser til å oppfylle ytelseskravene, anses ikke å være i fungerende tilstand.

******Qos (Quality of Service)******

<div align='center'><img src="/img/QoS.png" width=700px></div>
Def som “et sett med kvalitetskrav på den kollektive oppførselen til ett eller flere objekter”. 

Dig.kom.; QoS beskriver ytelsen til pakkesvitsjede nettverk. 

Internett og datastrømmning: QoS beskriver ytelsen til applikajsoner

************************************Funksjonelle vs ikke-funksjonelle krav************************************

Funksjonelle krav spesifiserer noe et system må gjøre, ikke-funksjonelle spesifiserer hvordan det burde oppføre seg

<a name="del7"></a>
# Trusler

For å lage et sikker og robust IKT system må vi ta hensyn til et vidt spekter av trusler som kan påvirke systemet og dets leveranse. Når man skal analysere et system, burde man ta for seg alle mulige trusler. Dette gjelder både tilfeldige feil og bevisste angrep.

<div align='center'><img src="/img/trusler.png" width=700px></div>

Innenfor pålitelighet snakker man ofte om faults, errors og failures.

- En “fault” er en defekt i et system;
    
    *programvarefeil, tilfeldige maskinvarefeil, minnebiter som sitter fast, utelatelsesfeil i    meldinger under dataoverføring*
    
- En “error” er et avvik fra den nødvendige driften av systemet. En “fault” kan føre til en “error”, som da vil gjøre “fault”en tydelig. En “fault” kan ligge i dvale/være passiv lenge før den viser seg som en “feil”. Når ein “fault” lager en “error” sies den å være aktiv.;
    
    *en software bug “fault” vil ikke være synlig for subrutinen der feilen hører hjemme blir kalt.* 
    
- En “failure” oppstår når systemet ikke klarer å utføre den nødvendige funksjonen, dvs levere dens tjenester.

Tilfeldige feil er vanligvis forbundet med maskinvarekomponenter. Siden alle fysiske komponenter er utsatt for feil, vil enhver IKT-infrastruktur være gjenstand for tilfeldige feil.
Deteksjon av feil gjøres vanligvis ved å kontrollere programvare.
Systemer kan ofte konstrueres for å tolerere eller til og med rette feil.

<div align='center'><img src="/img/ex1.png" width=700px></div>
<div align='center'><img src="/img/ex2.png" width=700px></div>

**Prosessen med en trussel-sårbarhet-hendelse**

Fra et sikkerhetsperspektiv er det vanlig å snakke om trusler, sårbarheter og hendelser.
I motsetning til feil x 3-patologien er det denne gangen et menneske involvert, som er årsaken til trusselen. Trusselen skjer derfor ikke «bare»; det ligger i mange tilfeller en klar intensjon bak.

*et virus (trussel) kan infisere en uopprettet datamaskin (sårbarhet), som da vil være ubrukelig for eieren (hendelsen).*

******Tilfeldige feil - “Systemsvikt”******

- Komponenter bryter sammen, ofte som følge av overbelastning
    - Kortslutning i elektronik
    - Elektronikk tar fyr
    - Harddisker slutter å fungere
    - Logiske feil i programkode
    - Produksjonsfeil i hardware
- Kan åpne opp for andre typer trusler

********************************************Utilsiktede feil - “Menneskelige feil”********************************************

- Mennesker gjør feil, selv med de beste intensjoner
    - Dokument sendt til feil mottaker
    - Uheldig sletting av filer
    - Inntasting av feil data i et system
    - Feilkonfig. av tjenester og systemer
        - Systemoppgraderinger feiler
    - Mister minnepinner
    - Søler kaffe på serveren
    - Fiberkabler blir gravd over

********************************Bevisste angrep********************************

- Skadevare
- Man-in-the-middle: angrep hvor angriperen skjult releer og potensielt endrer kommunikasjonen mellom to parter som tror de kommuniserer direkte
- Tjuvlytting
- Root kits
- Injection attacks
- Buffer overflow: angrep som utnytter sårbar programvare som tillater skriving utenfor allokert minne på datamaskinen (”Smashing the stach for fun and profit”)
- Passordangrep
- DoS
- Social engineering (Phishing): bruker menneske for å få informasjon om en organisasjon ellers dens systemer
- Tyveri
- Spionasje
- Utpressing
- Sabotasje, vandalisme, terrorisme

************Sårbarheter************

Svakheter i et system som tillater trusler å forårsake hendelser

<div align='center'><img src="/img/vulnerabilities1.png" width=700px></div>¨
<div align='center'><img src="/img/vulnerabilities2.png" width=700px></div>

********************************Svakheter i den norske IKT infrastrukturen********************************

- Mange aktører
- Mer sentralitet
- Ikke dimensjonert for “peaks” i trafikken
- Mangel på redundans

<div align='center'><img src="/img/WHYYY.png" width=700px></div>



<a name="del8"></a>
# Trusler og trender

**Sårbarheter**

"Vulnerabilities are flaws in a computer system that weaken the overall security of the device/system. Vulnerabilities can be weaknesses in either the hardware itself, or the software that runs on the hardware. Vulnerabilities can be exploited by a threat actor, such as an attacker, to cross privilege boundaries (i.e. perform unauthorized actions) within a computer system. To exploit a vulnerability, an attacker must have at least one applicable tool or technique that can connect to a system weakness. In this frame, vulnerabilities are also known as the attack surface." -_✨Wikipedia✨_

****************************Alvorlighetsgrad*****************************

Forskjell på teknisk alvorlighetsgrad og risiko
- Teknisk alvorlighetsgrad:
    - Hva oppnår man med sårbarheten
    - Hva skal til for å utnytte sårbarheten
    - Standardiserte verdier for alvorlighetsgradd
        - CVSS
              - Åpen standard, brukt av mange
              - 0 - 10
- Risiko:
    - Avhenger av verdien til systemet of sannsynligheten for utnyttelse
      
<div align='center'><img src="/img/CVSS.png" width=700px></div>


Når en sårbarhet er kjent er den lett å finne, derfor er det viktig å oppdatere. En ukjent sårbarhet er sårbarheter i systemet man enda ikke vet om, men dette betyr ikke at de ikke er funnet. Disse er svært vanskelig å beskytte seg mot.


**Typer angrep**

Målrettet: 
- Vanskelig
    - Dersom man har et oppdatert og robust system er det vanskelig å hacke seg inn fra internettet.
- Feilkonfigureringer eller svakheter
    - Avhengig av feilkonfig. eller svakheter i løsninger som er eksponert mot internet
    - Angrep mot påloggingssystemer er blandt det mest effektive

- Zero-day*:
    - Svært effektivt å bruke, men veldig vanskelig å få tak i
        - Effektiv -> Overraskelsesmoment, potensielt store skader og potensielt store skader
        - Vanskelig å Oppdage og Få Tak I -> Kompleksitet i oppdagelse, skjeldne og verdifulle, etiske og juridiske begrensninger, og kort levetid etter offentliggjøring

  > **Zero-day**: Når en ukjent sårbarhet endelig blir oppdaget og utnyttet av en angriper, kalles det en "zero-day" sårbarhet. Dette betyr at det ikke finnes noen kjent løsning eller sikkerhetsoppdatering for å rette opp problemet, og det kan føre til alvorlige sikkerhetsbrudd.


Opportunistisk:
- Enkle mål som er sårbare
    - Enkle angrep mot systemer som allerede har sårbarheter

- Skannere
    - Det finnes mange automatiske skannere som kontinuerlig skanner systemer på internett etter svakheter

- Enkle angrep etter kompromittering
    - Ofte enkle og automatiske angrep etter kompromittering, eks:
        - Kryptering av innhold
        - "Hacked by" defacement
        - Endring av reklame
        - Referanser til andre sider for å øke Google score
        - Bitcoing mining
     

**Trusselaktører**
- Innsidere -> Fordel
- Thrill seekers -> Omdømme/nysgjerrighet
- Hacktivists -> Ideologi
- Cyberkriminelle -> Vinning
- Nation State -> Politisk

<a name="del9"></a>
# Maritim digital kommunikasjon
Shipping blir mer og mer digitalisert
- Mer integrasjon om bord
- Mer datautveksling
- Mer trafikkstyring fra land
- Mot ubemannede skip

....og mer følsomt for angrep
- pirater
- smuggling
- svindel
- hackere
- spionasje

**Hvordan ser skipets IT-system ut?**
<div align='center'><img src="/img/shipIT.png" width=700px></div>

**Angrep på OT-sys** har potensielt store konsekvenser, f.eks. kollisjon eller grunnstøting. Vanligvis meget komplisert.

**Angrep på viktige IT-systemer** kan hovedsaklig ha store konsekvenser for økonomi eller rykte. Det kan være både tilfeldige og planlagte angrep.  

**Angrep på kommunikasjon** kan ramme OT- og IT-systemer. Da har man en større angrepsflate. Dette er antagelig "enklere" enn direkte OT-angrep.

> Operasjonell teknologi (OT) refererer til maskinvare og programvare som brukes til å kontrollere og overvåke fysiske enheter, prosesser og hendelser i industrielle miljøer. OT er en sentral del av mange industrier, spesielt de som involverer produksjon, energiproduksjon, transport og andre former for kritisk infrastruktur.

**Litt terminologi**

- VHF: Very High Frequency – Radio-kanaler på 25 kHz hver som brukes til talekommunikasjon eller AIS. Kanalene er i området 156 til 162 MHz.
- AIS: Automatic Identification System – Automatisk sending av navigasjonsinformasjon fra alle større skip (posisjon, kurs, fart ...).
- ASM: Application Specific Messages – Mulighet til å sende generelle datameldinger i AIS-kanalene og to nye kanaler i VDES.
- VDES: VHF Data Exchange System – Nytt system av kanaler for digital VHF.
- VDE: VHF Data Exchange – Nye 100 kHz VHF kanaler (hver er fire gamle) for digitale meldinger.

**Skip kommuniserer med mange parter**
<div align='center'><img src="/img/shipKom.png" width=700px></div>



<a name="del10"></a>
# Mottiltak - sikkerhet

Sikkerhetskontroller er mottiltak som kan brukes for å unngå, oppdage, redusere eller minimere risikoen for eiendeler. Kontrollene vil redusere risikoen for skade eller tap ved å stoppe, avskrekke eller bremse et angrep på en ressurs.

Sikkerhetskontroller kan klassifiseres etter når de brukes:
- Forebyggende kontroller er ment å forhindre at en hendelse inntreffer
- Detektivkontroller er ment å identifisere og klassifisere en hendelse når den forekommer
- Korrigerende kontroller er ment å begrense skaden forårsaket av en hendelse.

Sikkerhetskontroller kan også klassifiseres etter deres natur:
- Administrative kontroller: hendelsesprosedyrer, sikkerhetsbevissthetsgjøringstrening, "fireøye-prinsippet", etc.
- Tekniske kontroller: antivirusprogramvare, brannmurer, autentisering mekanismer osv.
- Fysiske kontroller: låste dører, gjerder og overvåkingskameraer.
  
Sikkerhetskontroller kan tildeles en eller flere av de forskjellige kategoriene i begge klassifikasjoner. For eksempel er en fingeravtrykkskanner både en teknisk og fysisk kontroll siden den består av en maskinvareenhet (fysisk) som kjører autentiseringsprogramvare (teknisk). Det er en forebyggende kontroll siden den vil blokkere uautoriserte brukere fra systemet den beskytter. Sikkerhetsbevissthet er en forebyggende kontroll (kan også være detektiv, dersom de ansatte lærer å oppdage og rapportere sikkerhetshendelser). Sikkerhetsbevissthet er en administrativ kontroll.

Valg og implementering av sikkerhetskontroller for IKT-systemer og organisasjoner er en viktig oppgave. Sikkerhetskontroller er sikkerhetstiltak/mottiltak som er utformet for å: 

(i) beskytte konfidensialiteten, integriteten og tilgjengeligheten til eiendelene som behandles, lagres og/eller overføres av disse systemene/organisasjonene; 

(ii) tilfredsstille et sett med definerte sikkerhetskrav.


**Autentisering**

...er en fundamental byggestein og primær del av forsvaret i et IKT system. Omhandler prosessen å verifisere identiteten til en person/et system.

- Prosessen:
    - Identifikasjon
    - Verfikasjon av et sertifikat
- Ulike måter:
    - Noe du vet
        - passord (mest vanlige, har mange svakheter - cuz pepl r stopid), personlig informasjon
    - Noe du har
        - nøkkel, bank ID, mobiltelefon
    - Noe du "er"
        - fingeravtrykk, iris scan, ansiktsgjenkjenning
    - Noe du "gjør"
        - stemme, håndskrift, tasterytme
    - Hvor du er
        - Lokasjon

**Identifikasjon, autentisering og autorisasjon**

> Hvem er du? Hvordan kan du bevise det? Hva kan du gjøre? --> Tilgangskontroll


**Kryptering**

- Symmetrisk (hemmelig key) kryptering
    - Reversibel
    - Samme nøkkel brukes for kryptering og dekryptering
    - Delt hemmelig nøkkel
- Asymmetrisk (offentlig key) kryptering
    - Forskjellige nøkler for å kryptere og dekryptere
    - Krypterer med mottakerens offentlige nøkkel, dektryptere med privat
    - Tregt, krever mye ressurser
    - Fungerer dårlig
Løsningen er å kombinere begge metodene.

- Nøkler
    - Hold krypteringsnøkkelen hemmelig
    - Beskytt krypteringsnøkkelen fra modifikasjoner og tap
    - Vær klar over viktigheten av lengde (høhø)
        - Målt i bits
        - 2^n mulige kombinasjoner
    - Lag en sterk kryptografisk nøkkel og del den ut sikkert

 
**Digitale signaturer**

- Plaintext + key -> signartur funksjon -> plaintext + signatur
- Prinsipp av PGP (Pretty good privacy)
- Signere mld ved å bruke en symmetrisk melding
    - Dårlig skalering
    - MAC: Message authentication code
        - Mest vanlig: HMAC, hashed message authentication code
- Signere mld ved å bruke asymmterisk melding
    - Ulike keys brukes for å lage og verifisere digitale signaturer
    - Krever mer prosesseringsressurser. Kan optimaliseres vha hashing


**Digitale sertifikat**

- Brukes for å verfisere signaturer, knytte en key til en enhet
- Signatur hierarki
    - Rotsertifiseringsautoritet -> Sertifikatsautoritet 1 & 2 -> Alice (1) og Bob (2)
- Får opp varsel dersom det er et problem med sertifikatet til nettsiden du er inne på


**Sikkerhetskontroller**
Nettverkssikkerhetsprotokoller
- IPsec
    - Hvordan sikre IP-pakker. Gir CIA
    - Nettverkslaget
    - Gir konfidensialitet, integritetsbeskyttelse, dataopphavsautentisering (¿say what? direkte oversatt, not my fault) og replay protection av hver melding ved kryptere og signere alle meldingene.
    - To hovedprotokoller:
        - Autentiseringsheader (AH)
        - Encapsulating Security Payload (ESP)
        - ESP foretrekkes siden den tilbyr både autentfikasjon og konfidensialitet, AH har bare autentifikasjon.
    - To moduser:
        - Transport: Mellom endebrukere. Bare nyttelasten er kryptert
            - Data -> TCP header -> IPsec header -> IP header
        - Tunnel: Mellom inngangsporter. Både nyttelast og header er kryptert.
    - Karakteristikk:
        - Pålegger ikke PKI (Public Key Infrastructure)
        - Applikasjonsuavhengig
        - Gjennomsiktig for applikasjoner når den er integrert i kjernen
        - De fleste VPN-er bruker IPsec
- TLS/SSL
    - Transportlaget, kjører bare på toppen av TCP
    - Basert på SSLv3. Bruker PKI for å kunne tilby brukerautentisering i tillegg til symmetrisk nøkkel for konfidensialitetsproblem
    - To metoder:
        - Gjensidig autentifikasjon:
            - Både client og server autentiserer seg når det etableres en sesjon
            - Veldig dyrt
        - Server-side autentifikasjon:
            - Bare serveren gir et sertifikat når det etableres en sesjon
- SSH - Secure Shell
    - Applikasjonslaget. Connection oriented -> Bruker bare TCP
    - Primært brukt på shell-baserte løsninger
    - Bruker offentlig nøkkel kryptografi for å bevise autensiteten til shell-brukeren
    - Vedlikeholder en rekke klarerte hosts
 

<a name="del11"></a>
# Mottiltak - Pålitelighet
**Tre fundamentale pålitelighetsegenskaper**
- Tilgjengelighet: evnen å tilby en gitt tjeneste på/innen et gitt punkt/tidsintervall
- Pålitelighet: evnen å tilby uforstyrrede tjenster (kontinuitet)
- Vedlikeholdbarhet: evnen til å bli gjenopprettet til en tilstand der det kan levere den nødvendige tjenesten

> Mottiltak i denne forstand blir da hva vi kan gjøre for å holde et system oppe slik at det kan fortsette å levere de tjenestene den tilbyr.


<div align='center'><img src="/img/dependability.png" width=700px></div>

- Unngå feil: forhindre at feil oppstår
- Feiltoleranse: fikse feilen før systemet går ned
- Fjerning av feil: redusere antall og alvorlighetsgraden av feil som kan oppstå
- Feilvarsling: analysere systemet og finne ut hvor det er mest hensiktsmessig med mottiltak

<div align='center'><img src="/img/means.png" width=700px></div>

Målet med både feilunngåelses- og feiltoleransestrategiene er å kunne levere den spesifiserte tjenesten, til tross for forekomst og aktivering av feil i systemet
Feilunngåelse betyr å unngå at feil introduseres. Målet er å ha et feilfritt system. Ingen feil introduseres under utformingen av systemet.
Feiltoleranse betyr at feil kan oppstå og kan føre til feil, men feilene skal ikke resultere i feil som kan observeres av brukeren. Målet er å levere tjenesten til tross for at det oppstår feil i systemet.

> Merk at et feiltolerant system kan fungere på et redusert nivå når deler av systemet har sviktet. Det kan være en reduksjon i gjennomstrømming eller en økning i responstid, men tjenesten er fortsatt funksjonell.

**Hvordan oppnå:**
- Unngåelse av feil:
    - Ingen feil introdusert under design og implementering.
    - Skjerming av systemet under drift.
    - Bruk utprøvde design og komponenter.
    - Kvalitetssikringsprosesser.
- Feiltoleranse:
    - Realisert av redundans i 
        - Maskinvare
        - Programvare
        - Informasjon
        - Tid
- Fjerning av feil:
    - Under utvikling:
        - Verifikasjon
        - Diagnostisering
        - Rettelser
    - Under drift:
        - Korrigerende vedlikehold
        - Forebyggende vedlikehold
      
      Enhver kombinasjon av disse kan brukes for å forbedre et systems feiltoleranse

> Den gyldne regelen (for redundans): _No single point of failure._

**¿Qué es redundans?**

Redundans i en nettverksinfrastruktur kan implementeres som
• Enhets("node")redundans
• Bane("link")redundans
• Protokollredundans: legge til ekstra programvare, informasjon og/eller tid

<div align='center'><img src="/img/redundans.png" width=700px></div>


Redundans er tillegg av ressurser i form av maskinvare, programvare, informasjon eller tid utover det som er nødvendig for normal levering av systemtjenester.

To forskjellige metoder for å implementere redundans:
- Modulær redundans
    - To eller flere moduler som fungerer samtidig - alltid en kopi kjører og holdes oppdatert med all interaksjon med systemet
        - Hardware
        - Boeing 777: 3x3 redundans
- Standby-redundans (også kjent som "backup"-redundans)
    - Én aktiv komponent, én eller flere passive komponenter klare til å overta. Bare ett eksemplar får sanntidsoppdateringer. De andre oppdateres ofte.
        - Routing system
        - Servere
     
Trippel modulær redundans (TMR) betyr at tre delsystemer beregner et resultat, og det resultatet blir behandlet av en flertallsvelger for å produsere en enkelt utgang. Hvis et av de tre undersystemene svikter, kan de to andre undersystemene korrigere og maskere feilen. TMR er en veldig vanlig tilnærming for å gjøre maskinvare overflødig, og den er også ofte implementert i programvare.

> Hvorfor trenger vi tre undersystemer? Hvorfor er det ikke nok med to?


**Ulemper med redundans**
- Dyrt
- Økt kompleksitet -> Flere PoF og økt risiko for menneskelige feil
- Hvor skal man stoppe?
- Er feil egentlig uavhengige?
- Er det virkelig ingen SPoF igjen?

<div align='center'><img src="/img/ekom.png" width=700px></div>

Ekom er et eksempel på nettverk med god redundans, kanskje bortsett fra i aksessnettverket.


**Vær forberedt på feil og å måtte håndtere dem!**


For å minimere den totale systemkostnaden må du vurdere
- utviklingskostnad
- produksjonskostnad
- utstyrskostnad
- driftskostnad
- vedlikeholdskostnader

Noen ganger kan det være et alternativ å ikke forebygge feil, men heller håndtere de så fort de har oppstått.

**Fire faser for å komme seg etter en feil**
- Deteksjon: trenger å finne ut at systemet ikke fungerer (hvordan vil du (eller systemet) bli varslet?)
- Lokalisering: hvor er det?
- Isolasjon: ikke alltid, men noen ganger må du isolere feilen for å forhindre mer skader
- Reparer – gjenopprett: bring systemet til å fungere igjen

Merk at ikke alle disse fasene er aktuelt i alle feilsituasjoner.

Spørsmål å vurdere når du velger strategi for håndtering av feil:
- Hva koster nedetiden?
- Hva er RTO (Recovery Time Objective) og RPO (Recovery Point Objective)?

> Når et system skal utvikles, spesifiseres dets ikke-funksjonelle krav til sikkerhet, personvern, pålitelighet, sikkerhet og ytelse (osv.), sammen med alle funksjonskrav. De ikke-funksjonelle kravene vil avhenge av bruken av systemet. De ikke-funksjonelle kravene ‐> mottiltak som skal iverksettes. Hvilke mottiltak som skal velges og «styrken» av disse tiltakene vil avhenge av konsekvensene av hendelser og feil som kan oppstå.


<a name="del12"></a>
# Risikohåndtering

Risikohåndtering brukes fordi det ikke er mulig å lage helt feilfrie systemer. Da må prioritere hvilke tiltak man skal prioritere (huh?).

**Basic-est of the basics:**
- Risiko: sannsynligheten for en uønsket hendelse og dens konsekvenser for en ressurs
- Uønsket hendelse: en hendelse som skader eller reduserer verdien av en eiendel
- Ressurs: alt av verdi
- Sannsynlighet: Sjansen for at noe skjer
- Konsekvens: virkningen av en uønsket hendelse
- Risikonivå: størrelsen på en risiko som kommer fra dens sannsynlighet og konsekvens

<div align='center'><img src="/img/risiko.png" width=700px></div>


**Risikostyring** er alt en organisasjon gjør for å kontrollere og håndtere risiko
- Iterativ prosess:
    - Etablere risikostyringskontekts
    - Kvantitativt eller kvalitativt vurdere relevant informasjonsrisiko.
    - Behandle, beholde, unngå og/eller dele risikoen på en passende måte
    - Holde interessesenter informert
 
**Risikovurdering** har som formål å forstå og dokumetere risikobildet vedrørende en bestemt del eller apsektv av et system eller en organisasjon. 

**Trinn 1: Kontekstetablering**

- Planlegging av riskovurdering
- Mål og målsettninger
    - Hvorfor og for hvem gjøres denne risikovurderingen?
-Omfang
    - Hvilken del av systemet skal vurderes? _f.eks. protokollag, komponenter, brukere_
    - Hva vil ikke bli vurdert?
    - Hvilke mottiltak er iverksatt
    - Hvilke aktører kan man stole på? _Hva slags brukere er involvert?_
    - Hva er systemets overflate? _Den delen av systemet som er eksponert, og kan angripes_
- Ressurs
    - En ressurs er noe verdifullt som må beskyttes
    - Informasjon, programvare, tjenester, maskinvare
    - Vurdering av ressursen(e) og verdien
        - Forskjellen mellom primære eiendeler og støttemidler
            - Primær: Grunnleggende funksjoner. Kritisk viktig å beskytte
            - Støtte: Andre verdier som må beskyttes for på beholde primære eiendeler beskyttet
- Risikoskalaer
    - Konsekvenser
    - Sannsynligheter
        - Kvantitativ: Probability
        - Kvalitativ: Likelihood
        - Eksempel: Del inn i intervaller på tid. f.eks. sjelden mindre enn én gang per tiår
        - Kan legge til flere dimensjoner til sannsynlighetsskalaene
- Kritierier for risikovurdering: Hva er akseptabel risiko?

**Trinn 2: Risikoidentifikasjon**

- Risikoidentifikasjon gjøres med hensyn til de identifiserte **eiendelene** ved å identifisere **trusler** og forså hvordan trusler kan føre til hvilke **uønskede hendelser** på grunn av hvilke **sårbarheter**
    - Vil resultere i en liste over uønskede hendelser
- Tre metoder:
    - **Dokumentgjennomgang**
        - Software, sonemodeller, sikkerhetspolicy, log files, config.files, etc.
        - For å forstå hvilke sårbarheter som finnes
    - **Testing**
        - Ikke alltid mulig, men veldig nyttig
    - **Intervjuer**
        - Samle en gruppe mennesker fra ulike seksjoner og operasjoner og diskuter hva som kan gå galt


**Trinn 3: Risikoanalyse**

- Risikoanalye har som formål å estimere og bestemme nivået på de identifiserte risikoene
    - Estimer sannsynligheten og konsekvensene for hver uønskede hendelse
- Vurdere sannsynlighet
    - Hvem vil gjøre dette? Hva er deres motivasjon? Hvordan vil de gå frem? Hvilke tilfeldige feil kan skje?
- Sannsynlighet/konsekvens-matrise
    - Viktig å se hvordan de ulike risikoene er i forhold til hverandre
 

**Trinn 4: Risikoevaluering**

- Sammenligning av risikoanalyseresyktater med risikokriterier for å bestemme hvilke risikoer som bør vurderes for behandling


**Trinn 5: Risikobehandling**

- Identifisere og velge midler for risikoredusering
- For risikoer som er uakseptable, må man identifisere og velge mottiltak som reduserer risikoene
- Prøv å redusere sannsynlighet og/eller konsekvens
- Ta i bruk mottiltak (reduser risikoen)


**Fire hovedstrategier for å håndtere risiko**
1. Unngå
    - Eliminere. Siste utvei
2. Reduser
3. Overfør
    - Flytt risikoen til en tredjepart, f.eks. ved outsourcing. Forsikring
5. Godta
    - I noen tilfeller er det ikke verdt det å gjøre mottiltak. Aksepter risikoen.
- Risikostyring er alltid en pågående prosess.
- Risikovurdering er en begrenset prosess som organisasjoner gjennomfører på jevnlig basis
- Utfordringer med risikostyring i komplekse systemer
    - Moderne nettverkssystemer har mang ulike interessesenter
    - Trusselkilder kan ligge hvor som helst i verden
    - En betydelig del av truslene er forsettlige
    - "Insidere" er offte de farligste truslene (og de vanskeligeste å forutsi og beskytte mot)
    - "Dominoeffekten" er vanskelig å forutsi
- Ulike typer usikkerhet
    - Epestemisk usikkerhet: usikkerhet pga uvtenhet eller mange på bevis
    - Aleatorisk usikkerhet: usikkerhet pga iboende tilfeldighet
- Black swans
    - Uønskede hendelser som er svært sjeldene og uventede, men som har svært betydelige konsekvenser
    - Ikke vurdert i risikovurderinger
- Kontrollsystemer



<a name="del13"></a>
# Grafteori
- _Hvorfor grafteori?_
    1. Konverter oppgave til graf
    2. Bruk verktøy fra grafteori til å få resultater
    3. Tolk resultatene fra grafteorien i den originale settingen
    Virkelige systemer av ulik natur kan ha samme representasjon
- Grunnleggenede egenskaper
  - Grafdiameter: "Lengste korteste vei i en graf"
  - Tilkobling: En graf som kobles tili hvis det er en bane mellom et hvilket som helst par av hjørner i grafen
  - Kantgrad: Antall kanter per node
  - Nodegradsfordeling: Fordeling som angir sannsynligheten for at en node har _k_ noder
- Skaleringfrie nettverk
    - Power law fordeling
    - Mange noder med få forbindelser, få noder med mange forbindelser
- Tilfeldige nettverk
    - Barábasi-Albert algoritmen
        - Skaper tilfeldig nettverk med power law fordeling
        - Basert på preferential attachment
            - Start med _m_ tilkoblede noder
            - Legg til ny node of koble til _m_ eksisterende noder
            - Tilkobling til nye noder med sannsynlighet $`p_i = \frac{k_i}{\sum_{j}{k_j}}`$
            - "Depending on a fraaciton og total links connected to node I"
    - Watts-Strogatz
- Sentralitet
    - Ulike sentralitetstiltak
    - **Degree centrality**
        - Nodegrad er sentralitetsindeks
        - "Noden med flest naboer er mest sentral"
        - Negativt:
            - Bruker bare kunnskap om de mest lokale
            - Noder som forbinder subgrafer anerkjennes ikke som viktige
    - **Degree centrality**
        - Tegn de korteste banene for alle nodeparene: Hvor mange av disse går gjennom $`v_i`$
        - $`\sum_{s < t \& (s, t ≠ i)}{\frac{n_{s,t}^{i}}{n_{s,t}}}`$
            - $`n_{s,t}^{i}`$ er antall korteste veier mellom $`v_s`$ og $`v_t`$ som går gjennom $`v_i`$
            - $`n_{s,t}`$ er antall korteste veier mellom $`v_s`$ og $`v_t`$
        - Merk: Et nodepar kan ha flere korteste veier







