# Die "Menschen hinter der Stelle" Philosophie

## Das Problem

Traditionelle Recruiting-Prozesse reduzieren Menschen auf Keywords und Jahre Erfahrung. Eine Stellenausschreibung mit "10 Jahre Java-Erfahrung" schliesst automatisch talentierte Entwickler aus, die vielleicht nur 8 Jahre haben aber außergewöhnliche Fähigkeiten mitbringen.

## Unsere Lösung

RecruitingDecidor macht sichtbar, WER wirklich hinter einer Stellenausschreibung steht:

### Konkrete Menschen statt abstrakte Zielgruppen

Statt: "Senior Developer gesucht"
Erhalten Sie: "Diese Stelle spricht Thomas (42) an, der nach Stabilität sucht, aber schließt Maria (28) aus, die innovativ arbeiten möchte"

### Datenbasierte Personas

Unsere AI-generierten Personas basieren auf:
- Realen Arbeitsmarktdaten
- Psychologischen Profilen
- Demografischen Statistiken
- Kulturellen Faktoren

### Transparenz für bessere Entscheidungen

Unternehmen sehen:
- WEN sie mit ihrer Ausschreibung erreichen
- WEN sie unbeabsichtigt ausschließen
- WIE kleine Anpassungen den Talent-Pool erweitern können

## Technische Umsetzung der Vision

```javascript
// Vereinfachtes Konzept
const analyzeJobPosting = (posting) => {
  // Phase 1: Was steht in der Ausschreibung?
  const requirements = extractRequirements(posting);
  const culture = analyzeCulture(posting);
  const psychology = extractPsychologicalProfile(posting);
  
  // Phase 2: Wer passt dazu?
  const personas = generatePersonas({
    requirements,
    culture,
    psychology,
    marketData: swissLaborMarket
  });
  
  return {
    reached: personas.attracted,
    excluded: personas.filtered_out,
    improvements: suggestOptimizations()
  };
};
```

## Impact

Durch diese Transparenz können Unternehmen:
- Unbewusste Biases erkennen
- Talent-Pools erweitern
- Inklusivere Stellenausschreibungen erstellen
- Bessere Matches erzielen

## Die Zukunft

Wir glauben an eine Zukunft, in der Recruiting nicht mehr über das Aussieben von Menschen funktioniert, sondern über das Verstehen und Einbeziehen ihrer einzigartigen Stärken.