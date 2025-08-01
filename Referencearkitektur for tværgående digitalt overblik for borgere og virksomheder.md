# Referencearkitektur for tværgående digitalt overblik for borgere og virksomheder

## Om denne versions status og anvendelse

_Referencearkitektur for tværgående digitalt overblik version 1.0_ er godkendt af Styregruppen for digital kommunikation. Referencearkitekturen er desuden optaget som del af den fællesoffentlige digitale arkitektur af Udvalget for arkitektur og standarder.

Det er ligeledes aftalt, at referencearkitekturen skal anvendes i de fællesoffentlige projekter under programmet _Mit Overblik_, herunder særligt projektet vedrørende _etablering af fællesoffentligt orkestreringskomponent og udarbejdelse af fælles standarder for data og services til overblik_, som er forankret i Digitaliseringsstyrelsen samt i projektet vedrørende _etablering af virksomhedsoverblik_, som er forankret i Erhvervsstyrelsen. Målgruppen for dette dokument er således arkitekter og andre relevante interessenter, der indgår i disse projekter.

Referencearkitekturen kan frit anvendes af myndigheder, leverandører og andre interesserede. Såfremt man har spørgsmål til anvendelsen af referencearkitekturen, opfordres lokale myndigheders projekter til at gå i dialog herom med Digitaliseringsstyrelsen: [arkitektur@digst.dk](mailto:arkitektur@digst.dk)

Det er forventningen, at erfaringer med anvendelse af referencearkitekturen vil give anledning til nye erkendelser og indsigt, der kan give anledning til at opdatere referencearkitekturen. Forslag til opdateringen kan sendes til [arkitektur@digst.dk](mailto:arkitektur@digst.dk). Det forventes, at referencearkitekturen senest vil blive konsolideret på baggrund af erfaringerne fra ovennævnte projekter omkring årsskiftet 2020/21.

Bemærk, at specifikke dataområder, opgaver, myndigheder og it-systemer, der nævnes i nærværende dokument, skal betragtes som eksempler. Konkrete aftaler og planer for anvendelsen afklares i fællesoffentlig regi i af styregruppen for digital kommunikation. Der henvises til [Mit overblik på Digitaliseringsstyrelsens hjemmeside](https://digst.dk/it-loesninger/borgerdk/mit-overblik/om-mit-overblik-paa-borgerdk/)

|     |     |     |
| --- | --- | --- |Versionsinfo
| Version | Dato | Ændring |
| --- | --- | --- |
| 1.0 | 17.05.2020 | Efter aftale i Udvalget for arkitektur og standarder er det ved en ændring af dokumentets titel og en række tilføjelser i teksten gjort tydeligt, at referencearkitekturen har tværgående digitale overblik som scope. Endvidere er tilføjet alternative tekster til billeder og tabeller, ligesom der er foretaget enkelte andre justeringer af hensyn til tilgængelighed. |

## Forord

Formålet med denne referencearkitektur er at bidrage til at skabe digitale løsninger, der giver mere gennemsigtighed for borgere og virksomheder i egne sager, ydelser, frister og andre data, som indgår samspillet mellem den enkelte borger eller virksomhed og den offentlige sektor. Scopet for denne referencearkitektur er digitale overblik, der indeholder data på tværs af domæner og på tværs af relevante myndigheder og eventuelle private aktører.

Borgernes tillid til offentlige myndigheders behandling af data er afgørende for den fortsatte udvikling af en mere sammenhængende digital offentlig sektor. Det er et fælles ansvar på tværs af stat, kommuner og regioner at sikre, at borgerne er trygge ved digitaliseringen og har tillid til den offentlige sektors behandling af personoplysninger.

Tilsvarende forhold er gældende på virksomhedsområdet, hvor der naturligvis er andre forhold og hensyn, der skal tages i betragtning.

Derfor skal referencearkitekturen også kunne anvendes til at udvikle forskellige konkrete løsningsarkitekturer, der hver især på bedste vis understøtter de behov, som borgere og virksomheder har for overblik over egne data.

Denne referencearkitektur giver en fælles beskrivelse på konceptuelt niveau af de begreber og sammenhænge, der er væsentlige for at forstå og arbejde med det konkrete design og implementering af løsninger, der viser tværgående digitale overblik. Referencearkitekturen dækker de otte perspektiver, som Hvidbogen om fællesoffentlig digital arkitektur beskriver: Styring, Strategi, Jura, Sikkerhed, Opgaver, Information, Applikation og Infrastruktur. Referencearkitekturen spænder med andre ord fra vision, mål og fastlæggelse af arkitektoniske principper og identifikation af de vigtigste juridiske og sikkerhedsmæssige rammer og begrænsninger til beskrivelse af de nødvendige forretningsmæssige og tekniske kapabiliteter.

## Resumé

Referencearkitektur for tværgående digitalt overblik for borgere og virksomheder sætter pejlemærker for offentlige it-løsninger, der skal bidrage til gennemsigtighed, kvalitetsudvikling og effektivsering af den offentlige service ved at give borgere og virksomheder et bedre tværgående digitalt overblik over deres anliggender med det offentlige.Referencearkitekturen understøtter realiseringen af initiativet _Mit Overblik_ i den fællesoffentlige digitaliseringspagt og Virksomhedsoverblik i den fællesoffentlige digitaliseringsstrategi, og den er udarbejdet i regi af initiativ 1.3 _Overblik over egne sager og ydelser_ i Den fællesoffentlige Digitaliseringsstrategi 2016 – 2020. Scope favner således begge disse initiativer. Referencearkitekturen skal dels anvendes til at støtte initiativerne med den konkrete løsningsudvikling, herunder udvikling af fællesoffentlig arkitektur, standarder og komponenter dels støtte de myndigheder og deres leverandører, som skal bidrage med data eller vise overblik på egne udstillingsplatforme. Denne referencearkitektur indgår i tæt sammenhæng med de øvrige referencearkitekturer i den fællesoffentlige digitale rammearkitektur (FDA).

Referencearkitekturen tager udgangspunkt i følgende vision for tværgående digitalt overblik[\[1\]](#Fodnote 1):

Borgere og virksomheder oplever, at de har overblik over fx status, beløb, aftaler og frister i forbindelse med aktuelle sager, ydelser og indberetninger ved anvendelse af de offentlige digitale kanaler. Borgere og virksomheder får bedre overblik over relevant information på det relevante sted.

Realiseringen af denne vision defineres som _evnen til - på tværs af den offentlige sektor - at kunne levere relevant information vedrørende den enkelte borgers og virksomheds sager, ydelser, betalinger, frister mv., som er konkret, relevant og overbliksskabende for den enkelte borger eller virksomhed._ Denne evne (kapabilitet) kaldes i denne kontekst _overblik._

Visionen udmøntes i fire overordnede brugerbehov:

1. **Relevant information præsenteres for brugeren i et forståeligt sprog, som understøtter overblik.**  
   Det kan eksempelvis dreje sig om sager, ydelser, aftaler eller frister som formuleres med et ordvalg, der gør brugeren i stand til af forstå indholdet.
2. **Overblik skal indeholde information og data, der er relevante for brugersituationer på tværs af myndighedsskel.**  
   Det kan eksempelvis være relevant at udstille sagsdata fra både kommunale og statslige myndigheder i et overblik.
3. **Aktuelle anliggender med det offentlige skal være forståelige for brugeren.**
4. **Overblikket skal leveres gennem de kanaler, som brugeren foretrækker**[\[2\]](#Fodnote 2)**.**

Referencearkitekturen fastlægger de principper, som offentlige it-løsninger, der bidrager eller udstiller overbliksfunktionalitet, skal overholde. Principperne er som følger:

1. [Informationer leveret til overblik er retvisende.](#princip-1-informationer-leveret-til-overblik-er-re)
2. [Information leveret til overblik kan distribueres gennem flere kanaler.](#princip-2-information-leveret-til-overblik-kan-dis)
3. [Overblik erstatter ikke myndighedsløsninger.](#princip-3-overblik-erstatter-ikke-selvbetjeningsls)
4. [Information leveret til overblik ledsages af oplysninger om, hvorledes brugeren kan få yderligere detaljer.](#princip-4-information-leveret-til-et-overblik-leds)
5. [Overblik er altid deklareret i forhold til, hvilke informationer brugeren kan forvente at finde i overblikket.](#princip-5-overblik-er-altid-deklareret-i-forhold-t)
6. [Overblik udstilles efter fælles model.](#princip-6-overblik-udstilles-efter-flles-model)
7. [Information, der indgår i et overblik, kan kategoriseres under de klassifikationer, som aftales fællesoffentligt.](#princip-7-information-der-indgr-i-et-overblik-kan-)
8. [Forretningslogik placeres så tæt på datakilden som muligt.](#princip-8-forretningslogik-placeres-s-tt-p-datakil)
9. [Sikkerhed følger data](#princip-9-sikkerhed-flger-data)
10. [Præsentationslag og orkestreringslag gemmer ikke data](#princip-10-prsentationslag-og-orkestreringslag-gem)

Referencearkitekturen beskriver et forretningsmæssigt målbillede med de væsentligste arkitekturbyggeblokke, som skal realiseres for at kunne levere det fællesoffentlige digitale overblik. Referencearkitekturen omfatter fælles terminologi for information i overblik, der kan vise relevante data med udgangspunkt i brugerens konkrete behov i en given situation.

Referencearkitekturen beskriver overordnet de metodiske rammer for begrebs- og datamodellering for fælles modeller til udstilling og dataudveksling.

Referencearkitekturen omfatter en række mønstre på forretningsmæssigt og teknisk niveau, der skal til for at skabe et tværoffentligt overblik over data fra de offentlige myndigheders forskellige registre og fagsystemer i samspil med allerede eksisterende digitale universer og løsninger samt myndigheders strategier for kommunikation med borgere og virksomheder.

Referencearkitekturen udpeger områder for fælles standarder og fælles komponenter og services i den samlede arkitektur for at danne og vise overblik. Udvikling, vedligehold og anvendelse af disse besluttes af styregruppen for digital kommunikation.

## Executive Summary (English)

This document outlines and explains a reference architecture for Transverse Digital Overview for citizens and businesses applicable for municipalities, regions, state agencies and ministries. This reference architecture is part of the implementation of the Danish public sector Digital Strategy 2016-2020. The reference architecture has been produced by a group of it-architects, business analysts and other experts from a number of public authorities.

This document outlines and describes a reference architecture for transverse Digital Overview for citizens and businesses and sets benchmarks for public IT solutions to contribute to transparency, quality and efficiency of the public service by providing citizens and businesses with a better digital overview of their relationships and affairs with the authorities across the public sector.

The reference architecture supports the realisation of the My Overview initiative in the Digitisation Pact and has been developed as part of the initiative _1.3 Overview of own cases and services_ in the Digitization Strategy 2016 - 2020. Scope thus embraces both of these initiatives. The reference architecture must be used partly to support the initiatives with the concrete development of it solutions, including the development of the common public architecture, related standards and components and partly to support the authorities and suppliers who will contribute with data or displays an overview on their own portals. This reference architecture is closely related to the other reference architectures in the Digital Framework Architecture (FDA).

The reference architecture is based on the following vision for digital overview:

Citizens and businesses experiences that they have an overview of, for example, the status, amounts, appointment and deadlines in connection with current cases, services and reporting using the public digital channels. Citizens and businesses get a better overview of relevant information in the relevant place.

The realization of this vision is defined as the _capability - across the public sector - to be able to provide relevant information regarding the individual citizen's and business’s cases, benefits, payments, deadlines, etc., which is concrete, relevant and overview-creating for the individual citizen or company_. This capability is called _overview_ in this context.

The vision is expressed in four general user needs:

1. Digital display and presentation of relevant information about e.g. cases, benefits, appointments and deadlines must be communicated in a language that the user can understand and that supports overview.
2. Overview must contain information and data relevant to user situations across government boundaries
3. The user must be able to understand his current affairs and relationship with the public authorities, and for example know when the user can expect answers from the public authorities and when the user is expected to act.
4. Providing overview for communication with the user must be possible through the channels the user prefers.

The scope for this reference architecture thus includes transversal digital overviews on a relatively high level. The scope does not on the other hand include digital overviews designed to meet the requirements for a partial domain.

The reference architecture establishes a set of principles that government IT solutions that contribute or exhibit overview functionality must adhere to. The principles are as follows:

1. Information provided to overview is correct.
2. Information provided to overview can be distributed through multiple channels.
3. Overview does not replace government self-service solutions.
4. Information provided to overview is supplemented by information on how the user can obtain further details.
5. Overview is always proclaimed according to what information the user can expect to find in the overview.
6. Information in overview is displayed according to a common model.
7. Information included in overview can be categorized under the classifications that are agreed upon by the parties in the public sector.
8. Business logic is placed as close to the data source as possible.
9. Security follows data
10. Presentation layers and orchestration layers do not store data

The reference architecture describes a business objective picture with the most salient architectural building blocks that must be realized in order to provide common public digital overview. The reference architecture includes common terminology for information at a glance that can display relevant data based on the user's specific needs in a given situation.

The reference architecture generally describes the methodological framework for modelling of concepts and data for common models used for exhibition and data exchange.

The reference architecture encompasses a number of business and technical patterns required to create a cross public overview of data from public authorities' various registries and case handling systems in interaction with existing digital universes and solutions, as well as government strategies for communication with citizens and businesses.

The reference architecture identifies areas for common standards and shared components and services in the overall architecture to create and display an overview. Decision for development, maintenance and use of these are made by the steering committee for Digital Communication.

## 0\. Introduktion

Denne referencearkitektur er udarbejdet som led i initiativ 1.3 _Overblik over egne sager og ydelser_, som indgår i den fællesoffentlige digitaliseringsstrategi 2016-2020 og programmet _Mit Overblik_, som indgår i den fællesoffentlige digitaliseringspagt_._ Referencearkitekturen indgår i den fællesoffentlige digitale arkitektur (FDA).

Den tilhører typen ”anvendelsesorienteret referencearkitektur”, idet den er målrettet anvendelse i forbindelse med udvikling og tilpasning af løsninger, der skal indgå i leveringen af et bedre tværgående overblik til borgere og virksomheder.

Udover anvendelsen i de fællesoffentlige projekter, der udspringer af ovennævnte initiativ og program, kan referencearkitekturen anvendes frit til inspiration for både offentlige og private aktører, der arbejder med udvikling af digitale overblik på tværs af organisationer, processer og systemer.

### Formål og værdi

Det overordnede formål med denne referencearkitektur er at sætte arkitekturrammer for, at der på tværs af den offentlige sektor kan tilbydes henholdsvis et bedre digitalt borgervendt og et virksomhedsvendt overblik over relevante data, som vedrører den enkelte borger eller virksomhed, og som det offentlige ligger inde med. Det kan fx være overblik over egne sager, ydelser, betalinger, frister, aftaler og lignende data, som er direkte relevante for den enkelte borger eller virksomhed.

Digitale overblik skal bidrage til at sikre, at den offentlige service leveres med høj kvalitet, effektivt, gennemsigtigt og sikkert. Borgere og virksomheder skal - nemmere end i dag – kunne få information om status, proaktiv information og svar på spørgsmål, de måtte have i forhold til deres egne anliggender med de offentlige myndigheder. De skal således gerne kunne undgå at skulle henvende sig fysisk eller telefonisk med spørgsmål om fx status på en igangværende sag eller størrelsen af kommende ydelser.

​Referencearkitekturen beskriver bl.a. den overordnede vision, strategiske kapabiliter, arkitekturprincipper, centrale begreber og logiske forretningtjenester samt tekniske komponenter og integrationer.

Referencearkitekturen skal anvendes til at støtte den konkrete løsningsudvikling, herunder udpegning af områder for udvikling og valg af fælles standarder og komponenter. Den skal støtte de myndigheder - og deres leverandører - som skal bidrage med data eller vise tværgående overblik på egne udstillingsplatforme.

Ved implementering af digitale overbliksløsninger skal alle kapabiliteter og tjenester, som er beskrevet i denne referencearkitektur, ikke realiseres 1:1, men ved at der udvælges det sæt, der er relevant for det givne forretningsmæssige scope. Eksempelvis vil implementeringen være forskellig på borger og virksomhedsområdet, blandt andet fordi der er forskellige brugerbehov, forskelle i portalernes roller i forhold til selvbetjeningsløsninger og forskelle i forhold til krav til de data, der skal indgå i overblik.

Værdien på konkret plan er, at de mange forskellige aktører, der skal bidrage til at realisere de politiske initiativer og skabe konkrete overbliksløsninger, har en fælles referenceramme for deres arbejde, herunder fælles begreber og terminologi samt principper og mønstre for løsninger, som gør, at det alt andet lige er nemmere at samarbejde og koordinere en så stor og kompleks opgave, som det er at skabe overblik på tværs af myndigheder.

### Scope

Scope for denne referencearkitektur er “tværgående digitalt overblik” forstået som _evnen til på tværs af den offentlige sektor digitalt at kunne levere relevant information vedrørende sager, ydelser, betalinger, frister mv., som er konkret, relevant og overbliksskabende for den enkelte borger eller virksomhed._

Et overblik kan fx være en liste over sager med angivelse af deres status eller et lidt mere detaljeret overblik over, hvad der er sket i de enkelte sager. Et overblik kan fx også vedrøre de økonomiske ydelser, man får, eller aftaler eller betalinger man skal være opmærksom på i den kommende tid.

Referencearkitekturen er gældende for information til tværgående overblik, hvor det er muligt og relevant at udarbejde en standardisering herfor. Det vil sige, hvor der er fælles egenskaber for data på tværs af datakilder, og hvor der er flere forskellige datakilder, der skal levere data, der skal kunne sammenstilles til fx en liste, som giver et samlet overblik over sager. Samt hvor disse data mest hensigtsmæssigt leveres via fælles metoder og infrastruktur, herunder fælles mekanismer til transformation, integration, udveksling og orkestrering af data.

Scopet omfatter således tværgående overblik på et relativt overordnet niveau. Scopet omfatter ikke andre typer af overblik, som fx alene begrænser sig til at skabe overblik inden for et specifikt domæne, hvor der kan være helt særlige behov og muligheder. Lokale overblik over fx en virksomheds tilskudssag, hvor brugeren får vist meget detaljeret information om sagens indhold og forløb, er ikke en del af scope for referencearkitekturen, da denne type overblik løftes af specifikke selvbetjeningsløsninger eller aftalte visninger på portaler. Overbliksvisninger kan indeholde link til selvbetjeningsløsninger, hvorved der skabes en sammenhæng mellem det overordnede centrale/tværgående overblik og detaljerede visninger i selvbetjeningsløsninger.

Detaljerede retningslinjer for præsentation af data ligger uden for scope. Med hensyn til retningslinjer for præsentation henvises særligt til Referencearkitektur for digital selvbetjening, Fælles krav til digitale løsninger samt for andre fællesoffentlige retningslinjer for præsentationslaget, herunder fælles metoder og visningsregler for overblik, som eventuelt måtte blive aftalt specifikt i forhold til præsentation af overblik.

### Anvendelse

En referencearkitektur skal hjælpe løsningsprojekter med at understøtte fælles, tværgående forretningsmål.

En referencearkitektur definerer fælles principper, begreber og arkitekturbyggeblokke.

En referencearkitektur udpeger områder for fælles løsningsbyggeblokke i form af fx specifikationer og komponenter.

![Figur 0.1.png](assets/Figur%200.1.png)

Figur 0.1 - Sammenhæng mellem Fællesoffentlig rammearkitektur, referencearkitekturer og understøttelse af myndighedernes forretningsmål

Denne referencearkitektur skal anvendes som vejledning og referenceramme for

* fællesoffentlig udarbejdelse af løsningsarkitekturer for borgerområdet og virksomhedsområdet med udgangspunkt i samspillet med portalerne borger.dk og Virk.
* fællesoffentlige valg/udarbejdelse af tekniske specifikationer og komponenter med henblik på realisering af overblik.
* den enkelte myndigheds udarbejdelse af løsningsdesign særligt med henblik på
  * integration til levering af data fra datakilder til overblik.
  * præsentation af overblik til slutbrugere på portaler o.l.
* review af løsningsbeskrivelser.
* udarbejdelse af opfølgende handlingsplaner og initiativer blandt digitaliseringsstrategiens parter med henblik på realisering af kapabiliteter.

### Målgruppe

Dette dokument er på forskellig vis relevant for tre overordnede målgrupper:

**Forretnings- og it-arkitekter** (løsningsarkitekter) tilknyttet offentlige digitaliseringsprojekter, der har til opgave at kravspecificere og designe løsninger, er den primære målgruppe og bør orientere sig i hele dokumentet med henblik på at kunne anvende dette aktivt i sammenhæng med relaterede dokumenter.

**Projektledere og beslutningstagere**, herunder forretningsansvarlige, digitaliseringschefer, it-chefer, afdelings- og kontorchefer og andre med rollen som systemejer kan med fordel læse de første dele af dokumentet: Strategi, Styring, Jura og Opgaver.

**Leverandører af offentlige it-løsninger** kan med fordel orientere sig i dokumentet i sin helhed.

### Centrale termer

Dette afsnit indeholder en beskrivelse af termer, der er centrale for læseren for at forstå referencearkitekturen. _Bilag B Begrebsliste_ indeholder definitioner og en samlet oversigt over referencearkitekturens begreber og terminologi. For generelle FDA-termer og begreber henvises [til undersiden om FDA begreber FDA begreber](/node/630).

| Central term                   | Beskrivelse                                                                                                                                                                                                                                                                          |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Tværgående digitalt overblik   | Evnen til - på tværs af den offentlige sektor - at kunne levere relevant information vedrørende den enkelte borgers og virksomheds sager, ydelser, betalinger mv., som er konkret, direkte relevant og overbliksskabende for den enkelte borger eller virksomhed.                    |
| Borgervendt kommunikation      | Kommunikation målrettet en borger, som opleves forståeligt og overskueligt, hvor der tages udgangspunkt i borgerens behov.                                                                                                                                                           |
| Virksomhedsvendt kommunikation | Kommunikation målrettet virksomheden som opleves forståeligt og overskueligt, hvor der tages udgangspunkt i virksomhedens behov, forstået som fx ejer, leder, medarbejder eller rådgiver/stedfortræder.                                                                              |
| Brugervendt kommunikation      | Fælles term for Borgervendt og Virksomhedsvendt.                                                                                                                                                                                                                                     |
| Myndighedsdomæne               | Forretningsområde som en myndighed er ansvarlig for.                                                                                                                                                                                                                                 |
| Brugerbehov                    | Behov set fra en borger eller virksomheds perspektiv.                                                                                                                                                                                                                                |
| Forretningsbehov               | Behov set fra et bestemt perspektiv som en digital løsning skal understøtte.                                                                                                                                                                                                         |
| Orkestreringskomponent         | Byggeblok, der samler data fra en eller flere datakilder og leverer et samlet resultat til anvenderne. Realisering af tjenester og funktionalitet placeret i orkestreringslaget.                                                                                                     |
| Domæneindeks                   | Byggeblok, der indekserer data og giver mulighed for hurtigere levering af relevante data til overblik inden for et datadomæne. Jf. referencearkitektur for deling af data og dokumenter vil domæneindeks være af typen implementeringsmønster Datadistributør (med brug af indeks). |
| Overbliksvisning               | Visning af overblik for et datadomæne, fx sag eller ydelser.                                                                                                                                                                                                                         |
| Detaljevisning                 | Visning af detaljer for en specifik instans af data, fx en sag eller ydelse.                                                                                                                                                                                                         |

### Tilblivelse og governance

Denne referencearkitektur er udarbejdet i regi af initiativ 1.3 i den fællesoffentlige digitaliseringsstrategi 2016-2020. Styregruppen for Digital Kommunikation er ansvarlig for endelig godkendelse af leverancen. Forud for endelig godkendelse har dokumentet været underlagt peer-review i regi af Styregruppen for data og arkitektur og publiceret i udkast til åben kommentering for interesserede med henblik på faglig kvalificering. Udvalget for arkitektur[\[3\]](#Fodnote 3) har ansvar for optagelse af referencearkitekturen som del af den fællesoffentlige rammearkitektur.

Referencearkitekturen er udarbejdet af Digitaliseringsstyrelsens Kontor for digital service (KDS). I udarbejdelsen har en arbejdsgruppe bidraget gennem en række af workshops. I gruppen har deltaget repræsentanter for KL, KOMBIT, ATP, Erhvervsstyrelsen og Digitaliseringsstyrelsen. Referencearkitekturen er udarbejdet over to perioder adskilt af en fase med uddybende analyser, pilotprojekter og teknisk PoC (Proof of Concept). Den er udarbejdet med konsulentbistand fra Devoteam og optimum IT, henholdsvis Strand og Donslund. De nævnte uddybende analyser og tekniske og brugervendte pilotprojekter er udført i samarbejde med bl.a. KL/KOMBIT, ATP, Styrelsen for Institutioner og Uddannelsesstøtte, Erhvervsstyrelsen (Virk) og Digitaliseringsstyrelsen (borger.dk). I forbindelse med disse har der indgået konsulentbistand fra Deloitte Digital, Nine og Netcompany.

Indholdsmæssigt er referencearkitekturen forholdsvis løsningsnær og anvendelsesorienteret og er på en række områder baseret på relevante erfaringer fra igangværende projekter og PoC-forløb på både borger og virksomhedsområdet. Referencearkitekturen indeholder derfor en række projektnære referencer som anvendelsesorienterede eksempler.

Denne referencearkitektur er del af rammearkitekturen i den fællesoffentlige digitale arkitektur (FDA). FDA-rammearkitekturen udfoldes bl.a. i en række referencearkitekturer, som hver dækker et emnefelt og gensidigt supplerer hinanden. De øvrige referencearkitekturer er i skrivende stund:

* Fællesoffentlig referencearkitektur for brugerstyring
* Fællesoffentlig referencearkitektur for selvbetjening
* Fællesoffentlig referencearkitektur for deling af data og dokumenter.

For en introduktion til og overblik over den samlede rammearkitektur samt relateret information henvises til [siden om rammearkitekturen](https://github.com/Faellesoffentlig-Digital-Arkitektur/Faellesoffentlig-rammearkitektur/blob/main/Faellesoffentlig-rammearkitektur.md), hvor denne referencearkitektur også publiceres.

Til konkrete implementeringsprojekter vil denne referencearkitektur blive suppleret af andre dokumenter i form af fx detaljerede begrebs- og datamodeller, dataudvekslingsformater, integrationsmønstre, snitfladebeskrivelser og vejledninger.

### Anvendt metode og notation

Referencearkitekturen følger den fællesoffentlige rammearkitekturs metoder og er udarbejdet efter Digitaliseringsstyrelsens retningslinjer for arkitekturdokumentation og med anvendelse af skabelon for referencearkitekturer. Anvendte notationer omfatter ArchiMate, UML og BPMN.

Referencearkitekturen er generelt udarbejdet, så den er så konsistent som muligt med andre arkitekturdokumenter og standarder udarbejdet i regi af den fællesoffentlige rammearkitektur.

Referencearkitekturen bygger på etablerede fællesoffentlige arkitekturprincipper, aftaler og retningslinjer vedrørende arkitektur, data og anvendelse af åbne standarder.

I forhold til ejerskab af de elementer, der indgår i dokumentets definitioner, jf. Bilag B Begrebsliste, markerer:

* **Fed tekst (i rød)**: At et element eller en relation ejes og defineres i denne referencearkitekturs begrebsmodel.
* Almindelig tekst (i blå): At et element eller en relation er kendt, men ejes og defineres et andet nærmere angivet sted, fx i andre referencearkitekturer eller i lovgivning.
* _Kursiv (i grå̊)__:_ At et element eller en relation er identificeret, men ikke nærmere defineret i denne referencearkitektur.

Fremtidige revisioner af denne referencearkitektur vil blive tilpasset revisioner af rammearkitekturen, herunder metoderammer og relaterede referencearkitekturer.

### Læsevejledning

Dette dokument følger skabelon for referencearkitektur under FDA-rammearkitekturen i Den fællesoffentlige digitaliseringsstrategi 2016-2020, hvor den overordnede opdeling er i henhold til otte grundlæggende arkitekturperspektiver og med hovedvægt på en række af de arkitekturprodukter, som er beskrevet i FDA retningslinjerne for formidling og dokumentation af arkitektur.

Kapitel 0 henvender sig til alle læsere. Det omfatter en generel introduktion til referencearkitekturens formål, scope, de centrale begreber omkring borger og virksomhedsvendte overblik, samt beskriver konteksten for dokumentets anvendelse og tilblivelse.

De følgende kapitler henvender sig til læsere med interesse for det enkelte perspektiv. Alle læsere bør læse de to kapitler Styring og Strategi for at få en uddybende forståelse af formål og kontekst. Tilsvarende giver kapitlerne Jura og Sikkerhed et overblik over væsentlige hensyn, begrænsninger og afgrænsninger.

Særligt kapitlerne Opgaver og Information henvender sig til forretningsarkitekter med information om den forretningsmæssige arkitektur, mens kapitlerne Applikation og Infrastruktur henvender sig til læsere med interesse for den tekniske arkitektur.

Læsere, der har ansvar for realisering af visning og/eller orkestrering af digitale overblik, skal især fokusere på afsnit for _Præsentation_ og _Orkestrering_ i kapitlerne _Opgaver_ og _Applikation_ samt kapitlerne _Sikkerhed_ og _Information_.

Læsere, der har ansvar for realisering af leverance af data til digitale overblik, skal især fokusere på afsnit for _Integration_ og _Datakilder_ i kapitlerne _Opgaver_ og _Applikation_ samt kapitlerne _Sikkerhed_ og _Information_.

Kapitel 1-8 omfatter beskrivelse i forhold til hvidbogens perspektiver.

* Styring: Beskriver de forretningsmæssige mål, mulige gevinster samt de styringsmæssige rammer omkring tværoffentlige overblik.
* Strategi: Beskriver de overordnede forretningsmæssige behov, visionen, mål og beskriver målbillede og strategiske kapabiliteter. Perspektivet omhandler også kort as-is situationen og den ønskede fremtidige målarkitektur samt de gap og forudsætninger, der skal opfyldes for at opnå målarkitekturen. Endvidere følger et afsnit med anbefaling om fælles standarder og løsningsbyggeblokke.
* Jura: Beskriver kort de juridiske bindinger, men har i øvrigt fokus på det aftalemæssige setup, der samlet skal etableres i forbindelse med et overblik.
* Sikkerhed: Omhandler sikkerhedsrisikobillede for overblik samt anbefalet sikkerhedsmodel for realiserede løsninger, der tager udgangspunkt i referencearkitekturen.
* Opgaver: Beskriver de vigtigste forretningskapabiliteter, der skal etableres og understøttes i forbindelse med overblik og overbliksløsninger samt forretningsaktører og roller, der indgår.
* Information: Indeholder en overordnet begrebsmodel for overblik og beskriver kort de vigtigste informationselementer, der indgår ift. at danne et overblik. Desuden beskriver dette kapitel i kort form en model for forløb for begrebs- og datamodel-arbejdet for de modeller, der skal anvendes i et specifikt overblik.
* Applikation: Omfatter applikationsarkitekturen og beskriver funktionalitet og applikationsservice i forhold til den overordnede lagdelte logiske arkitektur samt beskriver mønstre for mulige implementeringsscenarier ved implementering af et overblik.
* Infrastruktur: Beskriver de væsentligste forhold vedrørende den tekniske infrastruktur, som skal understøtte realisering af forretningsarkitekturen og applikationsarkitekturen beskrevet i denne referencearkitektur.

Dokumentet har et sæt bilag, der uddyber specifikke emner i referencearkitekturen, fx begreber og kataloger. Følgende bilag er del af referencearkitekturen:

* Bilag A Tjekliste: tjekliste til anvendere af referencearkitekturen.
* Bilag B Begrebsliste: liste over begreber defineret i referencearkitekturen og centrale begreber defineret andre steder, fx i referencearkitektur for deling af data og dokumenter.
* Bilag C Implikationer af Hvidbogens principper: Indeholder detaljeret beskrivelse af implikationer af Hvidbogen principper og arkitekturregler for referencearkitekturen.
* Bilag D Kataloger: En uddybende beskrivelse af kataloger og mulige implementeringsløsninger.
* Bilag E Oversigt over kilder og baggrundsmateriale: Liste over de kilder og baggrundsmateriale der er anvendt i forbindelse med udarbejdelse af referencearkitekturen.

## 1\. Styring

### Interessenter

Dette afsnit beskriver de vigtigste interessenter og deres interesser.

| Interessent                                                          | Interesse                                                                                                                                                                     |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Borgere                                                              | Er anvendere af udstillede overblik.                                                                                                                                          |
| Virksomheder                                                         | Er anvendere af udstillede overblik.                                                                                                                                          |
| Myndigheder (ministerier, styrelser, regioner, kommuner, andre)      | Leverer data til overblik.<br><br>Kan præsentere borger- eller virksomhedsvendt overblik på egne portaler og selvbetjeningsløsninger.<br><br>Anvender referencearkitekturen.  |
| Private udførere af offentligt relaterede opgaver                    | Kan evt. levere data til overblik (fx a-kasser, privatpraktiserende læger o.l.)<br><br>Kan evt. ønske at præsentere overbliksdata i egne portaler og selvbetjeningsløsninger. |
| Andre private aktører, fx NGO’er, banker og andre typer virksomheder | Kan evt. ønske at præsentere overbliksdata i egne portaler og selvbetjeningsløsninger.                                                                                        |
| Leverandører                                                         | Anvender referencearkitekturen ved udvikling og levering af overbliksløsninger.                                                                                               |
| Staten                                                               | Definerer overordnede mål og rammer for overblik sammen med KL og Danske regioner.                                                                                            |
| KL                                                                   | Definerer overordnede mål og rammer for overblik sammen med Staten og Danske regioner. Repræsenterer de kommunale interesser i udarbejdelse af referencearkitekturen.         |
| Danske regioner                                                      | Definerer overordnede mål og rammer for overblik sammen med Staten og KL.                                                                                                     |
| Borger.dk                                                            | Primær portal for visning af de borgervendte overblik.                                                                                                                        |
| Virk.dk                                                              | Primær portal for visning af de virksomhedsvendte overblik.                                                                                                                   |

### Forretningsmål

Referencearkitekturen er en del af realiseringen af initiativ 1.3 i Den fællesoffentlige Digitaliseringsstrategi 2016 – 2020.

#### Uddrag fra digitaliseringsstrategien 2016-2020

Den offentlige sektor skal være mere gennemskuelig. Borgere og virksomheder skal derfor have lettere adgang til at se, hvilke data om dem selv en myndighed har. Og brugerne skal have større indsigt i deres sager, ansøgninger, data og relationer med offentlige myndigheder.

I [Digitaliseringspagten](https://digst.dk/media/19919/digitaliseringspagt-en-ny-retning-for-det-faellesoffentlige-samarbejde.pdf) (marts 2019) mellem Regeringen, KL og Danske Regioner fremgår det at:

Regeringen, KL og Danske Regioner vil igangsætte en markant indsats, der skal give borgerne et bedre overblik og mere gennemsigtighed i den digitale offentlige service. Parterne er enige om, at øget gennemsigtighed og nemmere adgang til oplysninger om egne forhold er centrale elementer for at sikre, at borgerne er trygge ved digitaliseringen. Initiativet er et vigtigt skridt i retning af at styrke tilliden og realisere den fælles målsætning.

Således at der nu er tale om et bredt initiativ under overskriften _Bedre overblik og mere gennemsigtighed_, der mere detaljeret indebærer at:

\[..\] borgerne får et bedre digitalt overblik over de mest relevante oplysninger om dem selv og deres igangværende sager, udbetalte ydelser, betalinger og relevante aftaler – på tværs af staten, kommunerne og regionerne. Initiativet har til formål at give borgeren bedre adgang til oplysninger om sig selv og udvider dermed ikke mulighederne for deling af oplysninger mellem myndigheder. Som led heri skal borgerne tilbydes en bedre og mere personlig digital service bl.a. i form af påmindelser og notifikationer.

Regeringen, KL og Danske Regioner er enige om at etablere et Mit overblik, der skal give borgeren adgang til egne data på en lettilgængelig måde. Borgerens adgang til egne data skal være tilgængeligt der, hvor borgeren færdes, blandt andet på borger.dk. Overblikket vil indeholde en visning af relevante oplysninger, som det offentlige har om borgeren, samt borgerens igangværende sager og tildelte økonomiske ydelser.

### Styringsrammer

Digitale overblik kræver styring og koordinering på tværs af de aktører, der indgår i etablering af overblik af de elementer, der indgår i løsninger og det samlede flow for data.

Referencearkitekturen peger på følgende områder, hvor der skal etableres styring og governance:

* Overbliksvisninger.
* Datamodeller - indhold, udarbejdelse og versions/ændringsstyring.
* Klassifikationer - indhold, udarbejdelse og versions/ændringsstyring.
* Services mellem lagene i arkitekturen.
* Standarder og profileringer.

Desuden vil der være behov for et strategisk ejerskab, der tager stilling til, hvilke kanaler som data i overblik via fællesoffentlig infrastruktur skal kunne leveres til -herunder sikre videreudviklingen af den understøttende it-infrastruktur og hertil finansiering af den samlede drift og udvikling. Ved kanalstyring forstås både den tekniske kanal, portal, app etc, og beslutning om hvem og hvor data vises. Dvs., hvilke aktører kan vise hvilke data på hvilke tekniske kanaler. Ved beslutninger bør der anlægges en udefra-og-ind betragtning for at sikre det brugervendte perspektiv.

De styringsmæssige rammer for tværgående digitalt overblik er pt. under overvejelse og ikke afklaret endeligt.

Som led i digitaliseringspagten er der etableret en governance omkring de centrale elementer i forhold til at etablere Mit Overblik for borgere, hvor FODS-initiativ 1.3 Sags og Ydelsesoverblik naturligt bliver en integreret del af dette governancesetup.

Governance for Mit Overblik er etableret som et program med tilhørende styregruppe og har den primære styring omkring overbliksvisning og det forretningsmæssige scope.

Governance for datamodeller og klassifikationer samt heraf afledte services anbefales etableret centralt, hvor både nyudvikling og forvaltning forankres for at sikre konsistens på tværs.

Governance for de virksomhedsvendte elementer og løsninger anbefales forankret hos Erhvervsstyrelsen, det vil sige så tæt på Virk som muligt.

Realisering af referencearkitekturens elementer som fællesoffentlige løsninger og tilhørende governance, fx en orkestreringskomponent, anbefales forankret i Digitaliseringsstyrelsen.

De aftalemæssige rammer for governance ift. datakilder og præsentation af overblik oversigtligt er beskrevet nærmere i kapitlet om jura-perspektivet.

### Gevinster

Nedenstående belyser de centrale gevinster, der er mulighed for at opnå ved realisering af løsninger baseret på nærværende referencearkitektur. Gevinster opnås ikke ved realisering af overblik alene, da fx datakvalitet i datakilderne også er et vigtigt element i forhold til tillid og henvendelser[\[4\]](#Fodnote 4):

Nedenstående gevinster kan ved realisering af tværgående overbliksløsninger danne ramme for de kriterier, der opstilles for at afklare hvilket overblik, der skal implementeres, det informationsmæssige indhold for overblikket, og hvor kapabiliteter placeres i den aktuelle løsningsarkitektur. Der er tale om vurderede gevinster, som i visse i tilfælde er kvalitative gevinster og gevinster afledt af et politisk ønske om at sikre borgere og virksomhed større gennemsigtighed gennem nemmere adgang til egne data.

Gevinster kan både være positive og negative samt være spille sammen. Der kan fx være situationer, hvor én gevinst modvirker en anden. Fx kan øget overblik og indsigt på kort sigt give flere henvendelser, men samtidig give et pres på myndigheden for at forbedre datakvaliteten og på længere sigt opnå færre henvendelser og større effektivitet.

Påmindelser om frister, hvor en myndighed har behov for information fra brugeren, vil også kunne drive trafik til myndighederne og kunne afhjælpe nogle af de udfordringer, som omhandler for sent afleverede dokumenter og registreringer og dermed skabe hurtigere sagsbehandling samt bedre forudsætninger for at undgå rykkere.

|     |
| --- |Forretningsmæssige gevinster for borgere og virksomheder:
| Gevinster for borgere og virksomheder |
| --- |
| 1\. Tværgående overblik medvirker til, at brugere selv løser deres opgaver uden behov for hjælp fra en myndighed/sagsbehandler. |
| 2\. Større tryghed for borgere og virksomheder omkring myndigheders sagsbehandling. |
| 3\. En samlet kanal for borgere og virksomheder hvor de kan få overblik over deres engagementer med det offentlige. |
| 4\. Borgere kan få bedre overblik over eksempelvis ydelser på tværs af myndigheder. |
| 5\. Virksomheder kan få bedre overblik over fx frister i forhold indberetning mv. til myndigheder. |
| 6\. Brugere kan gennem overblikket observere eventuelle fejl og initiere proces til rettelse af fejl. |

|     |
| --- |Forretningsmæssige gevinster for myndigheder:
| Gevinster for myndigheder |
| --- |
| 1\. Brugerne informeres og opfordres til at løse deres udeståender gennem selvbetjening. |
| 2\. Muligheden for at drive trafik hen til myndighedernes egne selvbetjeningsløsninger (nudging). |
| 3\. Færre henvendelser fra virksomheder om frister og indberetninger ved at der er et klart og brugervenligt overblik over, hvornår virksomheden skal indberette oplysninger. |
| 4\. Større gennemsigtighed i data medvirker til øget tillid til myndigheder, der får en kanal, som er tilgængeligt 24/7. |
| 5\. Brugernes rapportering af eventuelle fejl kan initiere proces til rettelse af fejl og vil kunne bidrage til styrket fokus på datakvalitet god dokumentationspraksis. |
| 6\. Vil medføre færre indsigtshenvendelser, når borgere og virksomheder selv kan få vist overblikket, når de har brug for det. Den øgede gennemsigtighed kan på kort sigt give flere henvendelser. |
| 7\. Myndigheder kan nemmere præsentere egne og andres data ensrettet og harmoniseret og i nye overbliksvisninger. |

|     |
| --- |Forretningsmæssige gevinster for andre aktører:
| Gevinster for andre aktører |
| --- |
| 1\. Det er nemmere for portaler og andre visningsklienter at etablere og vise digitale overblik. |
| 2\. Andre projekter og initiativer kan udnytte arkitekturen til visning af data, fx log-overblik og samlet visning af samtykker. |

## 2\. Strategi

Afsnittet beskriver de strategiske rammer i form af vision/målbillede, som uddybes gennem overordnede forretningsmæssige og brugermæssige behov, de strategiske kapabiliteter samt principper, der skal være styrende for arkitekturen.

### Vision/målbillede

Referencearkitekturen tager udgangspunkt i følgende vision for tværgående digitalt overblik[\[5\]](#Fodnote 5):

Borgere og virksomheder oplever, at de har overblik over fx status, beløb, aftaler og frister i forbindelse med aktuelle sager, ydelser og indberetninger ved anvendelse af de offentlige digitale kanaler. Borgere og virksomheder får bedre overblik over relevant information på det relevante sted.

Hovedmålet er at skabe velfungerende digitale kanaler, så borgere og virksomheder får et forbedret og mere tryghedsskabende overblik over relevante data på tværs af de offentlige myndigheder. Dette skal gerne medføre, at borgere og virksomheder i mindre grad behøver at anvende alternative og analoge kanaler som fx telefon og personlig henvendelse.

> ”Digitaliseringspagten beskriver det borgervendte initativ, der indebærer, at borgerne får et bedre digitalt overblik over de mest relevante oplysninger om dem selv og deres igangværende sager, udbetalte ydelser, betalinger og relevante aftaler – på tværs af staten, kommunerne og regionerne. Initiativet har til formål at give borgeren bedre adgang til oplysninger om sig selv og udvider dermed ikke mulighederne for deling af oplysninger mellem myndigheder. Som led heri skal borgerne tilbydes en bedre og mere personlig digital service bl.a. i form af påmindelser og notifikationer. Borgerens adgang til egne data skal være tilgængeligt der, hvor borgeren færdes, blandt andet på borger.dk”[\[6\]](#Fodnote 6).

Den overordnede visionen blev i foranalysen ”Sags og ydelsesoverblik – behovsanalyse” opsummeret i fem eksemplariske temaer, illustreret i nedenstående tabel[\[7\]](#Fodnote 7). Det bemærkes, at den er udtryk for en langsigtet, illustrativ vision snarere end et konkret politisk aftalt målbillede.

![Figur 2.1.png](assets/Figur%202.1.png)

Figur 2.1 – Opsummering af vision og brugerbehov til fem eksemplariske temaer

I det foreløbige arbejde med realisering af denne vision er målbilledet bl.a. blevet yderligere detaljeret ved tidlige udkast til overbliksvisninger på borger.dk og Virk. Visningerne er illustrative og er ikke udtryk for, hvordan overblik visuelt bliver implementeret på henholdsvis fx borger.dk og Virk, ligesom det forventes, at disse vil blive udviklet og tilpasset iterativt efter agile metoder.

![Figur 2.2.png](assets/Figur%202.2.png)

Figur 2.2 - Eksempel på udkast overbliksvisning på borgerområdet

![Figur 2.3.png](assets/Figur%202.3.png)

Figur 2.3 – Eksempel udkast til visning af pligter og frister - virksomhed

Det skal endvidere være muligt at kunne komme videre til relevante selvbetjeningsløsninger fra overblikket, hvor yderligere detaljer kan vises. Fx om hvad der sker i ens ansøgning eller specifikationer på ydelsen.

Et virksomhedsvendt overblik kan tilsvarende være over relevante krav til indberetninger eller muligheder for ansøgninger med information om relevante frister. Det kan fx også være i form af en liste eller et årshjul på Virk, når brugeren skal foretage en handling.

Overblik vil ikke erstatte selvbetjeningsforløb eller forretningsfunktionalitet i eksisterende eller kommende selvbetjeningsløsninger, men er et supplement til disse løsninger, der kan vises selvstændigt eller indgå heri.

### Brugerbehov og forretningsbehov

Visionen og det overordnede målbillede uddybes i dette afsnit i en række brugerbehov og forretningsbehov. Et tværgående digitalt overblik skal imødekomme de forskellige brugere af offentlige tjenesters behov for at kunne forstå og overskue relevant overbliksskabende data og supplerende information om egne anliggender med det offentlige. Behovet for information vedrører blandt andet borgere og virksomheders sager, status og frister samt eksempelvis, hvilke ydelser en borger kan forvente, og hvornår de i givet fald udbetales, eller hvornår en virksomhed eksempelvis har frist for at foretage sine indberetninger.

De overordnede aktører er borgere og virksomheder, der repræsenteres af personer, som kan antage en række forskellige brugerroller, der afspejler forskellige brugerbehov og rettigheder fx som virksomhedsejere eller medarbejdere i virksomheder. De vil have forskellige behov og rettigheder alt efter, hvilken rolle de optræder i. Virksomheders behov vil tillige variere efter, om der er tale om små eller store virksomheder. 

1. **Relevant information præsenteres for brugeren i et forståeligt sprog, som understøtter overblik**  
   Når brugeren bliver præsenteret for et overblik, skal brugeren kunne forstå og overskue de oplysninger, der præsenteres.
   
   * Hvor det er relevant, skal der kunne anvendes harmoniseret, borgervendt terminologi, der understøtter, at data og information kan vises ensartet - fx vedr emne eller status på en sag.
   * Brugeren skal kunne modtage og forstå informationen fra det offentlige uden besvær og skal kunne føle tryghed i, at alt er i orden - fx at en henvendelse er modtaget og handlet på.

2. **Overblik skal indeholde information og data, der er relevante for brugersituationer på tværs af myndighedsskel**  
   En bruger kan have behov for information om flere forhold og fra flere kilder, som alle vedrører brugerens situation. Det digitale overblik skal:
   
   * kunne hjælpe brugeren ved netop at vise de relevante informationer for brugerens situation og hverken vise for meget eller for lidt information.
   * kunne henvise brugeren til, hvor yderligere information er tilgængelig, fx på en myndigheds lokale løsninger.
   * kunne fremsøge data fra flere myndigheder og it-systemer og sætte disse informationer sammen i en for brugeren relevant visning, der matcher brugerens kontekst.

3. **Aktuelle anliggender med det offentlige skal være forståelige for brugeren**  
   Når brugeren har interaktion med det offentlige, skal brugeren vide, hvilke handlinger og tidsfrister der skal overholdes.
   
   * Brugeren skal kunne få statusinformation over de aktuelle anliggender, som er i gang hos det offentlige, fx om oplysningerne er under behandling og hos hvem.

4. **Overblikket skal leveres gennem de kanaler, som brugeren foretrækker**  
   Sandsynligheden, for at kommunikationen mellem det offentlige og brugere lykkes, er større, når kommunikationen til brugeren sker gennem de kanaler, som brugeren foretrækker.
   
   * Relevante løsninger skal understøtte, at visning af overblik for kommunikation til brugeren kan ske på et udvalg af kommunikationskanaler, som løbende kan tilpasses brugernes ønsker inden for myndighedens kanalstrategi.
   * Igennem datadeling skal andre organisationer have mulighed for at tilbyde brugeren adgang til releveante dele af overblik, der hvor brugeren er. Eksempelvis vil bankerne kunne tilbyde overblik over udbetalinger i en netbanksløsning under forudsætning af, at brugeren har givet samtykke til visningen.

De forretningsmæssige behov er beskrevet gennem følgende sæt af eksempler på overordnede user stories, der er udtryk for specifikke brugersituationer i et anvenderperspektiv. De overordnede user stories er udvalgte eksempler, der vurderes at være repræsentative for brugerbehovene[\[8\]](#Fodnote 8). De vil i konkrete udviklingsprojekter kunne anvendes som udgangspunkt for nedbrydning i mere deltaljerede user stories.

Tabellen over user stories er opbygget efter følgende struktur:

* _Bruger_: Borger eller en repræsentant/medarbejder i en virksomhed.
* _Behov der skal opfyldes_: Overblik.
* _Gevinst_: Indfrielse af de(t) brugerbehov, der er identificeret ovenfor.

| <bruger>                                                       | <behov>                                                                                              | Så jeg opnår | <en eller anden gevinst>                                                                              |
| -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------ | ----------------------------------------------------------------------------------------------------- |
| Som bruger vil jeg i et                                        | **Overblik** kunne se mine anliggender med det offentlige i et for mig forståeligt sprog             | Så jeg       | Føler mig **tryg** ved, at myndigheden behandler mine sager og ydelser korrekt.                       |
| Som borger vil jeg via                                         | **Sagsoverblik** kunne se, hvad der er sket i min aktuelle sag samt få et overblik mine øvrige sager | Så jeg       | Har fået en **forventningsaf-stemning** ift. mine og det offentliges handlinger.                      |
| Som borger vil jeg med                                         | **Ydelsesoverblik** kunne se mine bevilgede ydelser                                                  | Så jeg       | Ikke bliver **overrasket** over pludselige ændringer i udbetalinger.                                  |
| Som repræsen-tant for/med-arbejder i en virksomhed vil jeg via | **Fristoverblik** kunne få synlighed i **frister** på tværs af myndigheder                           | Så jeg       | Føler mig **tryg** ved, at jeg ikke overskrider en frist, og ved hvornår jeg skal indberette/anmelde. |
| Som repræsen-tant for/med-arbejder i en virksomhed vil jeg via | **Overblik** se om virksomhedsændringen er gået igennem                                              | Så jeg       | Er **bekræftiget** i, at anmeldelse, jeg har sendt, er modtaget.                                      |

### Strategiske kapabiliteter

De forretningsmæssige behov er grundlaget for de strategiske kapabiliteter, der er i scope for referencearkitekturen:

I den centrale forretningskapabilitet er _overblik_ defineret som _evnen til - på tværs af den offentlige sektor - at kunne levere relevant information vedrørende den enkelte borgers og virksomheds sager, ydelser, frister mv., som er konkret, direkte relevant og overbliksskabende for den enkelte borger eller virksomhed._

Denne overordnede kapabilitet kan nedbrydes i to underordnede kapabiliteter, som aktiveres på brugerens eget initiativ (pull):

* **Overbliksliste**: Visning af en samling af helt overordnede metadata på tværs af myndigheder og emner – fx alle eller et bredt udsnit af sager, ydelser, frister. Kan være filtreret, fx i forhold til et specifikt emne eller bruger.
* **Overbliksdetaljer**: Visning af udvalgte detaljer, herunder fx status og fremdrift på en sag, ydelse eller frister i den aktuelle kontekst, som fx ansøgning om boligstøtte og med mulighed for visning af yderligere detaljer.

Data suppleres med **metadata og supplerende information**, der muliggør, at brugeren tilbydes mulighed for forskellige handlinger på baggrund af overblikket, fx link til selvbetjeningsløsning hvor brugeren kan se yderligere detaljer. Dette vil som udgangspunkt ikke understøtte handlinger for brugeren direkte i en overbliksvisning, men derimod at brugeren kan guides eller viderestilles til relevante selvbetjeningsløsninger eller kontaktpunkter.

Det er del af visionen, at overblik skal kunne fungere proaktivt ved fx at give **påmindelser** om noget, som borgeren eller virksomheden skal være opmærksom på og handle ud fra, fx i form af en aftale eller en frist for en indberetning. Derfor kan der være datadomæner, hvor det på sigt skal være muligt at hente denne type data til visninger, der trækkes frem i brugergrænsefladen.

### Strategiske principper

Dette afsnit beskriver et sæt principper for overblik. Myndigheder og leverandører bør tage stilling til disse i forbindelse med konkret løsningsudvikling. Principperne anvendes desuden i forbindelse med specificering af fælles byggeblokke som orkestreringskomponent, standardiserede datamodeller og krav til snitflader.

Principperne beskriver de væsentligste egenskaber i forhold til overblik, som har betydning for at understøtte de overordnede fællesoffentlige visioner og mål for borger- og virksomhedsvendt overblik. Principperne har et snævert fokus på emnet overblik.

Principperne er underlagt de overordnede arkitekturprincipper i _Hvidbog om fællesoffentlig digital arkitektur_ (FDA) og supplerer disse. Implikationerne heraf er beskrevet i bilag C.

Principperne for overblik bør tillige anvendes i samspil med de emnespecifikke principper, der beskrives i andre FDA-referencearkitekturer. _Referencearkitektur for selvbetjening_ indeholder eksempelvis en række principper, som er direkte relevante for arkitekturen for tværgående digitalt overblik - se nedenstående boks, hvor implikationerne i forhold til overblik er beskrevet.

#### **Principper fra referencearkitektur for selvbetjening**

Nedenstående liste af principper fra referencearkitektur for selvbetjening er fundet specielt relevante i forhold til overblik, da de direkte har en implikation for referencearkitekturens indhold.

**Princip 2.** Selvbetjeningsløsninger er forståelige, nemme og intuitive at anvende for brugerne

* Implikationer af dette princip er, at det sætter retningslinjer for data, der vises i et overblik, både i forhold til præsentation, men også hvordan data kan harmoniseres på tværs bl.a. gennem fælles termer og detaljeringsniveau.

**Princip 4**. Brugerne oplever en sammenhængende service, også på tværs af myndigheder

* Implikationer er, at data på tværs af myndigheder skal opleves som et sammenhængende hele. Sammenhængen skal opleves uanset den digitale kanal, som brugeren vælger, hvorved det stiller krav til, hvordan arkitekturen understøtter dette, og at det ikke alene er et krav til brugergrænsefladen

**Princip 5**. Brugerne skal altid kunne se, hvilken myndighed der er ansvarlig for at levere en tjeneste

* Implikationer i forhold til overblik er, at brugeren tydeligt skal kunne identificere hvilke myndigheder, der har leveret hvilke data i et overblik

Denne referencearkitektur definerer også et eget sæt af principper, der supplerer ovenstående i forhold til at danne og vise et borger-/virksomhedsrettet overblik. Principperne indskærper emner inden for information, herunder hvordan information dannes og vises, da overblik er rettet mod borgere og virksomheder.

#### Princip 1: Informationer leveret til overblik er retvisende

Brugeren skal præsenteres for information i et overblik, der er retvisende og afspejler de data, myndighederne har i egne kildesystemer.

Rationale

* Brugerne skal kunne have tillid til informationerne i et overblik, og de skal matche de data, som myndighederne handler på. Informationerne skal derfor være retvisende og stemme overens med, hvad de enkelte myndigheder har registreret i egne kildesystemer.

Implikationer

* Kildesystemer skal være i stand til at udstille opdaterede informationer til overblik og gerne så tæt på nær realtid som muligt.
* Løsninger for designet til at vise et overblik skal sikre, at informationer, der indgår i et overblik, tilgås i nær realtid.
* Der skal være udpeget en systemejer, der kan sikre overholdelse af servicemål til fremsøgning af data til overblik.
* Hvis der er risiko for uoverensstemmelse mellem informationer i kildesystemer og i overblik, skal brugeren gøres opmærksom dette, fx ved at der vises en advarsel og evt. et tidsstempel for opdatering af oplysningerne.

#### Princip 2: Information leveret til overblik kan distribueres gennem flere kanaler

Overbliksdata skal kunne leveres til brugerne gennem deres foretrukne kanaler som fx fællesoffentlige portaler, myndigheders hjemmesider og apps[\[9\]](#Fodnote 9).

Rationale

* Brugeren skal have adgang til overblik over relevante informationer via de kanaler, som brugeren foretrækker. Det vil øge sandsynligheden for, at kommunikationen mellem borger og myndighed er succesfuld.
* Ved at data kan anvendes på flere kanaler, åbnes der for nye innovate løsninger og bedre brugeroplevelser. Eksempelvis vil en selvbetjeningsløsning kunne give en bedre brugeroplevelse, hvor der kan indgå overbliksdata fra flere myndigheder.
* Det bliver muligt at samle ensartet information på én kanal. Fx kan en samlet kommunikation af frister til virksomheder via virk.dk højne sandsynligheden for, at frister modtages og overholdes af brugeren.

Implikationer

* Det skal være let at dele og anvende overbliksdata. Arkitekturen skal derfor indeholde et orkestreringslag, som kan indhente fra mange datakilder, sammenstille disse og distribuere dem til relevante visningsklienter.
* Der skal defineres retningslinjer for levering af data til orkestreringslaget, som de deltagende myndigheder skal følge, således at det er muligt, at orkestreringslaget kan distribuere til flere kanaler.
* Myndighederne skal have en implementeringsstrategi for, hvordan data til overblik leveres på en ensartet måde fra kildesystemer og samtidig anvender de digitale universer, som allerede findes.
* Der skal være udpeget et strategisk ejerskab, der tager stilling til, hvilke kanaler som data i overblik via fællesoffentlig infrastruktur skal kunne leveres til. Ved beslutninger anlægges en udefra-og-ind betragtning for at sikre det brugervendte perspektiv.

#### Princip 3: Overblik erstatter ikke selvbetjeningsløsninger

Overblik skal give borgere og virksomheder et tværgående overblik, men det er en tilføjelse, der ikke ændrer på myndighedens ansvar for kommunikation til borgeren og virksomhederne fx i afgørelser mv. via kanaler som Digital post og egne selvbetjeningsløsninger.

Rationale

* Overblik er et supplement til de lokale og domænespecifikke løsninger, der viser og giver adgang til data, som myndigheder har om borgere og virksomheder.

Implikationer

* Myndigheder skal stadig udvikle og vedligeholde egne løsninger, der viser detaljer, og hvor borgere og virksomheder kan foretage handlinger.
* Myndigheder skal sikre, at der kan linkes fra overblik til relevante handlemuligheder.

#### Princip 4: Information leveret til et overblik ledsages af oplysninger om, hvorledes brugeren kan få yderligere detaljer

Brugeren skal have mulighed for at få adgang til mere detaljeret data og information i forhold til, hvad der vises i overblikket eller blive informeret om, hvor brugeren kan henvende sig for at få mere information.

Rationale

* I tilfælde af at der er yderligere data og information tilgængeligt via en anden platform, skal brugeren gives let adgang via link.
* Brugeren bør nemt kunne navigere fra overblikket til detaljerne i eksempelvis en sag eller ydelse for dermed at øge brugerens forståelse af de data, der er registreret. Disse data kan fx være udstillet i en lokal løsning.
* Brugerens større overblik og forståelse af egne data og relevante informationer vil bevirke, at brugeren føler tryghed og tillid, hvilket kan medføre, at myndigheder får færre henvendelser i behandling af brugerens anliggende.

Implikationer

* Myndigheder skal sikre, at data leveret til overblik tilføjes information om mulighederne for, at brugeren kan se eller på anden måde få yderligere detaljer.
* Visningsklienter, – fx borger.dk eller en domæneportal eller lokal myndighedsportal – der udstiller overbliksdata, skal udstille relevant information om, hvor brugeren kan få yderligere information og relevante links, så brugeren kan navigere fra overblikket til fx en lokal selvbetjeningsløsning, portal eller app.

#### Princip 5: Overblik er altid deklareret i forhold til, hvilke oplysninger brugeren kan forvente at finde i overblikket

Brugeren informeres i præsentationslaget om, at overblikket ikke er udtømmende.

Rationale:

* Brugeren undgår at overse vigtige henvendelser, aftaler eller lignende med offentlige myndigheder.

Implikationer:

* Præsentationslaget skal indeholde klar og tydelig information om, hvilke oplysninger brugeren kan forvente at finde i overblikket.
* Brugeren skal, hvor det er relevant, informeres i et klart og tydeligt sprog om, at et fravær af informationer om eksempelvis en frist, aftale eller sag ikke er ensbetydende med, at en sådan ikke findes.
* Brugeren skal oplyses om, hvor brugeren skal henvende sig for at finde fuldstændige oplysninger inden for et givent område.

#### Princip 6: Overblik udstilles efter fælles model

Data, der udstilles i et overblik, skal overholde fælles begrebs- og datamodel, så data fremstår som et samlet overblik.

Rationale:

* Data i overblik skal for anvenderen fremstå ensartet og i et for anvenderen forståeligt sprog.
* Overblik består af en række standardiserede typer forretningsobjekter fx sag, ydelse, frist og aftale.

Implikationer:

* Data, der indgår i overblik, transformeres, hvor det er relevant, med brug af fælles klassifikationer til fælles brugervendte termer.
* Der designes og vedligeholdes en fælles udstillingsdatamodel og tilhørende klassifikationer, der implementerer de fælles termer.
* Dataansvarlige for kildesystemer skal sørge for, at informationer til overblik leveres på en ensartet måde efter fælles udstillingsdatamodel og i et for brugeren forståeligt sprog.

#### Princip 7: Information, der indgår i et overblik, kan kategoriseres under de klassifikationer, som aftales fællesoffentligt

Anvendelse af fælles klassifikationer skal bidrage til, at overblik viser de rette data fra de rette it-løsninger og medvirke til at gøre information i overblik forståelig for brugeren. Eksempelvis er emneklassifikationer egnede til at definere en klar kontekst, og mindre taksonomier til beskrivelse af fx sagstatus er velegnede til at understøtte sammenstilling af data i lister og tabeller, så brugeren nemmere kan få overblik. Der vil være både tekniske og brugervendte klassifikationer, hvor brugervendte klassifikationer er data, der vises for brugeren, mens tekniske klassifikationer alene anvendes i selve oprettelsen af visningen fx for visuel fremhævning af udvalgte data.

Rationale

* Anvendelse af fælles klassifikationer skal sikre at uanset hvilken kanal data leveres gennem, så kan data ordnes og vises på en ensartet måde for brugeren.
* Det kan være nødvendigt at ordne data i enkle strukturer ved hjælp af klassifikationer, der anvendes til at skabe ensartethed og letforståelighed på tværs af forskellige opgaveområder, myndigheder og kildesystemer. Fx vedrørende emner, status, hændelser og handlinger.
* Det kan være nødvendigt at oversætte termer fra kildesystemer til brugervendte termer for at gøre data forståelige for målgrupperne blandt borgere og virksomheder bl.a. ved at anvende et mere hverdagsnært sprogbrug og forenklede taksonomier.

Implikationer

* Der skal laves aftaler om, hvordan fælles klassifikationer skal anvendes. Herunder udarbejdelse, vedligehold, udstilling/distribution samt anvendelse i forbindelse med implementering hos datakilder og visningsklienter.
* Datakilders dataansvarlige skal tage stilling til, hvordan fælles klassifikationer understøttes, herunder hvordan eventuel transformation håndteres. En oversættelse bør ske i eller så tæt på datakilden som muligt.
* Visningsklienter skal kunne anvende relevante fællesoffentlige klassifikationer, som understøtter levering af overblik.

#### Princip 8: Forretningslogik placeres så tæt på datakilden som muligt.

Forretningslogik, der håndterer understøttelse af fælles datamodeller i overblikket, skal placeres tæt på datakilden.

Rationale

* Den nødvendige forretningsviden og indsigt, der er grundlaget for at implementere forretningslogik til understøttelse af fælles datamodel, findes hos den myndighed, der ejer datakilden.
* Det kan være nødvendigt med brug af forretningslogik til at transformere data fra intern model til ekstern model for at danne data, der giver brugeren et relevant overblik. Fx så ”en sag” eller ”en ydelse” udstilles på en konsistent og ensartet måde for borgeren.
* Vedligeholdelse og aftestning optimeres, ved at forretningslogik ligger tæt på datakilden.

Implikationer

* Realisering af byggeblokke, der i arkitekturen ligger tæt på datakilden, ejes af myndighed, der er ansvarlig for datakilden.
* Ved afgørelse af hvor forretningslogik bedst placeres, prioriteres placering tæt på datakilden.

#### Princip 9: Sikkerhed følger data

Sikkerhed følger data således, at der anvendes samme sikkerhedspolitikker og sikkerhedsmetoder på data, uanset hvor data behandles.

Rationale:

* Den dataansvarlige er ansvarlig for data og den databehandling, der udføres, og skal sikre, at dette overholdes i forhold til den registrerede.
* Rettigheder i forhold til data håndhæves ensartet, hvor data behandles.

Implikationer:

* Databehandlere skal sikre, at datakildens adgangspolitikker overholdes.
* Der anvendes fællesoffentlige komponenter til styring af sikkerhed.

#### Princip 10: Præsentationslag og orkestreringslag gemmer ikke data

Data gemmes ikke af præsentationslaget eller orkestreringslaget, men kan opbevares temporært, så længe brugeren har en aktiv session.

Rationale:

* Data, der vises i overblik, er konsistente med data hos datakilder.
* Minimering af risici for tab af fortrolighed og informationssikkerhed
* Reducere kompleksiteten i forhold til dataansvar og aftaler
* Minimering af datakopier

Implikationer:

* Data gemmes ikke som kopidata i orkestreringslaget eller præsentationslaget.
* Visningsklienter må ikke gemme data udover cache til visning i den enkelte, aktive session.

### Udgangspunkt (as-is situation)

Dette afsnit beskriver kort as-is for overbliksløsninger. Referencearkitekturen skal understøtte, at målene kan realiseres med respekt for allerede eksisterende digitale universer og løsninger samt myndigheders strategier for kommunikation med borgere og virksomheder.

Der findes i dag overbliksløsninger i form af de fællesoffentlige portaler borger.dk og Virk, der for henholdsvis borger og virksomhedsområdet kan give en vis grad af overblik[\[10\]](#Fodnote 10). Desuden findes der en række områdespecifikke overbliksløsninger fx sundhed.dk på sundhedsområdet, BBR.dk på ejendomsområdet og Aula på grundskoleområdet. Myndigheder som SKAT, Styrelsen for Arbejdsmarked og Rekruttering, Styrelsen for Institutioner og Uddannelsesstøtte, Familieretshuset og enkelte kommuner har udarbejdet it-løsninger, som i forskelligt omfang kan tilbyde borgerne et niveau af adgang til lokale overblik med domænespecifikke data.

Der findes ikke en fælles tværoffentlig ensartet tilgang eller metodik for at give borgerne eller virksomhederne overblik over deres anliggende med det offentlige, og der findes ikke et overblik på tværs af myndigheder og myndighedsniveauer. Brugeren oplever i dag selv at være ansvarlig for at skabe overblikket og sammenhængen, når brugerens anliggende går på tværs af myndigheder.

Foranalysen ”Sags- og ydelsesoverblik – Designanalyse af Sags- og ydelsesoverblik på borger.dk og virk.dk” (Deloitte, august 2017) peger på udfordringer for brugerne med at forstå information fra det offentlige i form af forståelse af myndighedernes sprog og termer[\[11\]](#Fodnote 11).

Erfaringer fra ADDA-projektet[\[12\]](#Fodnote 12) og de gennemførte PoC’er[\[13\]](#Fodnote 13) på overblik viser ligeledes, at de data, som skal anvendes til at danne overblik, skal følge en fælles datamodel og tilhørende klassifikationer.

Data i fagsystemer følger ikke nogen fælles model; der er forskellige modeller fra myndighed til myndighed fra fagområde til fagområde og fra leverandør til leverandør. Der er områder med store fagsystemer, som udgør de facto standarder på det pågældende område. Der findes også domæner med standardisering fx på det kommunale område, hvor man i arbejdet med monopolbrud og rammearkitektur har taget de eksisterende OIO Sag og Dokument-standarder[\[14\]](#Fodnote 14) i brug. Men set ud over det samlede it-landskab i det offentlige er der en heterogen anvendelse af datamodeller og repræsentationer af data til overblik, der ikke umiddelbart kan anvendes i overbliksløsninger.

### Målarkitektur (to-be situation – resumé)

I dette afsnit beskrives et konceptuelt overblik over de vigtigste elementer i målarkitekturen. Først beskrives de overordnede områder i det samlede tekniske økosystem, og dernæst introduceres de vigtigste forretningstjenester, som skal etableres for at realisere ovenstående vision og mål. Målarkitekturen er abstrakt og forholder sig ikke til hvor og af hvem, der konkret etableres overbliksløsninger.

Tværgående digitalt overblik kan udstilles i de fællesoffentlige portaler, i dedikerede løsninger på fagområder, på myndighedernes egne hjemmesider og på andre digitale kanaler, som brugerne anvender og efterspørger.

Et sigte med referencearkitekturen er, at der kan udvikles nye gode digitale overblik på tværs af myndigheder, og at disse udstilles som services, der både kan tilgås af en bruger og af et system via et API. Derfor er en central del af arkitekturen baseret på, at det skal være nemt at dele standardiserede data til overblik til forskellige kanaler via en central orkestreringskomponent, der udstiller en række services. En service kan fx udstille overbliksdata om, hvad der udbetales i uddannelseshjælp og boligstøtte, således at myndigheder eller andre kan udvikle visninger vendt mod en konkret målgruppe på egne kanaler.

Nedenstående to figurer illustrerer målarkitekturen på henholdsvis et konceptuelt og (overordnet) logisk niveau med fokus på de vigtigste tjenester. Arkitektur omfatter i princippet et samlet økosystem, der understøtter de ønskede kapabiliteter. Den fulde arkitektur indeholder fire lag og to områder, som går på tværs af de fire lag.

![Figur 2.4.png](assets/Figur%202.4.png)

Figur 2.4 Konceptuel målarkitektur

![Figur 2.5.png](assets/Figur%202.5.png)

Figur 2.5 Overordnet logisk målarkitektur med fokus på forretningstjenester

* **Præsentationstjenester** er de tjenester, der leverer brugergrænsefladen og præsenterer overbliksdata til brugeren. Det kan fx være en portal, en web-selvbetjeningsløsning eller en mobil-app.
* **Orkestreringstjenester** er de tjenester, der leverer sammenstillet overbliksdata til et givent overblik for brugeren i en relevant kontekst - her vist som aktører.
* **Integrationstjenester** er et teknisk lag, som har til opgave at indhente relevante data og konvertere/transformere samt berige data til fælles udstillingsmodel, så orkestrering kan sammenstille data til det specifikke overblik. I praksis vil dette lag typisk blive realiseret som et fælles domæneindeks for et givent domæne eller eventuelt med brug af et staginglag, der kan udstille data på vegne af legacy-systemer, så de kan indgå i arkitekturen.
* **Datakilder og grundlæggende tjenester** omfatter de registre og fagsystemer, der skal levere data til overblik såvel som uddybende detaljeret information, hvor det er relevant.
* **Kataloger** som støtter integrationstjenester i forbindelse med berigelse og eventuel transformation af data til levering til overblik. Det er fx kataloger over selvbetjeningsløsninger og datakilder samt datamodeller og særligt klassifikationer, der anvendes til at transformere og berige overbliksdata
* **Brugerstyringstjenester** der skal understøtte brugerstyring og adgangskontrol på tværs af de fire lag.

Kapitel 5 uddyber målarkitekturen i et forretningsperspektiv og kapitel 7 i et teknisk perspektiv.

#### Forskellige implementeringsscenarier

Overblik kan realiseres på mange måder. Denne referencearkitektur definerer en samlet arkitektur, der skal kunne understøtte, at data fra mange kilder kan vise på mange måder på mange visningsklienter. Derfor indeholder den fulde arkitektur de beskrevne fire lag, men over tid vil der være forskellige varianter, der kan komme i spil i konkrete projekter og integrationsløsninger. Nedenstående figur illustrerer dette.

![Figur 2.6.png](assets/Figur%202.6.png)

Figur 2.6 - Implementeringsscenarier

Direkte integration er fx mulig her og nu, men vil på sigt kunne give en stor kompleksitet - også kaldet ”integrationsspaghetti” - mellem datakilder, som kan være uønsket fx for et fagsystem. Ved at indarbejde et integrationslag kan man samle og dermed afløfte en del af denne kompleksitet. Integration/datadistributør er således ikke obligatoriske, men en mulighed.

Fx er de tidlige versioner af Mit Overblik på borger.dk udarbejdet ved hjælp af dele af KOMBIT støttesystemer, der har fungereret som domæneindeks. På borgerområdet udvikles der en orkestreringskomponent. En datakilde vil kunne integrere direkte til denne, hvis den overholder aftalte standarder eller vil kunne levere via et integrationslag som fx KOMBITs støttesystemer. I det sidste tilfælde er den fulde målarkitektur i spil.

De to støtteområder _Kataloger_ og _Brugerstyring_ vil være relevante i alle scenarier, men det forventes, at de vil blive udviklet og modnet over tid i forhold til de behov, der er i forbindelse med overblik.

### Gaps og forudsætninger

Gaps og forudsætninger beskriver de emner, hvor der er et gap i mellem as-is situationen og det målbillede, der beskrives i dette dokument. Desuden beskrives en række væsentlige organisatoriske og tekniske forudsætninger, som en realisering af målbilledet forudsætter.

En væsentlig forudsætning og udfordring i forhold til at levere overblik, der giver værdi for brugerne, er, at de er til at forstå. Det betyder, at de data, der præsenteres, skal være nemme at overskue og forstå for borgere og virksomheder i forhold til den kontekst, som de befinder sig i.

De relevante data skal tilvejebringes fra myndighedernes it-systemer og præsenteres ensartet og sammenstillet. Myndighedernes sprog er i nogle tilfælde karakteriseret ved brug af lovnære formuleringer mv., som ikke er nemme at forstå for brugere, og it-systemer anvender endvidere typisk forskellige begrebs- og datamodeller. Hertil rummer en række af de eksisterende offentlige datastandarder mulighed for fortolkning og giver derved ikke garanti for, at begreber anvendes på en ensartet måde.

En forudsætning omkring data er, at der opnås enighed om anvendelse af fælles datamodeller for overblik med tilhørende standarder, at der er bred opbakning til fælles datamodeller, og at ansvar for mapning til disse fra eksisterende datamodeller og datatransformation anerkendes af datakilder. 

Det er ligeledes en forudsætning, at der skelnes mellem de relativt få data, der giver overblik og de mange detaljer, der fx kan være knyttet til en sag, men som ikke i sig selv bidrager til et overblik. Et overblik skal være enkelt og indeholde netop de relevante data, der giver brugeren en oplevelse af overblik. I nogle tilfælde kan der være behov for mere information og flere detaljer. Brugeren skal via et link kunne klikke fra et overblik til fx en dedikeret løsning, hvor den enkelte myndighed kan give adgang til mere detaljeret information. Det kan fx være en sagsafgørelse eller om indholdet af en konkret ydelse. Behov og muligheder vil variere fra myndighed til myndighed og vil nødvendiggøre forskelligartede løsninger i forhold til detaljeringsniveauer og visninger.

Den beskrevne arkitektur vil stille krav til den enkelte myndighed og de fagsystemer, der skal levere data til overblik. Data skal leveres i henhold til fælles datamodeller, og data skal have en fornøden forretningsmæssig kvalitet til at indgå i overblik. For legacy-systemer vil det kræve en større indsats for den enkelte myndighed, hvor det for en række systemer vil være nødvendigt at implementere eget staginglag eller domæneindeks.

Ved nyanskaffelser og systemmoderniseringer anbefales det at inddrage aspekter omkring levering af data til digitale overblik, og hvordan de fornødne kapabiliteter beskrevet i denne referencearkitektur bedst understøttes som en integreret del af den nye løsning.

### Migrering til denne referencearkitektur

Migreringsafsnittet beskriver ganske kort den overordnede ramme for migrering.

Desuden beskrives den overordnede plan for migrering fra AS IS til realisering af målbilledet med udgangspunkt i Digitaliseringspagten. Afsnittet beskriver scenarier for migrering hen imod realiseringer af referencearkitekturens byggeblokke. Scenarierne fokuserer primært på, hvorledes data-domæner og datakilder bliver integreret i realiseringer af referencearkitekturen.

Den overordnede ramme er, at der med digitaliseringsstrategien og digitaliseringspagten er taget hul på etableringen af de beskrevne kapabiliteter. Udviklingen vil ske iterativ både på borger- og virksomhedsområdet. Portalerne borger.dk og virk.dk vil initielt være drivende for udviklingen, og vil som de første realisere målbilledet. Dette vil ske på forskellige måder, som matcher de forskellige behov, men vil blive koordineret mest muligt, hvor det er relevant. Fx omkring standardiserede datamodeller og snitflader. Det forventes, at der startes med MVP-løsninger – (Minimal Viable Product), og at de forskellige kapabiliteter realiseres i takt med modning og erfaringer. Det vil både gælde datadomæner og tjenester som kataloger, fuldmagt og samtykke.

På sigt forventes det, at der vil komme anvendelser af overbliksdata på domæneportaler, i dedikerede selvbetjeningsløsninger og apps. Sådanne præsentationsløsninger vil på sigt kunne være med til både at drive behov for data og funktionalitet og vil kunne bidrage til den samlede værdiskabelse.

#### Etablering af overblik på borgerområdet

Etableringen af overblik på borgerområdet gennemføres trinvist frem mod 2024.

Nedenstående illustrerer dette forløb.

![Figur 2.7.png](assets/Figur%202.7.png)

Figur 2.7 - Etablering af Mit Overblik på borgerområdet

Udvælgelsen af områder og data sker under hensyntagen til, hvad der giver mest værdi for borgeren samt til områdernes modenhed og den løbende systemmodernisering. Hvilke konkrete data, der gøres tilgængelig på borgervendte digitale overblik, aftales løbende mellem parterne.

#### Etablering af overblik på virksomhedsområdet

På virksomhedsområdet eksisterer der på nuværende (primo 2020) tidspunkt ikke tilsvarende aftaler, som det er tilfældet med Digitaliseringspagten og økonomiaftalerne på borgerområdet. Der er gennemført en datakortlægning af myndighedernes virksomhedsdata, som potentielt kan indgå i et Virksomhedsoverblik. På den baggrund vil der bliver udarbejdet en plan for etablering af et overblik på virksomhedsområdet. Det forventes på nuværende tidspunkt at blive implementeret efter samme tidshorisont og principper som borgerområdet.

Udvælgelsen af områder og data og forventes at ske under hensyntagen til, hvad der giver mest værdi for virksomhedsbrugerne, hvilke myndigheder der ønsker at deltage samt til områdernes modenhed og den løbende systemmodernisering.

#### Modning af datadomæner til tværgående overblik

De forretningsmæssige afklaringer af hvilke data, der indgår i overblik, sker løbende.

For en række af disse data vil det gælde, at der er et potentiale for at standardisere dem fx ud fra et ønske om, at de skal kunne vises sammenhængende for brugereren og kunne vises på flere visningsklienter. I givet fald vil de give værdi, hvis de kan indsamles og distribueres standardiseret via en fælles orkestreringskomponent.

Pga. den iterative afklaring af data der skal indgå i overblik, vil der også ske en iterativ udvikling af standardiserede udstillingsdatamodeller. Dette skyldes også, at potentialet for standardisering ift. sammenstilling af data i et borger- henholdvis et virksomhedsvendt overblik ikke er fuldt kendt på forhånd, men erfares i takt med dialogen med myndighederne og brugerne.

Derfor vil der være situationer, hvor data initielt integreres direkte fra en datakilde, (fagsystem eller domæneindeks) uden at data er standardiseret og går via en orkestreringskomponent. På et senere tidspunkt kan der være sket en modning, som gør det relevant at migrere over til en fælles datastandard og integration via orkestreringskomponent.

#### Migreringsscenarie fra Direkte integration til Via Orkestrering

Scenariet migrering fra direkte integration til integration via orkestreringskomponent er illustreret i nedenstående figur.

![Figur 2.8.png](assets/Figur%202.8.png)

Figur 2.8 - Migreringscenarie for direkte integration til anvendelse af orkestreringskomponent

(NB! I figuren vises kun forskellen på, om der anvendes orkestreringskomponent eller ej. Integrationslaget kan indgå i begge situationer, men er ikke obligatorisk.)

Det forventes, at data fra flere og flere datadomæner over tid vil blive udstillet gennem en fælles orkestreringskomponent som beskrevet i denne referencearkitektur frem for gennem punkt til punkt integrationer. Det er naturligvis vigtigt at være så meget på forkant som muligt, men der kan undtagelsesvist være data, som først vises via en direkte integration med borger.dk, uden at der nødvendigvis er defineret en standard, som skal overholdes; men som senere skal genimplementeres, således at de kan overholde fælles standard og udstilles via den fælles orkestreringskomponent.

Der vil også ske en modning indenfor de enkelte datadomæner, hvor datamodeller udvides og tilpasses til ændrede forretningsmæssige behov. Desuden må det forventes, at den tekniske udvikling vil ændre på de foretrukne integrationsmønstre.

Undtagelsen beskrevet ovenfor kan opfattes som et worst case scenarium, som imidlertid i praksis kan være relevant af mange årsager. Dette giver et andet væsentligt migreringsscenarie, der som nævnt omfatter migrering af datakilder fra at levere overbliksdata gennem en direkte integration til brugergrænsefladen til at anvende realiseringer af arkitekturen beskrevet i denne referencearkitektur.

Dette scenarie er aktuelt, da data til Overbliksdata for en række datadomæner fx vil blive leveret direkte tidligt i realiseringen af Mit Overblik-programmet, fordi data ikke på gældende tidspunkt er kandidat til at blive omfattet af standardisering. Der ses følgende forløb for dette scenarie:

1. Data er udpeget som kandidat til visning i overblik.
2. Data vurderes ikke at være kandidat til standardisering, fx fordi der kun er identificeret en datakilde.
3. Der implementeres direkte integration mellem datakilde og brugergrænsefladen gennem proprietær datamodel, som parter kan enes om.
4. Integration og visning sættes i produktion.
5. På et tidspunkt revurderes data til at være kandidat til standardisering, fx. grundet at nye datakilder skal levere samme type data.
6. Der udarbejdes standard udstillingsdatamodel for datadomæne.
7. Datakilden skal ændre integration til at følge referencearkitekturen, så data til overblik sammenstilles og udstilles af orkestreringslaget (Orkestreringskomponent). Dvs. datakilden skal udstille de specificerede services (se Applikationsperspektiv - Datakilder).
8. Datakilden skal sikre, at krav og funktionalitet til Integrationslaget er opfyldt, herunder at transformation til standard udstillingsdatamodel er defineret og implementeret.
9. Brugergrænsefladen skifter fra direkte integration til at hente data via Orkestreringslaget på samme måde som for andre datadomæner, hvor der findes en standardiseret datamodel.

I kapitel 6: ”Information” beskriver proces og forløb for, hvorledes et nyt data-domæne håndteres ift. eventuel standardisering, og dermed hvordan det omfattes af referencearkitekturen.

### Anbefaling om fælles standarder og løsningsbyggeblokke

Afsnittet beskriver områder, hvor referencearkitekturen peger på kandidater for fælles tekniske standarder og profileringer samt kandidater for fælles løsningsbyggeblokke i form af fx applikationskomponenter eller infrastrukturservices.

Kandidater til fælles løsningsbyggeblokke og infrastrukturservices:

* Erfaring fra PoC for Orkestreringskomponent viser, at der med stor fordel kan anvendes tekniske standardprodukter ved implementering af orkestreringslagets funktionalitet, og anvende disse som standard infrastrukturservices fx understøttelse af parallelisering af kald til integrationslagets services.
* Fælles platform for udstilling af kataloger.
* Fælles platform for udstilling af klassifikationer.

Referencearkitekturen peger på følgende emner, hvor der med fordel kan udarbejdes fælles standarder og vejledninger:

* Fælles udstillingsmodeller for datadomæner som fx Sag, Ydelse, Gæld, Aftale.
* Fælles klassifikationer / kontrollerede udfaldsrum for udvalgte egenskaber i datamodeller som fx sagsemne, sagsstatus og harmoniserede beskrivende / forklarende ledestekster.
* Snitfladespecifikationer (pr overbliksservice pr datadomæne)
* Standard for udstilling af fælles kataloger fx klassifikationer, selvbetjeningsløsninger, datakilder og datamodeller. Standard omfatter taxonomi og servicegrænseflade.
* Vejledning om transformation og berigelse til fælles udstillingsmodel
* Vejledning og krav til brugergrænseflader der udstiller overblik.
* Vejledning om konfigurationslogning der skal foretages på de forskellige lag i arkitekturen.

## 3\. Jura

Beskriver de væsentligste bindinger i relation til lovgivning og aftalemæssige forhold samt juridiske krav i forhold til sikkerhed og privacy.

### Juridiske bindinger

De mest relevante love og forordninger med særligt fokus på dannelse og visning af overblik er:

* EU-databeskyttelsesforordningen (GDPR) beskriver pligter og rettigheder ved behandling af persondata. I sammenhæng med denne referencearkitektur er databeskyttelsesloven central, da en stor del af de data, der vises i et overblik, er personhenførbare på borgerområdet og i nogen grad på virksomhedsområdet. En række aspekter, der dækkes af GDPR, er relevante i forhold til videregivelse af persondata fra datakildesystemerne herunder databehandleraftaler og tilslutningsaftaler.
* Forvaltningsloven - mere specifikt vejledningsforpligtigelsen - er relevant for visning af overblik på den/de implementerede brugergrænseflader, da data samles fra flere myndigheder. Der henvises til Datatilsynets skabelon[\[15\]](#Fodnote 15) for oplysning/vejledning for detaljer, således at vejledningsforpligtigelsen opfyldes.

### Dataansvar og aftalestyring

Det datamæssige ansvar for data, der vises i overblik - herunder selve præsentation og konteksten fx på en portal -, ligger hos datakilden, hvilket danner fundamentet for det aftalemæssige setup, der skal etableres for et overblik. Nedenstående figur illustrerer det aftalemæssige setup, der skal etableres. Det skal bemærkes, at der her er taget udgangspunkt i persondata, som kræver databehandlerafttaler. For andre typer data kan der være et andet setup.

![Figur 3.1.png](assets/Figur%203.1.png)

Figur 3.1 – Setup for databehandleraftaler

I nedenstående beskrivelse af databehandleraftaler refereres der til lagene i arkitekturen, men ved indgåelse af de aktuelle aftaler, vil aftaleparten være den organisation/myndighed, der forretningsmæssigt er ansvarlig for implementeringen af funktionaliteten i laget.

**Datakilder** skal etablere databehandleraftaler med alle brugergrænseflader, der viser overblik samt med integrationslaget/Domæneindeks, alternativt Orkestreringslaget, hvis der leveres data direkte til Orkestreringslaget.

**Integration/Domæneindeks** skal etablere databehandleraftale eller underdatabehandleraftaler med Orkestreringslaget.

**Orkestrering** skal etablere databehandleraftale med hver brugergrænseflader, der viser overblik.

For at sikre at databehandleraftale-setupet er på plads for en given visning af overblik, og der kun vises data, hvor der foreligger en databehandleraftale mellem datakilden og præsentationen, er det et arkitekturkrav til Orkestreringslaget, at laget kender de indgåede databehandleraftaler og omfatter funktionalitet til at filtrere/afgrænse data i forhold til aftalerne.

Referencearkitekturen anbefaler, at der anvendes bedste praksis baseret på datatilsynets skabelon eller de facto standard-skabeloner for databehandleraftaledokumenter som basis for indgåelse af databehandleraftaler, da overblik ikke stiller specifikke krav til indhold af databehandleraftalerne.

**Deklarering/ansvarsfraskrivelse.** I forhold til brugergrænseflader, der viser overblik, anbefales det, at der altid vises en tekst med deklaration og evt. forbehold for de data, brugeren ser, aktualiteten af disse og hvordan data kan anvendes af brugeren. Det er fx ikke nødvendigvis de sidst opdaterede data, der vises i et overblik, da dette afhænger af datakildens muligheder for at levere data i nær-realtid.

### Logning af tilstand

For at kunne behandle henvendelser og eventuelle klager fra borgere og virksomheder i forhold til data, der er vist i et overblik, skal implementering af lagene i arkitekturen logge tilstanden for konfigurationen på det pågældende tidspunkt for visningen. For hvert kald mellem implementeringer af lagene i arkitekturen, der gennemføres for en given visning, skal det logges hvilken konfiguration, der er aktiv på kald-tidspunktet. Der er ikke krav om, at de aktuelle data, der vises i et overblik, skal logges, da overblik kun viser data, der leveres fra en datakilde. Som dataansvarlig er det myndigheden for datakilden, der sikrer, at data kan fremfindes eller på anden vis kan dokumentere data vist i et overblik.

### Læseadgang og samtykke

I situationer, hvor tredjepart kan have behov for at se samme overblik, som en given borger eller virksomhed har adgang til, vil det være fordelagtigt, hvis borgeren/virksomheden kan give tredjepart læseadgang hertil. Afgivelse og validering af læseadgang ses realiseret af NemLog-in fuldmagtsløsning (bemærk nedenstående om udfordringer omkring fuldmagt).

De situationer, der bør understøttes af læseadgang, vil fx være tilfælde, hvor en pårørende på borgerområdet eller en revisor eller lignende på virksomhedsområdet skal have adgang til at se borgerens henholdsvis virksomhedens overblik.

Da der ikke videregives data til andre end borgeren selv i forbindelse med data i overblik, specificerer referencearkitekturen ikke behov for understøttelse af samtykke, det vil sige hverken afgivelse eller tilbagetrækning af samtykke.

Fuldmagter og samtykker som datadomæner vil kunne vises på overblik på samme måde som andre datadomæner forudsat en fællesoffenlig standardisering af digitaliserede samtykker.

#### Udfordringer omkring fuldmagt

Den eksisterende fællesoffentlige NemLog-in fuldmagtsløsning er rettet mod fuldmagt til specifikke selvbetjeningsløsninger inden for individuelle myndighedersområder. Her er afgrænsningen den enkelte løsning. For et tværgående digitalt overblik vil det imidlertid være tale om læseadgang/fuldmagt til data fra flere kilder/myndigheder. Her skal afgrænsningen være for det eller de relevante sæt data.

På sigt vil der være behov for, at fuldmagtsløsningen kan danne en fuldmagt, der giver læseadgang til flere løsninger og med en specificering af dataafgrænsning på baggrund af de standardiserede datamodeller for overbliksdata. Løsningen skal via et token kunne anvendes i tjenesterne i alle de fire lag i målarkitekturen.

### Andre påkrævede formelle aftaler.

Det skal sikres, at der i det driftsmæssige setup er aftaler på SLA og support for alle parter, der implementerer byggeblokke i de forskellige lag i arkitekturen. Dette gælder særligt krav til svartider, skalérbarhed og robusthed med henblik på at sikre en god performance i visningsklienter. Hertil kommer naturligvis krav til sikkerhed og tilgængelighed.

## 4\. Sikkerhed

Dette kapitel beskriver relevante og væsentlige sikkerhedsmæssige problemstillinger, der gælder specifikt i forhold til overblik.

### Sikkerhedsstrategi / -mønstre

Sikkerhedsstrategien for overblik er baseret på, at data til visning i brugergrænsefladen/præsentationen leveres af et orkestreringslag, men at data ikke lagres i dette jf. princip 9.

Sikkerhedsmodellen opstilles med udgangspunkt i et trusselsbillede for overblik, og referencearkitekturen forholder sig aktivt til ISO 27001[\[16\]](#Fodnote 16)og ISO 27005 ved, at der nedenfor opstilles en risikovurdering for udvalgte trusler, som kræver særlig opmærksomhed i forhold til sikkerhedsmodellen.

Sikkerhedsmodellen beskriver sikkerhed for hvert lag i arkitekturen.

### Trussels- og risikokatalog

 ISO 27000 opdeler trusler mod informationssikkerhed i følgende grupperinger:

| ISO 27000 trusselgruppering                                                                                                 | Særlig relevans                     |
| --------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| 1\. Mennesker<br><br>1.1 Medarbejdere<br><br>1.2 Samarbejdspartnere<br><br>1.3 Hackere, hacktivister eller andre kriminelle | Se nedenstående trusselsbilllede    |
| 2\. Naturkatastrofer                                                                                                        | Ingen særlige trusler identificeret |
| 3\. Ulykker                                                                                                                 | Ingen særlige trusler identificeret |
| 4\. Nedbrud og tekniske fejl                                                                                                | Ingen særlige trusler identificeret |

Overblik viser data om borgere og virksomheder indsamlet fra flere myndigheder og datakilder. For denne samling af data peger referencearkitekturen på følgende trusler, som kræver særlig opmærksomhed. Hver trussel har en tilhørende FIT-vurdering[\[17\]](#Fodnote 17) (fortrolighed, integritet, tilgængelighed), der danner grundlaget for den beskrevne sikkerhedsmodel.

| Trussel                                                                                 | Fortrolighed | Integritet | Tilgængelighed |
| --------------------------------------------------------------------------------------- | ------------ | ---------- | -------------- |
| 1.1 Medarbejdere                                                                        |              |            |                |
| Uautoriseret brug, misbrug af rettigheder                                               | X            | X          | X              |
| Tilsigtet informationslæk                                                               | X            |            |                |
| For vidtgående brugerrettigheder/adgangsprivilegier                                     | X            | X          | X              |
| Fejlagtig publicering af data, der indeholder fortrolige oplysninger                    | X            |            |                |
| 1.2 Samarbejdspartnere                                                                  |              |            |                |
| Leverandørrelaterede trusler - ondsindede medarbejdere, udnyttelse af privilegier (Lev) | X            | X          | X              |
| 1.3 Hackere, hacktivister eller andre kriminelle                                        |              |            |                |
| Cyberangreb - DDoS-angreb                                                               |              |            | X              |
| Cyberangreb – Phishing                                                                  | X            |            | X              |
| Cyberangreb - Statsfinansierede angreb (State-sponsored attacks = APT)                  | X            |            | X              |
| Cyberangreb - Forfalskning af informationer, ødelæggelse af websites                    | X            | X          | X              |

Trusselsbilledet afleder 2 fokusområder for sikkerhedsmodellen:

1. Sikring af orkestreringslaget og adgang til services som udstilles
2. Brugerrettigheder for hvem der har adgang til hvilke data i et overblik.

### Sikkerhedsmodel

Den overordnede sikkerhedsmodel for overblik er:

* Sikkerheden følger data, dvs. der skal være samme sikkerhed for data, uanset hvor data på et givet tidspunkt befinder sig/vises.
* Den grundlæggende rolle Dataanvender[\[18\]](#Fodnote 18) er i forhold til overblik relateret til to aktører (Borgeren har samtidig har rollen den registrerede, jf GDPR): Borger og Virksomhed. Disse to aktører skal kunne delegere adgang til overbliksdata via læseadgang. Borger skal kunne delegere læseadgang til en stedfortræder som fx en pårørende eller rådgiver. Virksomheden skal kunne delegere læseadgang til medarbejdere og stedfortrædere som fx en revisor eller DPO. Det er vigtigt, at forskellige aktører kan have forskellig autorisation i forhold til hvilke data, der vises i overblik fx forældre, børn, værge på borgerområdet og ift. virksomheder, ejer, medarbejder, rådgiver osv.
* Vedrørende GDPR og data, der vises i overblik, er borgeren både den Registrerede og Dataanvender. Ved forældremyndighed og værgemål ligger der en implict hjemmel til at se data for en anden Registreret. Det er her vigtigt at bemærke, at data om borgeren ikke er registreret i overblik, men alene i fagsystem og eller domæneindeks.
* Aftalemæssige forhold er en integreret del af sikkerheden, så Dataanvender kun har adgang til data, hvor der foreligger en databehandleraftale.
* Adgangsbillet for Anvender videregives til alle lag i arkitekturen, således at den er tilgængelig for datakilden, hvis datakilden ønsker at filtrere data i forhold til adgangsbilletten (anvenderen) fx rådgiver for en virksomhed.

Ved implementering af sikkerhedsmodellen i forhold til rettigheder henvises til Referencearkitektur for brugerstyring med særlig fokus på følgende begreber[\[19\]](#Fodnote 19):

* Bruger med tilhørende identifikation (akkreditiv) 
* Adgangsbillet der beskriver brugerrolle og tilhørende adgangsrettigheder (Engelsk Security token).
* Adgangskontrol baseret på en adgangspolitik jf. indgåede databehandleraftaler.

#### Sikring af orkestreringslaget omfatter:

* Udveksling af data mellem de forskellig lag i arkitekturen skal ske krypteret, når der er tale om eksterne snitflader, og udveksling mellem Orkestrering og brugergrænsefladen skal i givet fald ske med stærk kryptering.
* Adgangspolitik opsættes for hvem, der må tilgå services udstillet af orkestreringslaget, således at det kun er anvendere med tilladte akkreditiver, der har adgang.
* Adgangspolitik skal sikre, at der er indgået databehandleraftale med databehandler (aktører ansvarlige for tjenester i præsentationslag og orkestreringslag), og der er en kobling til akkreditiver, dvs., at der er defineret en tilhørende adgangspolitik for databehandleraftalen.
* Der anvendes bedste praksis for sikring af, at databehandler - fx. borger.dk-portalen - kan identificeres og akkreditiv kan valideres, fx certifikat.

#### Brugerrettigheder for hvem der har adgang til hvilke data

Adgangspolitikker for adgang til data i orkestreringslaget indlægges på datakildeniveau, dvs., orkestreringslaget sikrer, at data alene hentes fra datakilder, hvor der foreligger en databehandleraftale mellem datakilden og præsentationen/brugergrænsefladen.

Adgang til data på attributniveau sikres af datakilden gennem egne adgangspolitikker og på baggrund af den aktuelle adgangsbillet. Alle domæneindeks og datakilder skal implementere adgangskontrollen i forhold til data.

#### Brugervalidering og udveksling af adgangsbillet

Ansvar for validering af brugerens akkreditiver og sikring af, at brugeren har en valid session, er placeret i præsentationslaget. Præsentationslaget har også ansvar for, at der for hver bruger er udstedt en gyldig adgangsbillet, der udveksles mellem lagene. Ud fra forretningsmæssige behov og behov afledt af en risikovurdering kan de enkelte lag anvende adgangsbilletten til at validere brugeridentiteten eller til validering af, at den aktuelle bruger har tilstrækkelige rettigheder til at få vist data.

Der etableres trust mellem præsentationslaget og de øvrige lag, hvor de aktuelle lag er afhængig af implementeringsscenariet for det specifikke overblik. Dette kan fx understøttes ved anvendelse af FOCES-certifikater og kan suppleres med applikationsnøgler, der udveksles og valideres på de enkelte snitflader i arkitekturen.

## 5\. Opgaver

Afsnittet indeholder beskrivelse af de forretningskapabiliteter, referencearkitekturen peger på for at realisere visionen og det opstillede målbillede. Det forretningsmæssige målbillede i afsnittet om _målarkitektur (to-be situation – resumé)_ præsenterer en række tjenester, som uddybes og specificeres nærmere i nærværende afsnit.

![Figur 5.1.png](assets/Figur%205.1.png)

Figur 5.1 Forretningsmæssige tjenester og kapabiliteter

De to aktører, der er de centrale brugere, er _Borger_ og _Virksomhed_. Disse to aktører skal kunne delegere adgang til overbliksdata via læseadgang. Borger skal kunne delegere til fx en stedfortræder som fx pårørende eller rådgiver. Virksomheden skal kunne delegere til medarbejdere og stedfortrædere som fx en revisor. Se yderligere afsnittet Aktører og roller nedenfor.

### Præsentation

Præsentation er visning af overblik på den af brugeren valgte kanal. Hvor det for borger-aktøren typisk vil være borger.dk, og for virksomhedsaktøren vil være Virk. Som det fremgår af figuren, kan der være andre visninger af overbliksdata fx en kommunal portal, en hjemmeside med en selvbetjeningsløsning eller en mobil-app.

Jura-perspektivet omfatter konfigurationslogning for hvert lag i arkitekturen, hvorfor præsentationsslaget rummer kapabiliteten visningslogning til at understøtte dette.

### Orkestrering

Orkestrering samler de kapabiliteter og tjenester, der anvendes til at sammenstille og udstille overblik til brug for brugerflader, der viser overblik for anvendere, dvs. borgere og virksomheder.

#### Overblik

Den centrale forretningskapabilitet er Overblik, som gennem funktionalitet i Orkestreringslaget samt anvendelse af tjenester i integrationslaget indsamler, danner og udstiller overbliksdata. Kapabiliteten Overblik kan nedbrydes i to overblikstjenester:

* **Overbliksliste**: Udstiller en samling af data på tværs af emner – dvs. få centrale informationer for alle eller et bredt udsnit af fx sager, ydelser, frister eller andre data, der vises i overblik.
* **Overbliksdetaljer**: Udstiller detaljer for en eller flere udvalgte dataobjekter fx en specifik sag eller ydelse.

Disse to tjenester er helt konceptuelle og generiske og vil i praksis kunne implementeres på mange måder og i mange blandingsformer. Det forventes, at der over tid vil blive samlet erfaringer med de mest hensigtsmæssige metoder og design af tjenester til overblik.

Tjenesterne _Overbliksliste_ og _Overbliksdetaljer_ specialiseres for de enkelte datadomæner, der indgår i et overblik - fx Sagsliste og Sagsdetaljer. I afsnit for Informationsperspektivet er beskrevet hvilke datadomæner, der er relevante i forhold til overblikstjenesterne.

Som beskrevet i Jura-perspektivet er der et forretningsmæssigt behov for at styre, at overblikslister eller overbliksdetaljer kun vises på brugergrænseflader, hvor der foreligger en databehandleraftale. Denne kapabilitet er obligatorisk for alle brugergrænseflader, der anvender orkestreringslagets tjenester, og bør arkitekturmæssigt ligge så tæt på brugergrænsefladen som muligt, hvorfor denne kapabilitet indplaceres i Orkestreringslaget.

Jura-perspektivet omfatter konfigurationslogning for hvert lag i arkitekturen, hvorfor orkestreringslaget rummer en kapabilitet – Orkestreringslogning - til at understøtte dette.

### Integration

I Integrationslaget findes de nødvendige funktioner for, at data fra datakilderne kan samles og eventuelt transformeres til brug for præsentation i et brugervendt overblik.

**Transformation.** Data fra kildesystemer skal om nødvendigt transformeres fra kildesystemernes datamodel til den fælles brugervendte datamodel for det givne datadomæne, således at data kan sammenstilles af orkestreringslaget og præsenteres i et samlet overblik for borgere og virksomheder.

**Regelhåndtering.** Kobling mellem brugerrettede data i et overblik og data i kildesystemerne kræver opsætning af forretningsregler i forbindelse med dataafgrænsning og mapning mellem begreber og mapning mellem forvaltningsmæssige klassifikationer og de fælles brugervendte klassifikationer fx for sagsstatus. Regelhåndtering omfatter opsætning af forretningsregler til anvendelse af transformation og fremsøgning af relevante overblik for brugeren samt rækkefølge (fx ”Hvilken sag skal vises først?”) og evt. begrænsninger for data (fx ”Er der sager eller sagsdetaljer, der ikke må vises til den pågældende bruger?”).

Ejerskab for og vedligeholdelse af forretningsregler ligger altid hos den enkelte myndighed og anvendes altid i kontekst af denne myndigheds data. Arkitekturmæssigt placeres regelhåndtering derfor så tæt på datakilden som muligt for at sikre et utvetydigt ejerskab.

**Klassifikationshåndtering.** Klassifikationer og mapninger mellem forskellige alternative klassifikationer er en central del af transformationen fra data lagret i myndighedernes kildesystemer til data, der præsenteres i et overblik. Klassifikationer bidrager i stort omfang til fælles forståelsesramme på tværs af data og til en for brugeren opfattet ensartethed i data, der indgår i overbliksvisningen.

For at understøtte funktionalitet på selve brugergrænsefladen for overblik opmærkes data efter samme klassifikation, således at gruppering, sortering og ensartet håndtering af hjælpetekst samt henvisning og tool-tips er muligt at implementere for alle data i brugergrænsefladen uanset datakilden. Et eksempel på en sådan anvendelse er mapning fra en myndighedsvendt sagsstatusklassifikation til en fælles klassifikation tilpasset den brugervendte overbliksvisning.

**Konteksthåndtering.** Overblik skal kunne filtreres og vises for brugerne i en kontekst, der er forståelig og giver mening for dem. Konteksthåndtering sikrer også filtrering i forhold til, hvilken rolle brugeren har for det givne overblik. Dette er især relevant for virksomhedsoverblik, hvor forskellige virksomhedsroller skal kunne se forskellige udsnit af data i overblikket. Det forudsætter viden om, hvilken kontekst brugeren er i, og hvilken rolle brugeren har i konteksten.

**Integrationslogning.** Jura-perspektivet omfatter konfigurationslogning for hvert lag i arkitekturen, hvorfor integrationslaget rummer kapabiliteten Integrationslogning til at understøtte dette.

Integrationslaget omfatter to forretningstjenester, **Videregivelse-overbliksdata** og **Indeks**. Videregivelse-overbliksdata er tjenesten, som orkestreringslaget anvender til at hente data, der skal sammenstilles til et overblik. Tjenesten udstiller data, der er i overensstemmelse med den fælles datamodel og de fastlagte klassifikationer (se nedenstående beskrivelse om klassifikationer).

Indeks er forretningstjenesten, der giver orkestreringslaget mulighed for at forespørge, om der er relevante data i et datadomæne eller en datakilde for den aktuelle bruger. Indeks -også benævnt domæneindeks - anvendes til at optimere et overblik, ved at der kun forsøges fremsøgning af data fra datakilder og datadomæner, der har relevante data, eller ved at Indeks opbevarer en kopi af data for hurtig fremsøgning. Indeks omfatter også grundfunktionalitet til at vedligeholde indeks-information, dvs., datakilder kan opdatere data i indeks. Data i et indeks kan fx være overbliksdata eller binære data, der for en specifik nøgle angiver, om en datakilde har relevante data. Eksempel på relevante nøgler er CVR-nr og CPR-nummer eller anden unik identifikation på den aktuelle bruger. Det er vigtigt, at de nøgler, der besluttes anvendt, er tværgående og entydige nøgler, da nøglen dels skal kunne videregives fra brugergrænsefladen dels skal være kendt af datakilderne.

### Datakilder og grundlæggende tjenester

Data til overblikket udstilles fra Datakilder og grundlæggende tjenester, som udgøres af myndighedernes kildesystemer og referencedatatjenester. Kildesystemer kan også være eksisterende domæneindekser, som kan anvendes på vegne af kildesystemerne, fx kan de fælleskommunale støttesystemer ses som en datakilde, der leverer kommunale data på vegne af kommunernes ydelsessystem m.fl. Sådanne opkoblingspunkter på statsligt, kommunalt og regionalt niveau kan mindske kompleksiteten af it-landskabet og indeholder optimerede kopier af data, som udstilles på vegne af en række bagvedliggende fagsystemer.

Referencearkitekturen foreskriver, at datakilder udstiller en forretningstjeneste, **Fremsøg overbliksdata**, der fremsøger og returnerer relevante data fra fag- eller sags-systemet. Det er datakildens forretningsmæssige ansvar, at det er relevante data, der fremsøges, og at der kun returneres data, som den givne bruger må få vist (se sikkerhedsmodel for detaljer).

Jura-perspektivet omfatter konfigurationslogning for hvert lag i arkitekturen, hvorfor datakildelaget rummer kapabiliteten **Datakildelogning** til at understøtte dette.

### Kataloger

Kataloger i denne referencearkitektur er et udvalg af kataloger, der vurderes som særligt vigtige ift referencearkitekturens model for dannelse, berigelse, transformation, orkestrering og visning af overbliksdata, som er beskrevet nærmere i kapitel 6: Information.

Disse kataloger omfatter kataloger for datasæt, selvbetjeningsløsninger, informationssider, datamodeller, tekniske specifikationer og profiler samt klassifikationer. Disse kataloger er støttetjenester - især til kapabiliteter i integrationslaget. Katalogerne uddybes i kapitel 6: Information og Bilag D: Kataloger.

#### Realisering af kataloger

Katalogerne kan i praksis realiseres meget lavpraktisk som analoge løsninger eller mere avancerede tekniske løsninger.

Det anbefales dog, at klassifikation-tjenesten realiseres som en fællesoffentlig service, der udstiller klassifikationer generelt. Klassifikation er en tjeneste, der udstiller de klassifikationer, der anvendes til at klassificere data og ved transformation af data. Klassifikation ses om en generisk tjeneste, der også understøtter de særlige klassifikationer, som er nødvendige for at fremsøge, transformere, sammenstille og vise data i et overblik. Klassifikation-tjenesten er i arkitekturen en vigtig tjeneste, da den er grundlaget for at sikre, at de rigtige klassifikationer er tilgængelige for alle datakilder og integrations og orkestrerings-funktionaliteten. Et andet vigtigt aspekt, som tjenesten understøtter, er, at det er samme version af en given klassifikation, der anvendes på tværs. Realiseringen af den faktiske klassifikationstjeneste er uden for scope af referencearkitekturen.

### Brugerstyring

Forretningstjenesterne under brugerstyring er støttetjenester til håndtering af Identiteter herunder autentifikation og validering af identiteter som beskrevet i referencearkitektur for brugerstyring samt udstedelse og validering af Adgangsbilletter. Endvidere er der forretningstjenester til udstedelse og validering af elektroniske fuldmagt, således at aktører kan delegere til andre aktører.

### Aktører og roller

I denne referencearkitektur defineres ingen nye aktører eller forretningsroller. Der indgår en række aktører, der er defineret i andre referencearkitekturer eller standarder. Det samme er gældende for de roller, der kan tilknyttes til aktørerne.

Aktører, der indgår referencearkitekturen, er:

* Borger er jf. EIRA (Citizen) “A person who is a member of a particular country and who has rights because of being born there or because of being given rights, or a person who lives in a particular town or city.” Borger ses om en specialisering af Person, der er defineret i grunddatamodellen Person
* Virksomhed er en juridisk enhed registreret i CVR-registret med CVR-nummer og defineret i grunddatamodellen Virksomhed. Virksomhed er en specialisering af Organisation - en Organisation[\[20\]](#Fodnote 20) er en juridisk enhed med rettigheder og ansvar. Eksempler på organisationer er myndigheder (fx et ministerium, en styrelse, en kommune) eller virksomheder.
* Offentlig myndighed er en specialisering af Organisation og er en organisation inden for stat, region eller kommune.

I forhold til overblik og referencearkitekturens scope kan aktørerne have følgende roller. Hvilke specifikke roller, den enkelte aktør kan have tilknyttet, er illustreret i nedenstående aktør/rolle-model.

![Figur 5.2.png](assets/Figur%205.2.png)

Figur 5.2 - Relation mellem aktører og roller

* Den registrerede - den person (datasubjekt) som oplysninger vedrører. Defineret i Databeskyttelsesforordningen.
* Dataanvender \- en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der med specifik hjemmel behandler data fra en datasamling til eget formål. Defineret i Referencearkitektur for deling af data og dokumenter.
* _Stedfortræder_ \- en fysisk eller juridisk person, der som 3. part varetager opgaver på vegne af en anden.
* Ejer er den eller de personer eller juridiske enheder, der er registreret i CVR som ejer af en virksomhed. Grunddatamodellen Virksomhed.
* Medarbejder er en person, som modtager vederlag for personligt arbejde i et tjenesteforhold for en virksomhed, dvs. ansat i virksomheden[\[21\]](#Fodnote 21).
* Dataansvarlig \- en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der alene eller sammen med andre afgør til hvilke formål og med hvilke hjælpemidler, der må foretages behandling af personoplysninger (rolle fra GDPR).

Rollerne: Ejer, Medarbejder og Stedfortræder er vigtige roller i forhold til at afgrænse hvilke data, der skal vises på virksomhedsområdet. Disse roller er derfor centrale for sikkerhedsmodellen og virkemåden af dataafgrænsning og filtrering.

### Processer

I dette afsnit vises et eksempel på en typisk anvendelsessituation for overblik, herunder hvordan procestrin anvender tjenester og funktioner i det forretningsmæssige målbillede. Eksemplet forholder sig ikke til, hvordan overblikket implementeres i fx fællesoffentlige portaler, dedikerede apps eller på myndighedens hjemmeside. Bemærk at der kan være flere datakilder, der leverer data, men at der i figuren kun fremgår én datakilde.

#### Bruger tilgår overblik

”Brugeren tilgår overblik” viser, hvorledes processen for en brugers anvendelse af overblik kan foregå. Processen viser et sagsoverblik, men samme forløb vil være gældende for andre datadomæner fx aftaler. Figuren og beskrivelsen forholder sig ikke til anvendelse af integrationsmønstre for kald af tjenester og levering af data, samt hvorledes en visning vil ske på brugergrænsefladen. Anvendelse af integrationsmønstre er beskrevet under applikationsperspektivet.

![Figur 5.3.png](assets/Figur%205.3.png)

Figur 5.3 - Bruger tilgår overblik

Brugeren vil efter login være kendt i brugergrænsefladen, og processen starter med at brugeren vælger, hvor en _bruger tilgår overblik_.

| Aktivitet                                                                         | Forklaring                                                                                                                                                                                                                   |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bruger vælger overblik for sager                                                  | Bruger er logget ind på brugergrænseflade, der udstiller overblik, og brugeren vælger sagsoverblik af de overbliksmuligheder, der tilbydes.                                                                                  |
| Indsamling af kontekst med efterfølgende kald til Overbliksliste                  | Brugergrænsefladen indsamler kontekstinformation, som skal anvendes ved fremsøgning og levering af sagsoverbliksdata.<br><br>Brugergrænsefladen kalder tjenesten Overbliksliste i orkestreringslaget.                        |
| Valider aftaler og kald<br><br>Videregivelse af overbliksdata i integrationslaget | Det valideres, at der er valide databehandleraftaler for de overbliksdata, der forespørges på.<br><br>Herefter kaldes tjenesten Videregivelse af overbliksdata.                                                              |
| Fremsøg overbliksdata                                                             | Datakilden fremsøger de forespurgte data i forhold til den kontekst, der forespørges ud fra, og data filtreres evt.                                                                                                          |
| Transformation og Klassifikationshåndtering                                       | De fremsøgte data modtages i integrationslaget og transformeres til fælles datamodel og klassificeres i forhold til fællesoffentlige klassifikationer og de specifikke klassifikationer gældende for overblik fx sagsstatus. |
| Levering af overblikdata                                                          | Data med rette klassifikation og i henhold til fælles datamodel leveres til orkestreringslaget i forhold til aftalt format og teknologi.                                                                                     |
| Sammenstil modtagne data                                                          | Orkestreringslaget sammenstiller modtagne data til et samlet svar til brugergrænsefladen.                                                                                                                                    |
| Vis sagsliste for brugeren                                                        | Brugergrænsefladen præsenterer de modtagne data, og brugeren kan se sagsoverblikket.                                                                                                                                         |

## 6\. Information

### Forretningsobjekter

Forretningsmæssige data - repræsenteret ved kerneforretningsobjekter - bliver udfoldet i selvstændige datamodeller, der udvikles i henhold til standardiseret proces jf. nedenstående. Kerneforretningsobjekter er eksemplevis Sag, Ydelse og Aftale.

### Data og information – indsamling og visning

Referencearkitekturen omfatter i sig selv meget begrænset information, da arkitekturens scope er flowet fra datakilder til brugergrænsefladen. I overblik indgår forskellige typer af data, hvilket er illustreret i nedenstående konceptuelle model.

![Figur 6.1.png](assets/Figur%206.1.png)

Figur 6.1 Konceptuel model for data der indgår i overblik

Referencearkitekturen omfatter følgende former af data:

* Overbliksdata - Fagdata der er udvalgt til visning i overblik.
* Klassifikationer - Er fællesoffentlige klassifikationer fx FORM samt klassifikationer, der oversætter koder og fagspecifikke værdier til standardiserede betegnelser og forklaringer. Defineres i forhold til den enkelte datamodel med hensyntagen til anvendelse og visning.
* Kontekstspecifikke metadata – metadata der forklarer specifikke forhold vedrørende overbliksdata fx ansvarlig myndighed og kontaktoplysninger fx ledetekster. Det kan også være Påmindelser. Visning af påmindelser kan fx ske ud fra en bestemt opmærkning af data som ”påmindelsesegnet” foretaget af datakilden eller på baggrund af simple regler opsat for specifikke attributter fx status på en sag eller en dato på en frist.
* Redaktionelle data – er redaktionelle data, der vedligeholdes og leveres af datakilden sammen med fagdata som en del af overbliksdata, således at de kan vises i overbliksvisningen.
* Referencedata - er referencedata og grunddata, der relaterer sig til overbliksdata og er en del af visningen. Fx navn og adresse på en borger hentet i CPR-registret.
* Omsluttende redaktionelle data - er redaktionelle data, der vises i brugergrænseflade - fx overskrifter og hjælpetekster -, og som er specifikke for den aktuelle brugergrænseflade.
* Overbliksliste - er få udvalgte overbliksdata i listeform fx liste over sager.
* Overbliksdetaljer - er detaljer for det enkelte objekt, der fremgår af overblikslisten, fx detaljer for en specifik sag.

Referencearkitekturen er anvendelig for et bredt spektrum af data og fra forskellige datadomæner. Næste kapitel om information indeholder derfor en beskrivelse af processen for udarbejdelse af de udstillingsmodeller, som data i overblik skal overholde, samt de klassifikationer data skal klassificeres efter. Dette dokument indeholder derimod ikke egentlige begrebs- og informationsmodeller for de enkelte datadomæner, idet disse skal udarbejdes som selvstændige specifikationer.

### Standardisering af data

For data opstiller referencearkitekturen den præmis, at den er gældende for data, der er standardiserbare i forhold til overbliksvisningen. At data er standardiserbare betyder, at en række kriterier er opfyldt, og at data leveret fra datakilder kan transformeres til en fælles udstillingsdatamodel gældende for overblik.

#### Kriterier for standardisering

Referencearkitekturen opstiller følgende sæt af kriterier, der specificerer grundlaget for at vurdere, om data i et givent datadomæne er kandidat til standardisering:

* Data, der vises i overblik, er persisteret i forskellige systemer.
* Data skal kunne leveres fra flere datakilder.
* Data fra flere datakilder er egnet til sammenstilling på brugergrænsefladen
* Data skal kunne vises i forskellige overblik, dvs. på forskellige brugergrænseflader, enheder eller kanaler.

Et supplerende kriterie kan være udsigten til at gennemføre en fornuftig standardiseringsproces, fx ud fra om data er helt eller delvist specificeret i en eksisterende kernemodel. Ligeledes kan der være hensyn til eksisterende internationale standarder eller pågående standardiseringsarbejde i internationalt regi.

Standardiserede datamodeller kan fx indeholde felter med persondata, felter med kontekstrelateret information fx om forklaringer, vejledning, kontaktpunkter og links til selvbetjening, der udfyldes af den enkelte myndighed samt metadata, der udfyldes ved brug af fælles klassifikationer som fx emneklassifikation, taksonomi for sagsstatus og kontrollerede udfaldsrum for ledetekster.

#### Proces for udarbejdelse af fællesoffentlig udstillingsdatamodel (fælles datamodel)

Data, der skal vises i overblik og som lever op til kriterierne for standardisering i forbindelse med tværgående digitalt overblik, går på tværs af myndigheder og dataansvarlige, hvorfor den fælles udstillingsmodel skal opfylde krav fra en række interessenter og ressortområder.

Referencearkitekturen beskriver en generisk proces for, hvordan fælles udstillingsmodeller kan udarbejdes, da antallet og omfanget af udstillingsmodeller varierer over tid. Dels er det forskellige overblik, der tilbydes, dels ændres de enkelte overblik. Scope er modeller, der skal gå på tværs af domæner, mens modeller, der kun skal gælde for et afgrænset domæne, er uden for scope.

Processen tager udgangspunkt i, at der er etableret et grundlag gennem udarbejdelse af mock-up, brugerinterviews og andre aktiviteter, der afdækker hvilke data, der er relevante at vise i et overblik for det pågældende datadomæne og for den forretningsmæssige scoping, der er besluttet. Slutproduktet ved gennemførelse af processen er en fælles udstillingsmodel samt beskrivelse af indholdet af tjenesterne Overbliksliste og Overbliksdetaljer.

Den fulde proces med angivelse af grundlag/input er illustreret i nedenstående figur. Erfaringer fra ADDA-projektet viser klart, at processen skal gennemføres iterativt, og løbende afprøvninger af visning af data på en brugergrænseflade giver stor indsigt i, hvilke data, hjælpedata og metadata der for det enkelte overblik er relevante og giver værdi for brugeren. Dette kan fx være hvor mange og hvilke overbliksdetaljeringsniveauer, der giver mening, hvor dette ikke nødvendigvis er ens for alle myndigheder og datakilder. Det vil bero på en konkret forretningsmæssig vurdering ud fra brugerbehov og muligheder.

![Figur 6.2.png](assets/Figur%206.2.png)

Figur 6.2 - Proces for udarbejdelse af fælles udstillingsmodel

Da de fælles datamodeller, der udarbejdes i projekter jf. ovenstående proces, er et særdeles vigtigt element i og en forudsætning for implementering af digitale overblik, bør der etableres en stærk styring og vedligeholdelse af datamodellerne.

Referencearkitekturen peger på følgende styrings- og vedligeholdelsessetup:

* Ejerskab af fælles datamodeller forankres et sted. Digitaliseringsstyrelsen vil være kandidat til forankring af ejerskab for modeller, der går på tværs af flere domæner, men forankring kan også ske hos andre relevante aktører.
* Datamodeller indlægges og samles i et fælles modelleringsværktøj og repositorie, der vedligeholdes af Digitaliseringsstyrelsen.
* Der udpeges en modelredaktør for den enkelte datamodel, der er ansvarlig for og udførende på den løbende forvaltning af datamodeller og tilhørende klassifikationer og sikrer, at gældende versioner af datamodeller er tilgængelige for anvendere.

![Figur 6.3.png](assets/Figur%206.3.png)

Figur 6.3 - Styring og vedligeholdelse af modeller

Som beskrevet i kapitel ?Opgaver, bør det være muligt at opmærke data, således at brugergrænsefladen kan vise en notifikation[\[22\]](#Fodnote 22) for brugeren. De udviklede datamodeller til overbliksdata skal understøtte denne mulighed for opmærkning.

### Klassifikationer

Som en integreret del af arbejdet med fælles udstillingsmodeller skal der udarbejdes klassifikationer til anvendelse af visning af overbliksdata. Disse klassifikationer tager udgangspunkt i datakildernes anvendte klassifikationer, de fælles offentlige klassifikationer og krav fra brugergrænsefladen fx til sortering/filtrering.

Afhængigheder og påvirkninger for overbliks-klassifikationer er:

* Delmængde af datakilders klassifikationer vil ofte indgå i overbliks-klassifikationen, og mapningen til datakilders klassifikationer skal være entydig, fx vil overbliksklassifikation for sagsstatus være en delmængde af datakildernes klassifikationer.
* Delmængde af fællesoffentlige klassifikationer vil ofte indgå i overbliks-klassifikationen, og der skal være sporbarhed mellem disse. Findes der en fællesoffentlig klassifikation for data-domænet, anvendes denne som udgangspunkt.
* Brugergrænsefladers behov skal afspejles i hvilke klassifikationer, der er behov for og indholdet af disse - herunder input fra mock-ups. Fx behov for filtrering kan aflede yderligere klassifikation af data.

### Kataloger

Kataloger er en forretningsmæssig kapabilitet, der anvendes i overblik. De kataloger, der er relevante for de forskellige lag i arkitekturen, beskrives kort i nedenstående tabel og er beskrevet mere detaljeret i Bilag D: Kataloger.

| Katalog                                                                                                   | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Anvendere                                                                                                                                                                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Selvbetjenings-løsninger                                                                                  | Kataloget indeholder relevante selvbetjeningsløsninger, der tilbydes af offentlige myndigheder.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Datakilder: til konfiguration/udfyldelse af attributter i entiteter i datamodel for anvendelsesprofilen for det givne datadomæne.                                                                                                                                                                                                                                             |
| Datasætkatalog                                                                                            | Katalog over hvilke datasæt/datakilder der findes for de forskellige datadomæner, der er inkluderet i overblik eller er kandidat til at levere data til overblik.<br><br>Kataloget indeholder også information om end-point, der udstilles af datakilden.                                                                                                                                                                                                                                                                                                                                         | Forvalter af orkestrering (fx Orkestreringskomponent) hvor information fra kataloget skal anvendes til konfiguration af orkestreringen.<br><br>Forvaltere af overbliks-løsninger og portal/app administratorer har behov for at vide hvilke data, der kan fremsøges, hvem der er dataansvarlige, samt hvad der skal gøres for at etablere de nødvendige databehandleraftaler. |
| Katalog over fælles klassifikationer og udfaldsrum                                                        | Er et katalog, der giver en samlet oversigt over de klassifikationer, kontrollerede udfaldsrum i form af ledetekster og lignende, der er defineret til anvendelse i elementer i overblik i forbindelse med udarbejdelse af fælles datamodeller.<br><br>Katalogfunktionen er flad, men bagvedliggende funktion kan have større funktionalitet fx til understøttelse af relationer mellem klassifikationer.<br><br>Katalog, der også er repositorie og dermed indeholder selve klassifikationen, kan udstille to services: Fuldt download hhv. web service fx baseret på nøgleord eller referencer. | Kataloget anvendes af datakilder og integrationslaget til at finde den nyeste klassifikation og anvende denne i forbindelse med opmærkning og evt. transformation af data, der leveres af datakilder til overblik.<br><br>Kataloget anvendes desuden af visningsportaler, App o.l. til konfiguration af søgning og præsentation, fx ifbm emnestrukturering.                   |
| Katalog over informationssider                                                                            | Katalog over informations-og vejledningssider.<br><br>Fx opmærket efter FORM/KLE.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Anvendes af datakilder til at indsætte link til information og vejledninger, der kan give brugere af overblik mere uddybende information om betydning af data, der vises i overblik.<br><br>Anvendes af præsentationslaget/vis-ningsklienter til give brugere generel baggrundsinformation om opgaveområde, der vises data for i overblik.                                    |
| Datamodel-katalog                                                                                         | Katalog over fælles datamodeller for overblik.<br><br>Kataloget indeholder kort beskrivelse af modellen, og link til hvor den specifikke model og tilhørende skemaer kan findes. Modeller er i formaliseret modelsprog fx UML.<br><br>Evt. behov for interaktiv funktionalitet til opslag/fremsøgning af enkeltelementer samt fx mulighed for at kommentere eller fremsætte ændringsønsker.                                                                                                                                                                                                       | Anvendes af myndigheder og deres it-leverandører, når integration til orkestreringen skal implementeres. Det omfatter både datakilder og præsentationsløsninger.                                                                                                                                                                                                              |
| Katalog over specifikationer og lign. der skal anvendes til implementering snitflader og transformationer | Behov for stabilt sted hvor relevant arkitektur og tekniske specifikationer som fx anvendelsesprofiler lagres. Ikke UML-model, men tekniske specifikationer.                                                                                                                                                                                                                                                                                                                                                                                                                                      | Anvendes af it-leverandører/udviklere, der skal implementere services/snitflader, der udstiller data til overblik samt anvendere af de udstillede services fx visningsklienter.                                                                                                                                                                                               |

## 7\. Applikation

Dette kapitel beskriver det systemtekniske målbillede med de vigtigste tekniske arkitekturbyggeblokke og deres vigtigste indbyrdes interaktioner og beskriver i den sammenhæng relevante integrationsmønstre. Referencearkitekturen beskriver ikke realiseringen eller peger på konkrete produkter eller it-løsninger. Dette sker i løsningsarkitekturen for de konkrete byggeblokke.

Applikationsperspektivet beskrives i forhold til de fire lag, som referencearkitekturen specificer for overblik. I beskrivelsen af de enkelte lag fokuseres der på tjenester og funktioner. I det efterfølgende afsnit om implementeringsscenarier beskrives mulige kombinationer af tjenester og funktioner til komponenter.

### Præsentation

For applikationsbyggeblokke og komponenter i dette lag henvises til Referencearkitektur for selvbetjening, hvor disse er uddybende beskrevet.

I forhold til overblik er det vigtigt at fremhæve, at præsentationen er ansvarlig for bruger-autentifikation, hvorved det er brugergrænsefladen, brugeren har en session med. Se afsnit Sikkerhedsmodel i ovenstående for uddybende beskrivelse af brugervalidering og sessionshåndtering.

### Orkestrering

De vigtigste applikationsbyggeblokke for Orkestreringslaget er gengivet i nedenstående figur, hvor relation til brugergrænsefladen og brugerstyring (sikkerhed) også er medtaget.

På figuren fremgår også to applikationsbyggeblokke, Indeks-opdatering og Binært-indeks. Disse to byggeblokke kan placeres på både orkestreringslaget og integrationslaget, men er beskrivelsesmæssigt medtaget her.

![Figur 7.1.png](assets/Figur%207.1.png)

Figur 7.1 - Orkestrering

Orkestrering udstiller 2 typer services - liste og detaljer - samt omfatter en række øvrige applikationsbyggeblokke.

* **Overbliksliste** - Returnerer et overblik inden for det datadomæne, der forespørges overblik over fx Sager. Der vil være en service for hvert datadomæne - fx sag, ydelse, frister etc.
* **Overbliks-detaljer** - Generisk service der repræsenterer data til overblik for et datadomæne. Servicen skal tilrettes og navngives i henhold til datadomæne og vil eksistere i samme antal instanser, som der er udvalgt datadomæner. Fx. en service for Sagsdetaljer, Ydelsesdetaljer eller Fristdetaljer.
* **Brugerstyring** - Ekstern applikationsservice til administration og anvendelse af identiteter og rettigheder (jf. Referencearkitektur for brugerstyring)
* **Indeksopdatering** - Service der kaldes fra fagsystemer eller domæneindeks, så data i evt. binære indeks kan opdateres. Denne service kan placeres forskellige steder i arkitekturen og er på figuren vist som ekstern i forhold til orkestreringslaget, men kan inkluderes i dette lag
* **Orkestrer servicekald** - Håndterer servicekald til datakilder/domæne indeks og håndterer fejlsituationer og timeout. Anvender Konfiguration og Aftalestyring til at udvælge hvilke datakilder/domæneindeks, der er relevant at kalde, samt at der er det aftalemæssige grundlag for at gennemføre kald.
* **Sammenstilling** - Sammenstiller svar fra underliggende datakilde til et samlet svar, der kan leveres til brugerflade
* **Konfiguration** - Funktionalitet til at konfigurere kald og sammenstilling ud fra datamodeller og datakilders services samt databehandleraftaler
* **Aftalestyring** - Konfiguration af aftaler (databehandleraftaler) og styring af hvilke brugerflader, der har det aftalemæssige på plads i forhold til datadomæner
* **Orkestreringslogning** - Funktionalitet til logning jf. logningskrav beskrevet i juridisk perspektiv.
* **Validering** - Validering af at svar fra datakilder/domæne indeks overholder datamodel (skemaer)
* **Binært indeks** - Dataobjekt der indeholder oplysninger om, hvilke datasamlinger der indeholder oplysninger om personer, virksomheder og andre forvaltningsobjekter.

### Integration

Integrationslagets primære funktionalitet er i forhold til den enkelte datakilde eller indeks at gøre data tilgængelig for orkestreringslaget, i et format der overholder den fælles datamodel for det aktuelle datadomæne, samt sikre at data er beriget med kontekstspecifikke data, der er relevante for overblik, og at data er klassificeret i henhold til aftalte klassifikationer.

![Figur 7.2.png](assets/Figur%207.2.png)

Figur 7.2 - Integration

Integrationslaget udstiller på nuværende tidspunkt to generiske services samt omfatter en række øvrige applikations-byggeblokke. Der anvendes endvidere en række eksterne applikationsbyggeblokke og services fx katalogservice.

* **Overbliksliste** - Returnerer et overblik inden for det datadomæne, der forespørges overblik efter. Der er én overblikslisteservice for et datadomæne alternativt pr. datakilde.
* **Overbliks-detalje** - Generisk service, der repræsenterer data til overblik for et datadomæne. Servicen skal tilrettes og navngives i henhold til datadomæne og vil eksistere i samme antal instanser, som der er domæneindeks og/eller datakilder, der leverer direkte. Eksempler er Sagsdetaljer og Ydelsesdetaljer, der fremgår af figuren.
* **Katalogservice** - Ekstern applikationsservice til kataloger, hvor integrationslaget kan slå op i de nødvendige kataloger.
* **Klassifikationsservice** - Ekstern applikationsservice hvor klassifikationsdata, der anvendes til klassifikation, og transformation af data kan fremsøges.
* **Søgning** - Søgning er opslag i et indeks og fremsøgning af data, når disse er placeret i et domæneindeks af performancemæssige hensyn. Hvilke data og omfang af indeks-data der er behov for, og dermed hvilken søgningsfunktionalitet, der implementeres, afklares ved implementering af integrationslaget som oftest i samråd med datakilden(-rne).
* **Integrationslogning** - Funktionalitet til logning jf. logningskrav beskrevet i juridisk perspektiv.
* **Berigelse** - Berigelse er funktionalitet til at berige data fra fagsystem med yderligere data, der er specifikke for overblik, men ikke findes i fagsystem. Fx fælles ledetekst der er nødvendig i forhold til visning på brugergrænsefladen. Data til berigelse placeres i dataobjektet kontekstspecifik data, da data er specifik for den enkelte datakilde og i forhold til overblikskontekst. Sker berigelsen med data der er aftalt på tværs af datakilder, kan disse hentes i et fælles katalog gennem katalogservicen (se Informationsperspektivet for beskrivelse af fælles kataloger). Den enkelte implementering af integrationslaget afgør, hvilke data der er nødvendige at placere i Kontekstspecifik data, da dette i stor udstrækning er afhængig af, hvilke data den enkelte datakilde kan levere.
* **Transformation** - er en central funktionalitet i integrationslaget, da data transformeres fra datakildens udstillingsdatamodel og format til den fælles udstillingsdatamodel for overblik, der er gældende for det givne datadomæne. Transformation anvender fælles kataloger og klassifikationer til hjælp for transformationen. En fælles klassifikation er fx sagsstatus for overblik.
* **Klassifikation** - Omfatter funktionalitet til at påføre de for overblik påkrævede klassifikationer, således at data kan vises sammenstillet i et brugervendt overblik.
* **Kataloger** - Ekstern komponent der udstiller katalogservicen.
* **Klassifikationer** - Ekstern komponent der udstiller klassifikationsservicen.
* **Brugerstyring** - Se Orkestreringslag for beskrivelse af denne service.

### Datakilder

Datakilder repræsenterer alle datakilder, der leverer data til overblik gennem den arkitektur, som referencearkitekturen beskriver. For datakildelaget beskrives to emner: Hvilke services som datakilder forventes at udstille, og hvilke krav som datakilden bør opfylde.

![Figur 7.3.png](assets/Figur%207.3.png)

Figur 7.3 - Datakilder

Datakilder, der ofte vil være repræsenteret ved et fagsystem - fx et sagssystem, skal i forhold til Integrationslaget udstille 2 services: Fagdata-overblik - der returnerer en Overbliksliste over relevante data i fagsystemet - og Fagdata-detaljer - der returnerer detaljer om et eller flere dataobjekter. Disse 2 services afspejler de tilsvarende services, som integrationslaget udstiller, men med den forskel, at fagsystemer leverer data i forhold til datamodel, der aftales med Integrationslaget. Dette kan fx være i forhold til fagsystemets interne datamodel eller en udstillingsmodel, som fagsystemet anvender til andre serviceanvendere.

Hvis fagsystemet gør brug af Binært indeks, skal fagsystemet kalde servicen Indeks-opdatering, når data opdateres i fagsystemet, eller når det findes relevant at opdatere indekset.

Datakilden og dermed fagsystemet skal sikre, at der kun leveres data, som anvenderen har lov til at se, hvilket giver behov for Brugerstyring på data samt behov for understøttelse af læseadgang, hvis overbliksdata skal kunne vises for 3. part.

Den nuværende fuldmagtsløsning understøtter, at der gives fuldmagt til løsninger fremfor data. I forhold til overblik er der behov for en løsning, der understøtter afgivelse af læseadgang til data. Referencearkitekturen ser følgende funktionelle krav i forhold til fuldmagt.

* Læseadgang skal kunne afgives til data eller udvalgte dataobjekter.
* En datakilde skal kunne forespørge, om der er afgivet læseadgang/fuldmagt til data.

### Implementeringsscenarier

Dette afsnit beskriver kort mulige implementeringer og kombinationer af services og funktionalitet fra orkestreringslaget, integrationslaget og datakildelaget. De beskrevne scenarier er udvalgt på baggrund af indsigt og erfaringer fra de gennemførte projekter for overblik. Implementeringscenarierne er ikke komplette løsninger, men er veldefinerede dele fra den samlede arkitektur, der kan realiseres som komponenter eller løsningsbyggeblokke. Disse komponenter vil stadig indgå i og overholde den definerede arkitektur.

| Implementeringsscenarie                                   | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| --------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Fælles orkestreringskomponent                             | Dette scenarie samler al funktionalitet fra orkestreringslaget i en fælles komponent samt udstiller services tilhørende orkestreringslaget.<br><br>Den fælles komponent vil eksistere i en fællesoffentlig instans og understøtte alle realiserede brugergrænseflader, der udstiller borgervendte overblik.<br><br>Der realiseres en tilsvarende komponent på virksomhedsområdet til udstilling af virksomhedsvendte overblik.<br><br>Herved vil alle brugergrænseflader kun skulle hente standardiserede data til overblik et sted.<br><br>![2 Implementering_C.png](assets/2%20Implementering_C.png)<br><br>Implementeringsscenarie med fælles, central orkestreringskomponent                                                                                                                                                                                                                                                                                                                                                                              |
| Domæneindeks                                              | Domæneindeks er en realisering af al funktionalitet i integrationslaget for et datadomæne, eksklusiv kataloger og klassifikationer, der er eksterne services i forhold til integration.<br><br>Domæneindeks udstiller integrationslagsservices for datadomænet.<br><br>Domæneindeks vil have integration til en eller flere datakilder og kan lagre udvalgte data. Domæneindeks vil være en realisering af implementeringsmønsteret Datadistributør (med brug af indeks, beskrevet i referencearkitektur for deling af data og dokumenter.<br><br><br>![1 Implementering B.png](assets/1%20Implementering%20B.png)<br>Implementeringsscenarie                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Staging-komponent                                         | Staging-komponent samler al funktionalitet fra integrationslaget og realiserer en intern implementering af datakilde services.<br><br>Datakilde services implementeres ovenpå en kopi af data fra datakilden, der er lagret i og vedligeholdt af Staging-komponenten.<br><br>Hvorledes integration mellem datakilde og Staging-komponent implementeres, forholder scenariet sig ikke til. Men det anbefales at tage udgangspunkt i de tekniske muligheder, som datakilden har.<br><br>Staging-komponent skal også varetage brugerstyring for data og understøtte anvendelse af fuldmagt på data på lige fod med en anden datakilde.<br><br>Set fra orkestreringslaget vil dette implementerings-scenarie udstille alle integrationslagets services og kan anvendes på lige fod med andre realiseringer af integrationslaget.<br><br>Scenariet kan være relevant for gamle legacy systemer og systemer, der afvikles på en teknologisk forældet platform.<br><br>![3 Implementering B2.png](assets/3%20Implementering%20B2.png)<br><br>Implementeringsscenarie |
| Datakilde leverer direkte til orkestreringslag            | Dette scenarie indebærer, at datakilden selv udstiller de services, som integrationslaget specificerer og selv håndterer den funktionalitet, som integrationslaget omfatter - fx transformation.<br><br>Dette scenarie er anvendeligt for nye systemer, hvis interne datamodel ligger meget tæt op af den fælles datamodel. Dvs., der er minimalt behov for egentlig transformation, men stadig berigelse og klassifikation.<br><br><br>![](assets/4%20Implementering%20C2.png)<br>Implementeringsscenarie med fælles, central orkestreringskomponent                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Kataloger                                                 | Nye kataloger kan realiseres som MVP-løsning som simple lister og er en specialisering af Overbliks-detaljer, hvor eksisterende kataloger understøtter behovet anvendes disse - fx datasætkatalog som katalog over datakilder.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Klassifikationer                                          | De nye klassifikationer, der oprettes til brug for overblik, kan som mulig MVP-løsning realiseres som simple lister - fx udstillet på arkitektur.digst.dk eller anden egnet site.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Realisering af orkestreringslag med anvendelse af GraphQL | Teknologier som fx GraphQL kan muligvis anvendes som teknologiplatform for realisering af orkestreringslaget.<br><br>Dette er relevant, hvis der forretningsmæssigt bliver behov for at tilgå sammenstillede data gennem et formaliseret forespørgselssprog frem for anvendelse af mere faste REST services.<br><br>Her gøres opmærksom på, at kapabiliteter i orkestreringslaget skal opfyldes af den valgte GraphQL platform.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

### Understøttelse af Mit Overblik

Mit Overblik er en løsning, der implementeres på borger.dk, hvor løsningen skal give borgerne et bedre tværgående digitalt overblik over egne forhold og igangværende sager hos offentlige myndigheder.

Referencearkitekturen understøtter Mit Overblik ved, at borger.dk realiserer funktionaliteten for visningsklienter i præsentationslaget og gennem anvendelse af de forskellige implementeringsscenarier beskrevet i afsnittet om målarkitektur (to-be situation - resumé).

![Figur 7.4.png](assets/Figur%207.4.png)

Figur 7.4 – Programmet Mit Overblik realiserer en række af referencearkitekturens kapabiliteter

### Anvendelse af implementeringsmønstre

Services og udstillingsmønstre i denne referencearkitektur følger implementeringsmønstrene fra Referencearkitektur for deling af data og dokumenter (RAD) med følgende præcisering:

Implementeringsmønstret Direkte adgang fra RAD er relevant for:

* Services der udstilles af Orkestreringslaget
* Services der udstilles af Integrationslaget
* Services der udstilles af datakilder

Ved implementeringsscenarier hvor en komponent favner flere lag, og de beskrevne services derved bliver interne, er det ikke påkrævet at følge implementeringsmønstrene fra RAD.

Implementeringsmønstret fra RAD, der introducerer en datadistributør, er relevant for implementeringsscenarierne Domæneindeks og Staging komponent, hvorfor der henvises til retningslinjer for dette mønster.

## Infrastruktur

Afsnittet beskriver de væsentligste forhold vedrørende den tekniske infrastruktur, som skal understøtte realisering af forretningsarkitekturen og applikationsarkitekturen beskrevet i denne referencearkitektur. Fx krav til robusthed, tilgængelig og skalerbarhed samt anvendelse af eksisterende infrastrukturbyggeblokke.

Den systemmæssige kontekst, som infrastrukturen skal understøtte, kan karakteriseres ved:

* Hentning og visning af data foregår i realtid, da visning sker på portaler og evt. apps, hvor brugere forventer gode svartider.
* Der er potentielt mange datakilder, der leverer data til det samme overblik.
* Visning, herunder på borger.dk og Virk, har krav om tilgængelighed på 24x7.

Ud fra denne kontekst peger referencearkitekturen på følgende behov for, at infrastrukturen og anvendte infrastrukturbyggeblokke skal:

* understøtte høj grad af robusthed, herunder stor fleksibilitet for skalerbarhed, således at alle lag i arkitekturen kan skaleres i forhold til belastning. De enkelte lag og komponenter skal kunne skaleres uafhængigt af hinanden, da det er uforudsigeligt, hvordan anvendelsesmønstret for overblik vil blive og hvilke komponenter/datakilder, der belastes mest.
* understøtte parallelitet i alle lag, hvilket er et ufravigeligt krav. Dels grundet samtidige anvendere dels grundet det brede antal datakilder og dermed forventet mange realiseringer af integrationslaget. Hvis en anvender vælger et overblik, der henter data fra 16 forskellige datakilder, skal fremsøgning og hentning af data ske parallelt, således at det reelt er svartiden for den “langsomste”, der sætter rammen for den samlede svartid, som anvenderen oplever.

Referencearkitekturen peger på anvendelse af følgende infrastrukturbyggeblokke:

* **NemID** og **NemLog-in** til håndtering af sikkerhed og brugerrettigheder.
* **Digitalpost-løsning** eller dokumentlager, hvor borger eller virksomhed kan tilgå dokumenter, der refereres til fra data - fx reference til sagsdokumenter, dvs., man viderestilles til disse løsninger.
* **Borger.dk** som obligatorisk portal for visning af overblik på borgerområdet.
* **Virk** som obligatorisk portal for visning af overblik på virksomhedsområdet.
* Andre portaler med selvbetjeningsløsninger eller selvstændige selvbetjeningsløsninger, hvor der skal vises overblik.
* Eksisterende kataloger, der indeholder relevant katalogindhold.

Følgende infrastrukturbyggeblokke er kandidater til anvendelse, når de er klar til anvendelse:

* **GovCloud** som platform for orkestreringslag.
* Fælles offentlig **fuldmagtsløsning**, når det er muligt at give fuldmagt på dataniveau.

## Bilag A: Tjekliste

Bilaget indeholder en oversigt over de væsentligste krav og anbefalinger, der kan udledes af referencearkitekturen. Kan anvendes til støtte for projekters planlægning, udarbejdelse af arkitektur og arbejde med at definere krav.

\[Afsnittet udfyldes, når erfaringer fra afprøvning er opsamlet\].

## Bilag B: Begrebsliste

Indeholder en samlet begrebsliste over referencearkitekturens begreber og terminologi, som følger begrebslisteskabelonen i modelreglerne. [Skabelonen og yderligere information findes på FDA's hjemmeside](/node/694).

|     |     |
| --- | --- |Metadata for begrebsmodel
| Namespace | `https://data.gov.dk/concept/profile/digitaltoverblik/` |
| Modelnavn | Tværgående digitalt overblik for borgere og virksomheder |
| Modelansvarlig | Digitaliseringsstyrelsen |
| Versionsnummer | 0.8.0 |
| Seneste opdateringsdato | 10-10-2019 |
| Modelstatus | Under udvikling |
| Godkendelsesstatus | Afventer godkendelse |
| Modelomfang | Begrebsmodel for referencearkitekturen |
| Godkendt af |     |
| Forretningsområde | 06.38.10 Digital Infrastruktur |
| Juridisk kilde |     |
| Kilde | Fællesoffentlig Digital Arkitektur (arkitektur.digst.dk) |
| Sprog | Dansk |
| Beskrivelse | Begrebsmodel for begreber i referencearkitektur for digitalt overblik |

|     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |Begreber
| Foretrukken term | Accepteret term | Frarådet term | Definition | Eksempel | Kommentar | Juridisk kilde | Kilde | tilhører emneområde |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **tværgående overblik** |     |     | _Visning af information vedrørende den enkelte borgers og virksomheds anliggender med det offentlige, som er konkret, relevant og overbliksskabende for den enkelte borger eller virksomhed_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **lokale overblik** |     |     | _overblik der viser data fra en enkelt myndighed med tilhørende detaljevisning indenfor et meget afgrænset datascope_ | Visning af overbliksdata i selvbetjeningsløsninger hvor brugeren præsenteres for en opsummering af sagsforløb eller engagement | Er primært rettet mod virksomhedsområdet |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **brugervendt** | Borgervendt, Virksomheds-vendt |     | _overblik hvor data, der vises, er rettet mod borgere og/eller virksomheder frem for sagsbehandlere_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **myndighedsdomæne** |     |     | _Forretningsområde som en myndighed er ansvarlig for_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **orkestreringskomponent** |     |     | _Applikationskomponent der implementerer funktionalitet beskrevet for orkestreringslaget_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **domæneindeks** | Indeks |     | _Er instans af implementeringsmønster Datadistributør (med brug af indeks fra FDA referencearkitektur for deling af data og dokumenter_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| brugerstyring |     |     | _Håndhævelse af adgangskontrol og administration af brugere og deres rettigheder_ |     |     |     | FDA Referencearkitektur for brugerstyring |     |
| **_orkestrering_** | Orkestrer servicekald |     | _Håndtering af samtidige servicekald og sammenstilling af svar til et samlet respons_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_overbliksliste_** |     |     | _Service der returnerer et sammenstillet overblik eller et overblik indenfor det datadomæne_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_overbliksdetalje_** |     |     | _Generisk service der returnerer detaljedata til overblik_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_indeksopdatering_** |     |     | _Service der kaldes fra fagsystemer eller domæneindeks, så data i evt. binære indeks kan opdateres_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_indeks_** | **binært indeks** |     |     |     |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| **_sammenstilling_** |     |     | _Sammenstilling af svar fra underliggende datakilde til et samlet svar_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_konfiguration_** |     |     | _konfigurere kald og sammenstilling ud fra datamodeller_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_aftalestyring_** |     |     | _Konfiguration af aftaler (databehandleraftaler) i forhold til kald til datakilder_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| _logning_ | Orkestrerings-logning, integrationslogning |     |     |     |     |     |     |     |
| **_katalogservice_** |     |     | _Ekstern applikationsservice til kataloger_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_klassifikationsservice_** |     |     | _Ekstern applikationsservice hvor klassifikationsdata_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| **_berigelse_** |     |     | _At berige data fra fagsystem med yderligere data der er specifikke for overblik_ |     |     |     | FDA Referencearkitektur for tværgående digitalt overblik |     |
| _klassifikation_ |     |     | >   |     |     |     |     |     |
| _besked_ |     |     | _skriftlig eller mundtlig oplysning som sendes eller overbringes til andre_ |     |     |     | Den Danske Ordbog |     |
| data | registerdata |     | _Information lagret med henblik på (gen)anvendelse_ |     | Tidligere dansk definition: enhver repræsentation af fakta eller ide´ i en sådan form, at den kan kommunikeres eller omformes ved en eller anden proces \[Bogen om EDB. H.B. Hansen, 1969\] |     | ISO/IEC 11179- 4:2004 |     |
| dataansvarlig | Persondata-ansvarlig |     | _en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der alene eller sammen med andre afgør, til hvilke formål og med hvilke hjælpemidler, der må foretages behandling af person- oplysninger_ | En privatpraktiserende læge er dataansvarlig for hendes patientjournal |     | (EU) 2016/679 |     |     |
| databehandler | Persondatabehandler |     | _en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der behandler personoplysninger på den dataansvarliges vegne_ | Driftleverandøren af en database til en offentlig myndighed er databehandler på vegne af denne. |     | (EU) 2016/679 |     |     |
| adgangskontrol |     |     | _forretningsfunktion der afgør hvilke funktioner og data, en bruger får adgang til på baggrund af brugerens attributter og tjenestens sikkerhedspolitik_ |     |     |     | FDA Referencearkitektur for brugerstyring |     |
| adgangspolitik |     |     | _definition af kriterierne for at få adgang til en applikationsservice._ | En skoleleder kan have adgang til CPR oplysninger, hvis personen er elev, ansat på skolen eller pårørerende til elever. |     |     | FDA Referencearkitektur for brugerstyring |     |
| dataanvender | anvender af data;<br><br>anvender |     | _person eller organisation der behandler data til eget formål_ | Danmarks Statistik anvender data om CPR-data til udarbejdelse af le vealders-statistik |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| behandling af personoplysninger | Persondata-behandling; behandling af persondata | behandling; databe- handling | _enhver aktivitet eller række af aktiviteter — med eller uden brug af automatisk behandling — som personoplysninger eller en samling af personoplysninger gøres til genstand for, f.eks. indsamling, registrering, organisering, systematisering, opbevaring, tilpasning eller ændring, genfinding, søgning, brug, videregivelse ved transmission, formidling eller enhver anden form for overladelse, sammenstilling eller samkøring, begrænsning, sletning eller tilintetgørelse_ |     |     | EU) 2016/679 |     |     |
| datadistributør | datafordeler; distributør |     | _databehandler der som databehandler giver anvendere adgang til data på vegne af den dataansvarlige_ | Styrelsen for Dataforsyning og Effektivisering distribuere CPR data på vegne af Indenrigsministeriets CPR kontor |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| datasamling | datasæt; register;<br><br>datakilde |     | _en samling af oplysninger bestående af enkelte dele der forvaltes under et_ | CPR registeret, Det Interregionale billedindex (IBI) | Minder om begrebet ’arkiv’ fra Sag og Dokument samt om PSI lovens definition af datasamling. |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| dataservice |     |     | _applikationsservice der videregiver oplysninger fra datasamlinger på forespørgsel under håndhævelse af nødvendig adgangskontrol_<br><br> > | Kommunernes serviceplatform udstiller en person-service til opslag i CPR og skoledistrikter | oftest ved håndhævelse af adgangskontrol, men ikke nødvendigvis |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| forespørgsel | request |     | _meddelelse der sendes til en dataservice med forventning om svar indeholdende specifikke data_ | En link på en hjemmeside er en forespørgsel til en server, der svarer med en hjemmeside |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| _fuldmagt_ |     |     | _formel tilladelse til at handle på vedkommendes vegne i nærmere bestemte situationer_ |     |     |     | Den Danske Ordbog |     |
| meddelelse | elektronisk meddelelse |     | _formel besked der sendes elektronisk med veldefineret sikkerhed, tillid, integritet og leverancesikkerhed_ | En e-mail sendt via sikker e-mail mellem myndigheder betragtes som ulæselig for andre end modtagerens organisation, men den er ikke garanteret at nå frem. |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| modtager af elektroniske meddelelser | modtager |     | _forretningsrolle (person eller organisation) der modtager elektronisk meddelelse_ | En borger kan være modtager af en meddelelse sendt via Digital Post |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| påmindelse | advis; notifikation |     | _en besked der får modtager til at tænke på en vigtig begivenhed_ |     | Typisk uden dokumentation af behandling eller beskyttelse jf meddelelse |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| _registrator_ |     |     | _person eller apparat der registrerer noget_ |     |     |     | Den Danske Ordbog |     |
| adgangsrettighed |     |     | _rettighed der tildeles en bruger eller roller, der giver adgang til at udføre funktioner i et it-system._ |     |     |     | FDA Referencearkitektur for brugerstyring |     |
| samtykke til per- sondatabehandling | Samtykke; personda- tasamtykke |     | _klar bekræftelse der indebærer en frivillig, specifik, informeret og utvetydig viljestilkendegivelse fra den registrerede, hvorved vedkommende accepterer, at personoplysninger om vedkommende behandles_ |     |     | (EU) 2016/679 |     |     |
| svar | respons |     | _meddelelse dannet af dataservice som besvarer en forespørgsel_ |     |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| videregivelse af data | deling af data; data- deling |     | _forretningsfunktion hvorved data overføres ud af organisation_ | sende meddelelse indeholdende sagsoplysninger; Sundhedsdatastyrelsen videregiver medicinoplysninger fra Fælles Medicinkort til SOSU assistenter i Aalborg Kommune |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| videregivelse på forespørgsel |     |     | _integrationsmønster hvor data videregives af dataansvarlig på forespørgsel på anvenders initiativ_ |     |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |
| videregivelse ved meddelelse |     |     | _integrationsmønster hvor data videregives ved meddelelse af dataansvarlig på dennes initiativ_ |     |     |     | FDA Referencearkitektur for deling af data og dokumenter |     |

## Bilag C: Implikationer af Hvidbogens principper

Nedenstående liste af fællesoffentlige principper fra Hvidbogen er fundet relevante for overblik, hvor der for hvert princip beskrives implikationen i forhold til referencearkitekturen.

* Fællesoffentlig princip 1 Arkitektur styres på rette niveau efter fælles rammer
  * Implikationer for overblik er, at arkitekturregel 1.2 og 1.3 er rammesættende for selve referencearkitekturens specifikke indhold og scope, da referencearkitekturen skal indgå i den fælles arkitektur, og dokumentskabelon og terminologi følger de fællesoffentlige retningslinjer for arkitekturdokumentation
* Fællesoffentlig Princip 2: Arkitektur fremmer sammenhæng, innovation og effektivitet
  * Implikationer for overblik er, at arkitekturreglerne 2.1, 2.4 og 2.5 skal indtænkes i både forretning og applikationsarkitektur for overblik. Anvend eksisterende byggeblokke og design nye byggeblokke så de kan genbruges og optages i FDA. Referencearkitektur skal beskrive en arkitektur, der understøtter forandringer i overblik gennem mulighed for inddragelse og understøttelse af nye dataområder og nye overblik. Arkitekturen for overblik skal også give mulighed for, at private aktører kan realisere byggeblokke for overblik og anvende etablerede overbliksløsninger eller udvalgte byggeblokke
* Fællesoffentlig Princip 3: Arkitektur og regulering understøtter hinanden
  * Implikationer for overblik er, at arkitekturregel 3.1 er yderst relevant for overblik, da overblik går på tværs af myndigheder og ressortområder. De juridiske og aftalemæssige forhold, der er gældende, og som skal etableres, er en vigtig facet af referencearkitekturen
* Fællesoffentlig Princip 6: Gode data deles og genbruges
  * Implikationer af arkitekturregel 6.1 og 6.4 er, at disse er fundamentale egenskaber, som hele referencearkitekturen bygger på, da overblik ikke danner egne data, men genbruger og viser eksisterende data, der derved deles fra datakilderne
* Fællesoffentlig Princip 7: It-løsninger samarbejder effektivt
  * Implikationer af arkitekturregel 7.1 er, at denne arkitekturregel skal indtænkes for alle snitflader, der indgår i arkitekturen for overblik, så aktører, der enten leverer data eller anvender byggeblokke, har veldefinerede snitflader at arbejde op imod.
* Fællesoffentlig Princip 8: Data og services leveres driftssikkert
  * Implikationer af arkitekturregel 8.1 er, at dataleverance- og drift-sikkerhed er vigtige elementer at indtænke i arkitekturen, specielt da overblik er på tværs af myndigheder og datakilder

## Bilag D: Kataloger

Kataloger som værktøj for digitale assets har ofte en dobbeltfunktion, hvor kataloget både har en opslagsfunktion, hvor brugere kan finde, hvad der eksisterer - fx som et produkt/varekatalog -, samt har funktionalitet til at holde det aktuelle asset, repositorie funktion, hvor man kan hente det relevante digitale produkt - fx en datamodel i UML. I nedenstående har MVP-løsningen primært sigte på at understøtte opslagsfunktionen, hvor den fulde løsning også inkluderer repository funktionen for de kataloger, hvor dette er relevant.

Kataloger beskrives i forhold til følgende:

* Katalognavn: Navn på kataloget
* Beskrivelse: Kort beskrivelse af kataloget og indholdet af kataloget
* Anvendere: Beskrivelse af de primære anvendere af kataloget
* MVP: MVP-løsning for understøttelse af kataloget med fokus på de primære anvendere
* Fuld løsning: Fremtidig fuld løsning der også understøtter andre anvendere
* Andre anvendere og deres formål: Kort beskrivelse af andre potentielle anvendere af kataloget

| Katalog                                                                                  | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Anvendere                                                                                                                                                                                                                                                                                                                                                                      | MVP                                                                                                                                                                                                                                                                                                                                                                         | Fuld løsning                                                                                                                                                                                                                                                                                                                                                                                                                              | Andre anvendere og deres formål                                                                     |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Datakildekatalog                                                                         | Katalog over hvilke datakilder der findes for de forskellige datadomæner, der er inkluderet i overblik eller er kandidat til at levere data til overblik.<br><br>Kataloget indeholder også information om end-point, der udstilles af datakilden.                                                                                                                                                                                                                                                                                                                | Forvalter af orkestrering (fx Orkestreringskomponent), hvor information fra kataloget skal anvendes til konfiguration af orkestreringen.<br><br>Forvaltere af overbliks-løsninger og portal/app administratorer har behov for at vide, hvilke data der kan fremsøges, hvem der er dataansvarlige, samt hvad der skal gøres for at etablere de nødvendige databehandleraftaler. | Programmet har et internt katalog (fx et regneark).<br><br>En teknisk MVP i forhold til en orkestreringskomponent er et internt katalog, der evt. er en integreret del af konfigurationen af orkestreringskomponent.                                                                                                                                                        | Der etableres et selvstændigt katalog over datakilder og end-point, som evt. er tæt koblet til Datavejviser med referencer til beskrivelse af datasæt, datamodeller, beskrivelse af datakvalitet og API’er.                                                                                                                                                                                                                               |                                                                                                     |
| Datamodel-katalog                                                                        | Katalog over fælles datamodeller for overblik.<br><br>Kataloget indeholder kort beskrivelse af modellen og link til, hvor den specifikke model og tilhørende skemaer kan findes. Modeller er i formaliseret modelsprog fx UML.<br><br>Evt. behov for interaktiv funktionalitet til opslag/fremsøgning af enkeltelementer samt fx mulighed for at kommentere eller fremsætte ændringsønsker.                                                                                                                                                                      | Anvendes af myndigheder og deres it-leverandører, når integration til orkestreringen skal implementeres. Det omfatter både datakilder og præsentationsløsninger.                                                                                                                                                                                                               | Fælles datamodeller placeres på data.gov.dk, der udvides til ikke kun at være en indgang for grunddata-modeller.                                                                                                                                                                                                                                                            | Indhold i datamodel-kataloget løftes over i det fællesoffentlige datakatalog 2.0, der i kommende version har al nødvendig funktionalitet.                                                                                                                                                                                                                                                                                                 | Datamodellører der udarbejder nye datamodeller.                                                     |
| Katalog over fælles klassifikationer og udfaldsrum                                       | Er et katalog der giver en samlet oversigt over de klassifikationer, kontrollerede udfaldsrum i form af ledetekster o.l., der er defineret til overblik i forbindelse med udarbejdelse af fælles datamodeller.<br><br>Katalogfunktionen er flad, men bagvedliggende funktion kan have større funktionalitet fx til understøttelse af relationer mellem klassifikationer.<br><br>Katalog, der også er repositorie og dermed indeholder selve klassifikationen, kan udstille to services: Fuldt download hhv. web service fx baseret på nøgleord eller referencer. | Kataloget anvendes af datakilder til at finde den nyeste klassifikation og anvende denne i forbindelse med opmærkning af data, der leveres af datakilder til overblik. Kataloget anvendes desuden af visningsportaler, app o.l. til konfiguration af søgning og præsentation, fx ifbm emnestrukturering.                                                                       | MVP-løsning for dette katalog er at distribuere fx gennem publicering på data.gov.dk (stabil URL) filer med de aftalte klassifikationer og lister med udfaldsrum (ledetekster), som skal bruges på tværs.                                                                                                                                                                   | Der etableres en fællesoffentlig komponent, der kan udstille en klassifikationsservice, som gør det muligt at søge i og udtrække klassifikationer. Denne løsning bør afvente at antallet af klassifikationer forøges så meget, at der er behov for søgefunktionalitet, eller at der i andet regi etableres en katalog-service for klassifikationer, som også kan anvendes af klassifikationer for overblik. Evt. genbrug af ISA2 løsning. | Datamodellører der udarbejder nye datamodeller<br><br>UX-designere fx ved udarbejdelse af mock-ups. |
| Katalog over informationssider                                                           | Katalog over informations-og vejledningssider.<br><br>Fx opmærket efter FORM/KLE.<br><br>Indholdet af kataloget vil være:<br><br>*   Kort beskrivelse af indhold<br>*   FORM/KLE opmærkning<br>*   Link til side, fx [artikelside på borger.dk med information om navne- og navneændring](https://www.borger.dk/familie-og-boern/Navne-og-navneaendring/Navneaendring)<br>*   Begrænsninger i anvendelse. Angiver om indholdet har begrænset anvendelse, fx at information er specifik for kommuner i hovedstadsområdet                                          | Anvendes af datakilder til at indsætte link til information og vejledninger, der kan give brugere af overblik mere uddybende information om betydning af data, der vises i overblik.<br><br>Anvendes af præsentationslaget/visningsklienter til give brugere generel baggrundsinformation om opgaveområde, der vises data for i overblik.                                      | Borger.dk har eksisterende katalog, Artikelimport, der fuldt ud kan anvendes som MVP-løsning. Se: [https://artikelimport.borger.dk](https://artikelimport.borger.dk)<br><br>Der er veletableret governance (borger.dk redaktion) for indhold i borger.dk’s katalog, så det er opdateret og tidssvarende.<br><br>Der er pt. ikke en opdateret opmærkning efter FORM/KLE.     | Afventer yderligere behov/behovsafdækning                                                                                                                                                                                                                                                                                                                                                                                                 | Indholds-redaktører for portaler eller app’s der anvender indhold fra borger.dk.                    |
| Katalog over specifikationer og lign. der skal anvendes til implementering (repositorie) | Behov for stabilt sted hvor relevant arkitektur og tekniske specifikationer som fx anvendelsesprofiler lagres. Ikke UML-model, men tekniske specifikationer.<br><br>Digitaliser.dk har indtil nu haft denne funktion, men bliver nedlagt.<br><br>Repositorie skal være stabilt og organisationsuafhængigt.                                                                                                                                                                                                                                                       | Anvendes af it-leverandører/udviklere der skal implementere services/snitflader der udstiller data til overblik, samt anvendere af de udstillede services, fx visningsklienter.                                                                                                                                                                                                | Placeres på Arkitektur.digst.dk som en liste af dokumenter/pakker der kan downloades.                                                                                                                                                                                                                                                                                       | Afventer yderligere behov/behovsafdækning.                                                                                                                                                                                                                                                                                                                                                                                                |                                                                                                     |
| Selvbetjenings-løsninger                                                                 | Kataloget indeholder relevante selvbetjeningsløsninger, der tilbydes af offentlige myndigheder.<br><br>Indholdet af kataloger kan fx være:<br><br>*   Navn: Navn/titel på selvbetjenings-løsning<br>*   Link: URL til selvbetjeningsløsning<br>*   Beskrivelse: Kort tekst der beskriver selvbetjeningsløsning. Under 10 ord<br>*   Ansvarlig myndighed: Angivelse af hvilken myndighed der er ansvarlig for selvbetjeningsløsning<br>*   FORM-klassifikation: Klassifikation med FORM opgave-nr.                                                                | Datakilder: til konfiguration/udfyldelse af attributter i entiteter i datamodel for anvendelsesprofilen for det givne datadomæne.                                                                                                                                                                                                                                              | En MVP-løsning ift Mit Overblik er enten<br><br>1.  at ansvaret placeret hos den enkelte myndighed, der skal levere data til Mit Overblik eller<br>2.  at DIGST vedligeholder en fælles liste, fx i form af et excel-regneark baseret på udtræk fra borger.dk’s nuværende katalog, der publiceres og gøres tilgængeligt til download. FORM opmærkningen skal dog opdateres. | Borger.dk har i dag et internt katalog over selvbetjeningsløsninger,der er udstillet på borger.dk. Borger.dk kataloget kan udvides med relevante felter og gøres tilgængelig, enten via artikel-eksport eller en service. FORM opmærkningen skal opdateres. Dette skal dog aftales med borger.dk.                                                                                                                                         | Guides: Anvender katalog til opsætning/konfi-guration af servicekort.                               |

## Bilag E: Oversigt over kilder og baggrundsmateriale

Afsnittet beskriver det baggrundsmateriale, der indgik i udarbejdelsen af referencearkitekturen.

| Kilde                             | Materiale                                                                                                                                                                                                                                                                                |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Regeringen, KL og Danske Regioner | **Referencearkitektur for selvbetjening**; april 2017. [https://arkitektur.digst.dk/referencearkitektur-selvbetjening](https://arkitektur.digst.dk/referencearkitektur-selvbetjening)                                                                                                    |
| Regeringen, KL og Danske Regioner | **Referencearkitektur for deling af data og dokumenter**; maj 2018; [https://arkitektur.digst.dk/referencearkitektur-deling-af-data-og-dokume...](https://arkitektur.digst.dk/referencearkitektur-deling-af-data-og-dokumenter-0)                                                        |
| Regeringen, KL og Danske Regioner | **Referencearkitektur for brugerstyring**; april 2017; [https://arkitektur.digst.dk/rammearkitektur/referencearkitekturer/refere...](https://arkitektur.digst.dk/rammearkitektur/referencearkitekturer/referencearkitektur-brugerstyring)                                                |
| Regeringen, KL og Danske Regioner | **Den fællesoffentlige digitaliseringsstrategi 2016-2020**; maj 2016. [https://digst.dk/strategier/den-faellesoffentlige-digitaliseringsstrateg...](https://digst.dk/strategier/den-faellesoffentlige-digitaliseringsstrategi/tidligere-strategier/digitaliseringsstrategien-2016-til-2020/) |
| Regeringen, KL og Danske Regioner | **Digitaliseringspagten;** [https://digst.dk/media/19919/digitaliseringspagt-en-ny-retning-for-det-f...](https://digst.dk/media/19919/digitaliseringspagt-en-ny-retning-for-det-faellesoffentlige-samarbejde.pdf)                                                                        |
| KL                                | **ADDA-projektdokumentation**; [www.kl.dk/adda](http://www.kl.dk/adda)                                                                                                                                                                                                                   |
|                                   | PoC dokumentation                                                                                                                                                                                                                                                                        |
|                                   | **Initiativ 1.3 Analysedokumentation;** [https://digst.dk/digital-service/mit-overblik/](https://digst.dk/it-loesninger/borgerdk/mit-overblik/)                                                                                                                                                 |
| EU-kommissionen                   | **EIRA v3.0** - European Interoperability Reference Architecture. [https://ec.europa.eu/isa2/solutions/eira\_en](https://ec.europa.eu/isa2/solutions/eira_en)                                                                                                                            |
| EU-kommissionen                   | **EIF** - European Interoperability Framework. [https://ec.europa.eu/isa2/eif\_en](https://ec.europa.eu/isa2/eif_en)                                                                                                                                                                     |
| Digitaliseringsstyrelsen          | **Modelregler v2.0**; [https://arkitektur.digst.dk/node/1091](https://arkitektur.digst.dk/node/1091)                                                                                                                                                                                     |
| ISO                               | **ISO 27000**; [https://www.iso.org/isoiec-27001-information-security.html](https://www.iso.org/isoiec-27001-information-security.html)                                                                                                                                                  |
| Digitaliseringsstyrelsen          | **Sådan stiller du krav til leverandører om informationssikkerhed - katalog**; [https://digst.dk/styring/standardkontrakter/klausuler-til-informationssi...](https://digst.dk/styring/standardkontrakter/klausuler-til-informationssikkerhed/kravkatalog-til-leverandoerer/)             |
| Regeringen, KL og Danske Regioner | FDA - De**n fællesoffentlige digitale arkitektur**, [https://arkitektur.digst.dk/](https://arkitektur.digst.dk/)                                                                                                                                                                         |
| KL                                | **Fælles kommunale rammearkitektur;** [https://www.kl.dk/okonomi-og-administration/digitalisering-og-teknologi/...](https://www.kl.dk/okonomi-og-administration/digitalisering-og-teknologi/den-faelleskommunale-rammearkitektur/)                                                       |
| Regeringen, KL og Danske Regioner | **Hvidbog om fællesoffentlig digital arkitektur**; juni 2017. [https://arkitektur.digst.dk/node/241](https://arkitektur.digst.dk/node/241)                                                                                                                                               |
| The Open Group                    | **ArchiMate v3.0**, juni 2016. [https://publications.opengroup.org/archimate-library](https://publications.opengroup.org/archimate-library)                                                                                                                                              |

## Fodnoter

\[1\] Vision udledt af digitaliseringsstrategien 2016-2020 og aftalepapir for initiativ 1.3. [Temaside på Digitaliseringsstyresens hjemmeside med information om initiativ 1.3 https://digst.dk/media/12002/13-overblik-over-egne-sager-og-ydelser-aftalepapir.pdf](file:///C:/Users/B014441/Desktop/Eksport%20til%20Outlook/Temaside%20på%20Digitaliseringsstyresens%20hjemmeside%20med%20information%20om%20initiativ%201.3%20https:/digst.dk/media/12002/13-overblik-over-egne-sager-og-ydelser-aftalepapir.pdf)

\[2\] Såfremt det kan ske inden for de pågældende myndigheders eksisterende kanalstrategi og som minimum på en fællesoffentlig portal som borger.dk og Virk

\[3\] Udvalget for data og arkitektur har fra primo 2020 overtaget ansvaret for review og optagelse i FDA fra den nu nedlagte Styregruppe for data og arkitektur.

\[4\] Kilde: Deloitte: “Sags- og Ydelsesoverblik. Designanalyse af sags- og ydelsesoverblik”. Pjece: “Digital service i verdensklasse”

\[5\] Vision udledt af digitaliseringsstrategien 2016-2020 og aftalepapir for initiativ 1.3. [Temaside på Digitaliseringsstyresens hjemmeside med information om initiativ 1.3https://digst.dk/media/12002/13-overblik-over-egne-sager-og-ydelser-aftalepapir.pdf](https://digst.dk/media/12002/13-overblik-over-egne-sager-og-ydelser-aftalepapir.pdf)

\[6\] Kilde: [Udgivelse fra Regeringen, KL og Danske Regioner om ny retning for det fællesoffentlige samarbejde](https://digst.dk/media/19919/digitaliseringspagt-en-ny-retning-for-det-faellesoffentlige-samarbejde.pdf)

\[7\] Kilde: [Afsluttende rapport udgivet af Digitaliseringsstyrelse omhandlende Sags- og Ydelsesoverblik](https://digst.dk/media/18978/sags-og-ydelsesoverblik-behovsanalyse-afsluttede-rapport.pdf)

\[8\] Primær kilde: Sags- og ydelsesoverblik, Designanalyse af sags og ydelsesoverblik. Afsluttende rapport, 31. August 2017. [https://digst.dk/media/18978/sags-og-ydelsesoverblik-behovsanalyse-afslu...](https://digst.dk/media/18978/sags-og-ydelsesoverblik-behovsanalyse-afsluttede-rapport.pdf)

\[9\] Inden for rammerne af myndighedernes kanalstrategier.

\[10\] Dette afsnit udbygges evt. i kommende versioner. Herunder kunne man afdække it-landskabet og deres udviklingsplaner for de væsentligste it-systemer som kommer til at indgå i overblik.

\[11\] Se [Digitaliseringsstyrelsens temaside om overblik over egne sager og ydelser](https://digst.dk/digital-service/brugeroplevelse/)

\[12\] I KL's projekt 'Borgerens Adgang til Egne Data' har KL i samarbejde med 5 kommuner, borger.dk og KOMBIT udviklet løsningen Borgerblikket. Med Økonomiaftalen for 2020 er Borgerblikket blevet en del af det fællesoffentlige tiltag om Mit Overblik. Se [KL's temaside om Mit Overblik](https://www.kl.dk/okonomi-og-administration/digitalisering-og-teknologi/sammenhaengende-digital-borgerservice/projektet-om-borgerens-adgang-til-egne-data/)

\[13\] DIGST har gennemført PoC på orkestreringskomponent til borgervendte overblik og ERST har gennemført PoC på virksomhedsvendte overblik

\[14\] Se [Temaside om Sag- og Dokumentstandarder i den fællesoffentlige digitale rammearkitektur](https://arkitektur.digst.dk/rammearkitektur/sag-og-dokument-standarder)

\[15\] [https://www.datatilsynet.dk/media/6893/registreredes-rettigheder.pdf](https://www.datatilsynet.dk/media/6893/registreredes-rettigheder.pdf)

\[16\] ISO 27001 skal følges af statslige myndigheder: [https://digst.dk/sikkerhed/iso27001/](https://digst.dk/sikkerhed/iso27001/)

\[17\] FIT: Fortrolighed, Integritet, Tilgængelighed (engelsk: CIA)

\[18\] Jf. referencearkitektur for deling af data og dokumenter, se bilag B Begrebsliste

\[19\] Se Referencearkitektur for brugerstyring for detaljer. [https://arkitektur.digst.dk/rammearkitektur/referencearkitekturer/refere...](https://arkitektur.digst.dk/rammearkitektur/referencearkitekturer/referencearkitektur-brugerstyring)

\[20\] Organisation er defineret i “Specifikation af Model for Organisation. Version 2.0”

\[21\] Kilde: [Temaside af Eurofound om karakteristik af en medarbejder](https://www.eurofound.europa.eu/observatories/eurwork/industrial-relations-dictionary/employee)

\[22\] Bemærk at implementering af notifikationer på borgerområdet forudsætter en aftale herom mellem de relevante parter.
