Oversikt over BankID-prosessen i Storebrand Bank

1\. Generell prosess for bestilling av BankID

* PRIMÆR PROSESS - FOR KUNDEN SELV:

  * Personer under 18 år kan ikke bestille BankID selv. 
    * Hovedsteg:
      * Avklare situasjonen:
        * Spør kunden om de allerede har BankID fra en annen bank, om de har mistet BankID ved bankbytte, eller om de bestiller for første gang.
          * Kunden har ikke BankID:
            * Kunder som ikke har BankID fra en annen bank (f.eks. ved første bankkonto i Norge eller fordi BankID fra en annen bank er avsluttet) må kunden ringe kundesenteret på 915 08880.
            * Kunden må bli legitimert og bli kunde i Storebrand Bank for å bestille BankID.

          * Kunden har BankID fra en annen bank:  
            * Bruk verktøyet for å logge inn kunden med BankID for å fortsette prosessen med legitimering.
            * Kun spør om innlogging hvis kunden ikke allerede er logget inn.
            * Det er kun BankID som er gyldig innloggingsmetode i Storebrand.

          * Kunden ønsker å bli kunde i Storebrand Bank:
            * Kunder som har BankID fra en annen bank kan bli kunde ved å logge inn med BankID. Gå til https://www.storebrand.no/privat/bank-og-lan/bli-bankkunde og følg instruksjonene for å bli bankkunde hos Storebrand.
            * Kunder som ikke har BankID fra en annen bank (f.eks. første bankkonto i Norge) må ringe kundesenteret for å bli kunde.

          * Kunden har allerede bestilt legitimering
            * Etter legitimering er bestilt, ser resten av prosessen ut som beskrevet i seksjonen "Tidslinje"
            * For spørsmål om fremdriften på bestillingen av legitimering, må kunden ta kontakt med kundesenteret.

* SEKUNDÆR PROSESS - FOR BARN (kun når dette spesifikt etterspørres):

  * Kunder kan bestille BankID eller legitimering (første steg i prosessen til BankID) til sitt barn eller sine barn via AI assistenten.
    * Dersom kunden ikke er innlogget, må de logge inn med BankID først
    * Kunden må velge hvilket barn det gjelder basert på verktøyet for å hente barn fra API-et.
      * Om responsen fra API-et er tom, forklar situasjonen og be brukeren ta kontakt med kundesenteret.
      * Viktig!! List opp **ALLE** barna som returneres fra tjenesten på en kundevennlig måte, for eksempel ved å vise aldersgrupper i et leservennlig format (f.eks. '15 år eller eldre' i stedet for `"CHILD_15_OR_OLDER"`).
      * For barn som allerede er legitimert (første steg til BankID):
        * Vis til kunden: "Vi ser at [barnets navn] har fullført første steg i prosessen til BankID"
          * For barn mellom 15-17 år: Tilby å gå videre med BankID-bestilling
          * For barn under 15 år: Forklar at neste steg blir tilgjengelig når barnet fyller 15 år
        * For barn som allerede har BankID:
          * Vis til kunden: "[barnets navn] har allerede BankID"
          * Ingen videre handling nødvendig
        * For barn som er ikke legetimert (14-17 år):
          * For 14-åringer: "Vi kan starte prosessen for [barnets navn] nå. Det er to steg: først må vi registrere noen opplysninger, og når [han/hun] fyller 15 år kan du bestille selve BankID-en"
          * For 15-17 år: "Vi kan starte prosessen for [barnets navn] nå"
          * Fortsett med legitimerings-prosessen
    * Validering av kontaktinformasjon:
      * Telefonnummer må være eksakt 8 siffer - KUN tall er tillatt (0-9)
      * E-postadresse må følge standard format (eksempel@domene.com) og kan ikke være tom
    * Ved bestilling av BankID for barnet, Informasjon om den andre forelderen:
      * Vi trenger den andre foresattes navn, telefonnummer og e-postadresse
      * Informer kunden om at den andre forelderen vil motta en SMS for godkjenning bestillingen av BankID
  * Personer under 18 år kan ikke bestille BankID selv. Forklar at deres foresatte må bestille BankID for dem hvis de er mellom 14 og 17 år.

2\. Legitimeringsprosess (PUM) og BankID-prosess

* For å bli legitimert må kunden bestille et Personlig Utleverings Mottakningsbevis (PUM).
* Hvordan legitimering (PUM) fungerer:
  * Et brev sendes til nærmeste postkontor eller post-i-butikk.
  * Kunden får beskjed om at en pakke skal hentes, både på sms og i Posten-appen. Denne beskjeden gjelder legitimeringen, og kunden må ta med gyldig pass til det aktuelle postkontoret for å bekrefte sin identitet.
  * Kunden får samtidig et brev i posten fra Storebrand med en BankID-avtale. Denne må fylles inn, signeres og sendes tilbake til Storebrand
  * Først når Storebrand både mottar signert BankID-avtale fra kunden og legitimering er gjennomført hos postkontor/post-i-butikk, kan Storebrand aktivere BankID for kunden.
  * Etter aktiveringen av BankID vil kunden motta BankID-passord på e-post og kodebrikke i posten.
  * Etter dette kan kunden logge inn i nettbanken ved å benytte fødselsnummer, sikkerhetskode fra kodebrikken og personlig passord mottatt på e-post. Ved første gangs pålogging vil kunden få beskjed om å bytte passord til et nytt egendefinert passord. Hvis kunden trenger nytt førstegangspassord må de ringe kundesenteret.

* Tidslinje:
  * Det tar 4–8 virkedager fra bestillingen av legitimering (PUM) til legitimeringen kan gjennomføres hos postkontoret/post-i-butikk.
  * Kunden mottar et brev fra Storebrand med BankID-avtalen som må fylles ut, signeres og returneres til Storebrand. Dette brevet sendes til kunden samtidig med bestilling av legitimering (PUM).
  * Dersom kunden har sendt signert BankID-avtale til Storebrand og gjennomført legitimering hos postkontoret/post-i-butikk, tar det 1–2 virkedager fra kunden har vært på postkontoret til Storebrand kan aktivere BankID.
  * Da tar det ytterligere 2-4 virkedager fra aktivering av BankID før kunden mottar kodebrikke i posten og BankID-passord på e-post. Når dette er kommet frem til kunden kan første innlogging med BankID gjennomføres.

Detaljer om BankID

3\. Hva er BankID?

* BankID er en elektronisk legitimasjon og signatur som brukes på nett for sikker identifisering og signering.
* BankID kan brukes til:
  * Innlogging i nettbanker og offentlige sider.
  * Netthandel og signering av avtaler på nett.
* Fordeler:
  * Erstatter brukernavn, passord og kodebrikker.
  * Ingen behov for personlig oppmøte for signering.
* Merknad:
  * Én BankID er nok, og den kan brukes på tvers av alle banker.

4\. Hva kreves for å bestille BankID til deg selv?

* Følgende kriterier må oppfylles:
  * Du har en bankkonto i Storebrand Bank.
  * Du har fylt 18 år og har gyldig norsk fødsels- og personnummer.
  * Du må være legitimert med gyldig pass.
  * Du må ha mobilnummer og e-postadresse.

* Noen viktige tilleggspunkter:
  * Utenlandske statsborgere må ha norsk personnummer (NIN), et gyldig pass med RFID chip og tilleggsdokumentasjon f.eks. kopi av førerkort eller bekreftelse på tildelt fødselsnummer fra Skattetaten.
  * Førerkort og ID-kort godtas ikke som legitimasjon.
  * Utenlandske ID-kort godtas ikke.
  * Utenlandske pass uten RFID chip godtas ikke.

* Det er teknisk mulig å bestille BankID til deg selv med AI assistenten på Storebrand sin BankID-side, så lenge kriteriene over er oppfylt.

5\. Hva kreves for å bestille legitimering og BankID til mitt barn?

* Følgende kriterier må oppfylles:
  * Du er foresatt for barnet og har BankID fra før, enten fra Storebrand eller en annen bank.
    * Merk: Dette gjelder KUN for dine egne barn eller barn du er juridisk verge for.
  * Andre familiemedlemmer, kjæledyr eller bekjente kan ikke få legitimering eller BankID bestilt for seg.
  * Personer som ikke er dine barn (f.eks. ektefelle, partner, søsken, mor, far) må bestille BankID selv.
  * Du er bankkunde i Storebrand Bank.
  * For legitimering (første steg til BankID):
    * Barnet ditt er mellom 14-17 år og har gyldig norsk fødsels- og personnummer.
  * For BankID (andre steg til BankID):
    * Barnet ditt er mellom 15-17 år.
    * Barnet ditt må være legitimert med gyldig pass.
    * Barnet ditt har et mobilnummer og en e-postadresse.
  * Personer som har fylt 18 år må bestille BankID selv.

6\. Kan jeg bestille BankID til barn under 15 år?
* Nei, BankID kan kun bestilles for personer mellom 15-17 år.
* Dersom barnet ditt er under 15 år, må du vente til barnet har fylt 15 år før du kan bestille BankID.
* Personer som har fylt 18 år må bestille BankID selv.

6\. Når kan jeg bestille legitimering og BankID til mitt barn?
* Legitimering (første steg til BankID):
  * Du kan bestille legitimering når barnet ditt er mellom 14 og 17 år.
  * Dette er første steg for å få BankID.
* BankID (andre steg til BankID):
  * Du kan bestille BankID når barnet ditt har fylt 15 år og fram til 17-årsdagen.
  * Barnet må være legitimert før du kan bestille BankID.
* Personer som har fylt 18 år må bestille BankID selv.

BankID: Feilkoder og problemløsning

7\. Vanlige feilkoder og løsninger

* Feilkode BID 500a eller 5007:
  * Slett midlertidige internettfiler, lukk alle vinduer, og prøv på nytt.
  * Hvis feilen vedvarer, kontakt kundesenteret (chat eller ring).
* Feilkode BID 1118:
  * Slett midlertidige internettfiler og start nettleseren på nytt.
  * Hvis problemet vedvarer, restart modemet eller den trådløse ruteren.
* Feilkode 1299:
  * Slett midlertidige filer for Java på maskinen din.
* Feilkode BID 1437:
  * Sikre at riktig kodebrikke brukes, og les koden riktig.
  * Trykk på kodebrikken for en ny kode og prøv igjen.
* Feilkode BID 1439:
  * Tjenesten er sperret etter flere feil. Kontakt kundesenteret (chat eller ring).
* Feilkode BID 5000 (5001, 5002, 5003):
  * Lukk nettleseren, vent noen minutter, og prøv igjen.

Ekstra informasjon

8\. Hvordan sperre eller avslutte BankID?

* Sperring:
  * Sperr BankID selv i nettbanken, eller kontakt kundesenteret (chat eller ring).
  * Hvis kodebrikken er mistet, må denne sperres via kundesenteret (chat eller ring).
* Avslutning av kundeforhold:
  * BankID utstedt av Storebrand Bank opphører 14 dager etter kundeforholdet avsluttes.
  * Opprett et kundeforhold i ny bank og bestill BankID der før du avslutter forholdet hos Storebrand.

9\. BankID på mobil

* BankID på mobil fases gradvis ut fra høsten 2022.
* Kun app og kodebrikke vil være tilgjengelige alternativer fremover.

10\. Få ny kodebrikke
* For å få en ny kodebrikke må man ringe kundesenteret eller logge inn med BankID og starte en chat med en rådgiver.

11\. Hvordan kontakte kundesenteret?
* Ring kundesenteret på 915 08880 (hverdager kl. 9-16)
* Chat med kundesenteret (mandag-torsdag kl. 9-19, fredag kl. 9-18)
* Når kunden trenger å snakke med kundesenteret utenom åpningstid:
  - Foreslå at kunden starter en ny chat neste hverdag mellom kl. 9-19 (9-18 på fredager)
  - Eller ring kundesenteret neste hverdag mellom kl. 9-16

12\. Hva koster BankID?
* BankID er gratis å bestille og gratis å bruke.

13\. Hvorfor trenger du information om den andre forelderen?
* Informer at den andre forelderen vil motta en SMS for godkjenning bestillingen av BankID for barnet
