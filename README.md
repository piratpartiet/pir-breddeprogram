Breddeprogram for Piratpartiet Norge
====================================

Dette er de offisielle breddeprogram-filene for Piratpartiet Norge. 
Teksten skrives i MarkDown som kan konverteres til andre formater, for 
eksempel XHTML som limes inn på <http://piratpartiet.no> eller 
<http://wiki.piratpartiet.no>.

Bruk av Git og GitHub
---------------------

Mange foretrekker å skrive i Etherpad Lite («padden») eller på wikien, 
men de offisielle filene lagres i [Git](http://git-scm.com) for å ha 
fullstendig kontroll over hva som går inn i programmet. Git-repoen 
lagres på GitHub i <https://github.com/piratpartiet/pir-breddeprogram> 
(heretter kalt «hovedrepoen»). Denne repoen bør ikke pushes til direkte, 
men lag din egen fork (kopi av repoen) ved å trykke «Fork» som er oppe 
til høyre på GitHub-siden. For at du skal kunne gjøre dette, må du være 
registrert på GitHub.

Git er distribuert, så folk som ikke vil bruke GitHub kan derfor lagre 
repoen sin andre steder. For å ha best mulig oversikt over hva som skjer 
i `pir-breddeprogram.git` vil det enkleste være om vi konsentrerer 
aktiviteten på GitHub, men har du noe spesielt mot GitHub, er det 
selvfølgelig ingen tvang.

### Forslag til forandringer og påpeking av feil

Hvis du finner en feil eller har forslag til forandringer, er den beste 
måten å lage en pullrequest på GitHub der du selv har rettet feilen i 
Git. Hvis du ikke bruker Git, kan du istedenfor legge inn en issue (en 
post i issue-trackeren på GitHub) som beskriver feilen eller 
forandringene. Dette er for å samle alt dette på en plass og unngå at 
nye forslag går i glemmeboken. Diskusjoner omkring de enkelte forslagene 
kan foregå direkte i issue-trackeren under den relevante posten. Alle 
som har registrert seg på GitHub kan bidra til diskusjonen.

Et forslag som enda ikke er behandlet ligger som en «åpen» (open) issue. 
Når forandringen er vedtatt (godkjent eller refusert) og eventuelt lagt 
inn i repoen, forandres statusen til «lukket» (closed) og listes ikke ut 
sammen med de som ligger på vent.

Issue-trackeren for breddeprogrammet ligger på 
<https://github.com/piratpartiet/pir-breddeprogram/issues>.

### Brancher

`master`-branchen i <https://github.com/piratpartiet/pir-breddeprogram> 
er stabil. Ingen forandringer skal gå direkte inn der uten at 
forandringen er sett over og godkjent av minst ett annet medlem i 
[Programbanden](http://wiki.piratpartiet.no/index.php?title=Programbanden). 
Dette er for å unngå at feil forandringer introduseres i den stabile 
versjonen. Pullrequester kan brukes, eller man kan henvise til branchen 
i sin egen private klone.

Nye forandringer skjer på egne brancher i din egen kopi av hovedrepoen. 
Branchen der forandringene ligger bør kalles noe annet enn `master`. 
Bruk et beskrivende navn, for eksempel `skrivefeil-rettinger`, 
`readme-forandringer`, `nytt-punkt-om-utdanning` og så videre. Hvis 
klonen av hovedrepoen ligger på GitHub, kan alle se på aktiviteten i 
alle nye brancher ved å gå inn på 
«[Network](https://github.com/piratpartiet/pir-breddeprogram/network)» 
på GitHub-siden.

### Godkjenning av forandringer

Ofte ser man ikke selv at det er noe feil med forandringene man har 
gjort. Det kan for eksempel være skrivefeil man tror er riktige, eller 
feil i MarkDown-syntaksen. Dette kan unngås ved at minst en annen i 
Programbanden ser over de nye forandringene før de legges inn på 
`master`.

For å holde oversikten over hvem som har sett over forandringene på 
branchen, legger kontrolløren inn en kommentar på pullrequesten om at 
den er i orden og dermed kan legges inn, eventuelt hva som er feil med 
den og den dermed må tas på nytt.

Hvis det ikke er laget pullrequest på den, men at branchen ligger 
tilgjengelig for eksempel på andre plasser enn GitHub og det dermed ikke 
kan lages pullrequest, må en linje av denne typen legges inn på slutten 
av loggmeldinga i commiten:

    Reviewed-by: Navn Etternavn <email@example.com>

der navn og email legges inn. Dette er for å eventuelt kunne gå tilbake 
i historien for å se hvem som har lagt inn og godkjent forandringen. De 
som gidder, kan også legge inn en

    Signed-off-by: Navn Etternavn <email@example.com>

på slutten av loggmeldinga.

### Kun en forandring per commit

Når du legger inn forandringer i Git, legg kun en forandring inn i hver 
commit. Urelaterte forandringer bør legges inn i forskjellige commits. 
For eksempel, hvis du skal legge inn en forandring som retter 
skrivefeil, legger til ny tekst og i tillegg ordner på for eksempel 
`.mailmap`, bør forandringene splittes opp i tre commits: En for alle 
skrivefeilene, en for den nye teksten og en for 
`.mailmap`-forandringene. Dette gjør det enklere å kontrollere 
forandringene, og hvis en commit må reverteres på et senere tidspunkt, 
blir kun relaterte forandringer tilbakesatt.

### Lag en god loggmelding

Den vanlige konvensjonen for loggmeldinger i Git er som følger:

1. En linje på toppen som beskriver forandringen i korte trekk, helst 
   under 50 tegn, unngå å gå over 72 tegn på denne linjen. Denne linjen 
   listes i commit-oversikter og er ment å være et kort sammendrag over 
   hva commiten inneholder. Hvis du synes det er vanskelig å beskrive 
   hva commiten inneholder i så korte ordelag, tyder dette på at 
   commiten inneholder forandringer som ikke er relaterte og dermed må 
   splittes opp.
2. En etterfølgende tom linje.
3. Hvis det er mer å si om forandringen i tillegg til linjen på toppen, 
   legges det inn under den tomme linjen. Bruk linjebryting, 72 tegn per 
   linje. Ikke skriv alt inn på en lang linje, dette gjør det tungvint å 
   lese loggmeldingen i ettertid.

### Men hvorfor må vi være så nøye på disse reglene?

Tre ord: Orden i sysakene. Filene som ligger på `master`-branchen er de 
_offisielle_ filene for Piratpartiet Norge. Ingen feil skal introduseres 
der, og branchen skal til enhver tid være i tipp-topp stand. Under 
arbeidet skal vi kunne henvise medlemmer, presse og andre interesserte 
til GitHub hvor arbeidet foregår. Det tar seg derfor dårlig ut hvis 
teksten er skjemmet av skrivefeil, dårlig språk eller direkte feil 
informasjon.

Det som er listet opp her, er helt grunnleggende «god praksis» ved bruk 
av Git. Brudd på denne praksisen medfører ikke nødvendigvis kjølhaling, 
men at forandringene blir refusert og at du dermed må forandre på 
feilene som er påpeket. Men det å introdusere feil i `master`-branchen i 
hovedrepoen på <https://github.com/piratpartiet/pir-breddeprogram> er en 
annen historie. Det skal _ikke_ forekomme og er som oftest et tegn på at 
konvensjonene er brutt, for eksempel at forandringer er pushet direkte 
til repoen uten at noen andre har sett over dem. Alle kan gjøre feil, 
men alvorlige eller gjentatte brudd på disse konvensjonene som fører til 
at `master` i hovedrepoen blir forurenset, kan føre til degradering/tap 
av pushrettigheter i hovedrepoen. Selv om dette skulle skje, vil man 
fortsatt kunne lage sin egen klone av `pir-breddeprogram.git` og lage en 
pullrequest eller post i issue-trackeren.

Men la ikke disse småstrenge reglene forhindre deg fra å delta i 
arbeidet med breddeprogrammet! Reglene gjelder kun for bruk av Git og 
når nye forandringer skal legges inn i hovedrepoen. Hvis du vil, kan du 
bidra på wikien eller padden. Disse stedene kontrolleres jevnlig for nye 
forandringer og blir etterhvert lagt inn i hovedrepoen for 
breddeprogrammet.

----

    vim: set ft=markdown fenc=utf-8 fo=tcqnw :
