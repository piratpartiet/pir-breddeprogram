Breddeprogram for Piratpartiet Norge
====================================

Dette er de offisielle breddeprogram-filene for Piratpartiet Norge. 
Teksten skrives i MarkDown som kan konverteres til andre formater, for 
eksempel XHTML som limes inn på <http://piratpartiet.no> eller 
<http://wiki.piratpartiet.no>.

Bruk av GitHub
--------------

`master`-branchen i <http://github.com/piratpartiet/breddeprogram> er 
stabil. Ingen forandringer skal gå direkte inn der uten at forandringen 
er sett over og godkjent av minst ett annet medlem i 
[Programbanden](http://wiki.piratpartiet.no/index.php?title=Programbanden). 
Dette er for å unngå at feil forandringer introduseres i den stabile 
versjonen. Pullrequester kan brukes, eller man kan henvise til branchen 
i sin egen private klone.

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

----

    vim: set ft=markdom fenc=utf-8 fo=tcqnw :
