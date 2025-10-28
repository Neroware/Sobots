# Vorgehen Ontologie:

## Schritt 1: Social Robots
- Definition "SocialRobot" als AutonomousAgent (trivial)
- Definition "NaturalRobot" als PhysicalAgent (trivial)

## Schritt 2: Identifikation dimensionaler Räume
Nicht alle Kategorien in Ninas Taxonomie sind dimensionale Räume (Regions). Ein dimensionaler Raum wären z.B. die Kategorien der Interaktionsdauer. Auch in der Benutzerzielgruppe wäre das Alter eine Region, aber diese konkrete Kategorie wird gestört durch Begriffe wie "Laien" oder "Mitarbeitende". Tatsächlich ist der Bildungsgrad gegenüber Robotern auch eine Region...
In diesem Schritt gehe ich durch und identifiziere die dimensionale Räume, welche Nina in ihrer Taxonomie explizit oder implizit erschlossen hat.

### Nutzungskontext
Beobachtung: Das Exlusivitätskriterium liefert guten Aufschluss, ob die Kategorie eine Region ist. Leider wurden auch hier Fehler gemacht: Der Anwendungsbereich z.B. muss nicht exklusiv sein und ist eindeutig keine Region...

- Alter der Benutzerzielgruppe (Hinzugefügt durch AgeRegion und AgeInYears)
- Erfahrungsgrad der Benutzerzielgruppe (exisitiert bereits in SOHO als ExpertiseLevelScale)
- Physische Nähe (realisiert durch PhysicalCloseness)
- Mensch-zu-Roboter-Verhältnis (Definiert durch RatioRegion -> HumanToRobotRatio)

### Interaktionszeit

Hier sind alle drei Kategorien auch eine Region, Zeiträume sind klassischerweise dimensionale Räume

### Roboter

- Menschenähnlichkeit (dimensionaler Raum, aber Vermischung mit anderem Konzept, siehe: zoomorph vs. technisch)
- Robotertyp: Widerspreche, ein professioneller Serviceroboter kann auch medizinische Dienste verrichten! => KEINE Region!
- Art der Interaktion: Das kann ich Stand jetzt noch nicht einordnen...

### Interaktivität
=> Keine Regionen!

### Intelligenz
- Autonomie: Klare Region durch Vektorraum der Autonomiegrade (exisitiert bereits in SOHO)
- Adaptivität schwer, sollte auch eine Region sein, aber die Kategorien ergeben keinen Sinn für mich als dimensionaler Raum, stattdessen wirken sie eher wie Qualitäten, also ein Roboter hat die Qualität emotionaler Adaptivität...

## Schritt 3: Der Nutzungskontext

Der Nutzungskontext ist ein Zustand und somit per Definition von SOHO ein Event.
=> ContextOfUse erbt soho:Event
=> ApplicationArea erbt ContextOfUse
=> InteractionPartners erbt ContextOfUse
=> TargetGroup erbt ContextOfUse
=> TaskContext erbt ContextOfUse

Interaktionspartner sind ein Zustand im Kontext, allerdings verstehe ich nicht wie "Umwelt" hier passt...
! Tiere sind auch Teil der Umwelt
! Wie soll das mit der Anzahl passen? 1 Umwelt zu N Menschen...? Das passt irgendwie linguistisch nicht...
! Ich glaube, ich hatte diesen Punkt bereits angebracht... Wen du auf das Label bestehst, kann man es nachträglich noch als Unterklasse von InteractionPartners einfügen...
=> Wir schließen Umwelt zunächst aus, da es ein anderes Konzept ist, und in SOHO bereits an anderer Stelle enthalten.

## Schritt 4: Identifikation der Qualitäten eines Roboters

Während Regionen nur als dimensionale Wertemengen bzw. zur Kodierung einer Qualität dienen, sind Letztere Aspekte einer Entität, wobei Qualitäten nicht alleine exisitieren können, aber auch kein Teil der Entität sind. Die dimensionalen Räume basierend auf der Taxonomie wurden bereits in Sobots eingefügt, nun hat das gleiche mit den Eigenschaften zu erfolgen.

-> Definition: HumanProperty und SocialRobotProperty als Äquivalenzklassen mit trivialen Regeln

- Erscheinungsform: Die Erscheinungsform ist eine klare Qualität eines Agenten. Basierend auf den Angaben der Taxonomie habe ich entsprechend Regionen für die 'Menschenähnlichkeit' und die 'Tierähnlichkeit' definiert. Beide Vektorräume starten dabei vom Ursprung 'PurelyTechnical'.
