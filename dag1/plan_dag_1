
# Kursbeskrivelse – Del 1 av 3: Grunnleggende installasjon og oppsett av Drupal

I den første delen av kurset får du en praktisk introduksjon til **Drupal**, et fleksibelt og kraftig **CMS (Content Management System)** som brukes til alt fra enkle nettsteder til komplekse portaler og digitale plattformer.  

Vi starter med de helt grunnleggende trinnene: hva et CMS er, hvorfor Drupal er et godt valg, og hvordan du raskt kan komme i gang med installasjon og oppsett. Kurset passer for deg som er nysgjerrig på Drupal, enten du er utvikler, designer, redaktør eller bare ønsker å lære mer om hvordan man kan bygge og administrere et moderne nettsted.  

---

## Innhold i del 1
- Hva er et CMS, og hvorfor bruke **[Drupal](https://www.drupal.org/)**?  
- Drupal-økosystemet: moduler, temaer, distribusjoner og fellesskapet  
- Installere Drupal lokalt med **DDEV**  
- Administrasjonsgrensesnittet – en omvisning  
- Opprette innhold og bruke innholdstyper  

---

## Øvelse: Installer Drupal og lag en enkel nettside

Denne øvelsen gir deg praktisk erfaring med hvordan du setter opp et Drupal-prosjekt lokalt ved hjelp av **DDEV**.  
Du kan velge mellom å installere **vanlig Drupal 10** eller den ferdig sammensatte **Drupal CMS-distribusjonen**.  

### 1. Klargjør maskinen din
- På **Windows (WSL2)**:  
  Følg guiden for å installere WSL2, Docker Desktop og DDEV (se egen fil).  
- På **macOS**:  
  Installer Docker Desktop og DDEV via Homebrew.  

Test at alt fungerer med:  
    ddev version


### 2. Lag et nytt prosjekt
Velg en mappe der du vil ha prosjektet ditt, og kjør:  
    mkdir drupal-kurs
    cd drupal-kurs
    ddev config // følg instruksjonene på skjermen


---

### 3A. Alternativ 1: Installer Drupal 11 (vanilla) 
https://www.drupal.org/docs/develop/using-composer/manage-dependencies

    ddev start
    ddev composer create "drupal/recommended-project" .
    


### 3B. Alternativ 2: Installer Drupal CMS
Drupal CMS er en ferdig tilpasset distribusjon av Drupal med nyttige moduler, temaer og verktøy som gir deg et komplett CMS rett ut av boksen.  
Mer info: [Drupal CMS](https://new.drupal.org/drupal-cms/launcher)  

Installer med:  
    ddev start
    ddev composer create drupal-cms/drupal-cms-project:11.x-dev .



### 4. Installer nettstedet
Når installasjonen er ferdig, åpne Drupal i nettleseren:  
    ddev launch

Følg installasjonsveiviseren for å sette opp nettstedet ditt.  

---

### 5. Logg inn og opprett innhold
- Gå til `/user/login` og logg inn med brukeren du opprettet under installasjonen.  
- Opprett en ny **artikkel** eller **side** via menyen *Innhold → Legg til innhold*.  

---

## Praktisk informasjon
- Husk å ta med egen datamaskin.  
- Det er en stor fordel om du har installert DDEV på forhånd – se instruksjonene ovenfor.  
- Det er begrenset med plasser på kurset, så meld deg på tidlig.  

---

## Nyttige ressurser
- Offisiell Drupal-side: [drupal.org](https://www.drupal.org/)  
- Drupal CMS: [Drupal CMS launcher](https://new.drupal.org/drupal-cms/launcher)  
- Community og ressurser: [DrupalForge](https://drupalforge.com/)  
