#
# **Inteligenta mobila system 2022**
#
#
#
# **Sprint Loggbok**
# **Namn:	John Appelberg**
# **Grupp:	1**
# **Roll:	Scrum Master av Inbyggda System teamet**
# **Datum:	2022-05-22**
# **Sprint: 	7**
# **Tid:	40h
#
# **Sammanfattning**
Gruppen har slitit in in slutet på att lösa att problem som har varit kvar. Dessa har bland annat varit mystiska problem med data som försvinner vid seriell kommunikation, kortsluten (potentiellt) kamera och Pi som betydde att mycket behövdes göras om gällande konfigurationer samt problem med BT i appen och annat för att slutföra projektet. Många timmar har lagts och gruppen har behövt jobba i overdrive men vi lyckades slutföra projektet.
# **Dag för dag**
*Måndag*

- Jag satt mycket med dokumentationen (SDD) samt kommentering i koden denna dag. Resten av gruppen satt med Pien och försöka lösa dom sista momenten.

*Tisdag*

- Fortsatt dokumentation och refactoring i koden för min del, och andra medlemmar fortsatte med dokumentation för Pien samt implementerade dom sista sakerna i Pien.

*Onsdag*

- Denna dag slutförde jag dokumentationen för Arduinon och gick sedan över till att hjälpa resterande medlemmar gällande Pien. Det var under denna dag som den seriella kommunikationen strulade. Det har fungerat klockrent tills nu men när man skickar längre meddelanden struntar Pien att ta emot all data. Vi ändrade därför baud-rate och började skicka kortare meddelanden.
 
*Torsdag*

- Vi löste först den seriella kommunikationen tillsammans och kände oss helt klara gällande Arduinon och Pien.
- Då skulle såklart kameran gå sönder och därmed kanske har skadat Pien. Dock, trodde vi att det var mjukvarufel och jobbade med fel sak för att försöka lösa problemet.
- Vi satt länge med att försöka lösa problemet för att alla medlemmar var samlade (från andra grupperna med) för att att göra system-test. Dock, gick inte detta pga. kameran och Piens defekta komponeneter.

*Fredag*

- Jag kom in till skolan vid ca. 14 och då hade flera andra redan jobbat sedan tidig morgon. Det var fortsatt felsökning gällande kameran och Bluetooth.
- Vid 22:00 hade jag och Eric tillsammans löst problemet med kameran och Bluetooth, i Arduinon, genom att byta till en annan Pi och kamera.
- App-teamet hade lyckats koppla till Pien en gång men inte mer än så.

*Lördag*

- Grupperna hade ett flertal möten under dagen för att hålla konstant kommunikation mellan medlemmarna då det är lite tid kvar.
- Tillslut fick Yevve och Alexander fungerande Bluetooth i appen och alla jublade. Vad detta betydde var att vi alla skulle samlas i skolan dagen efter för att knyta ihop hela projeket.

*Söndag*

- Jag, Alexander, Eric, Sargis (delvis), Yevve, Didrik och Filip samlades, vilket är dom mest aktiva i projektet, och löste dom sista problemet och utförde för första gången ett komplett systemtest där dom sista buggarna åtgärdades.
- Vi jobbade även med lessons learned och slutförde lite dokumentation och andra final touches.
- Ett flertal personer, inkl. mig själv, samlades även i Discord för att bocka av dom sista requirementsen vid 12-slaget. Nu kände sig alla klara och allt är redo för att lämnas över som klart.

# **Reflektioner** 
*Generellt*

😊	Känns bra att kunna slutföra projektet med ett fungerande system.

☹	Medlemmar har inte bidragit alls med det det som borde bidras med (Valentin, Killian) och några har harit frånvarande ofta (Sargis, Alexander) av olika anledningar. Detta gjorde att det knappt var möjligt att få ihop systemet och få allt fungerande då vi har jobbat dom timmarna som fattades från frånvarande medlemmar.

`  `**?**  	Blankt.
 
*Processen*

😊	Team-worken det senaste har varit grymt bra när alla visste att vi behövde jobba tillsammans och effektivt för att fixa det som var kvar.

☹	Tråkigt att så många inte dyker upp eller bidrar med det dom borde. Det borde ha deklareras tydliga regler i början.

`  `**?** 	Blankt.

*Teamet*

😊	Dom som har varit aktiva, har jobbat på grymt bra.

☹	Dom som inte har varit aktiva, förtjänar inte det som dom som har varit aktiva förtjänar.

`  `**?** 	Blankt.

**Sprint 7 – John Appelberg	Sida | 1	2022-05-22**
