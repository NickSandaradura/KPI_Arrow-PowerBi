Dokumentation zur Erstellung der KPI-Indikator Pfeilen in PowerBI
Diese Anleitung beschreibt die Erstellung und Visualisierung von KPI-Indikator Pfeilen in PowerBI. Wir verwenden dazu die Messwerte "Arrow-Up" und "Arrow-Down" und visualisieren das Ergebnis mit dem Visual "Image Pro by Cloud Scope".

1. Erstellung des Messwerts "Arrow-UP"
Erstellen Sie einen neuen Messwert mit dem Namen "Arrow-UP". Dieser Messwert sollte den Pfad oder die URL zu einem Bild des aufwärts zeigenden Pfeils enthalten.

dax
Code kopieren
Arrow-UP = "URL_ZU_IHREM_AUFWÄRTS_PFEIL_BILD"
2. Erstellung des Messwerts "Arrow-Down"
Erstellen Sie einen neuen Messwert mit dem Namen "Arrow-Down". Dieser Messwert sollte den Pfad oder die URL zu einem Bild des abwärts zeigenden Pfeils enthalten.

dax
Code kopieren
Arrow-Down = "URL_ZU_IHREM_ABWÄRTS_PFEIL_BILD"
3. Erstellung des Messwerts "KPI"
Erstellen Sie einen neuen Messwert mit dem Namen "KPI". Dieser Messwert vergleicht die Werte von Value1 und Value2 und verwendet den entsprechenden Pfeil.

dax
Code kopieren
KPI = IF(
    CALCULATE(SUM(Value1)) > SUM(Value2), 
    [Arrow-UP], 
    [Arrow-Down]
)
// Hinweis: SUM wird nur benötigt, wenn die Werte als Summe angegeben sind.
4. Visualisierung des KPIs
Verwenden Sie das Visual "Image Pro by Cloud Scope", um die KPI-Indikatoren zu visualisieren.

Fügen Sie das Visual "Image Pro by Cloud Scope" zu Ihrem Bericht hinzu.
Ziehen Sie den Messwert "KPI" in das Feld "Image URL" des Visuals.
Passen Sie das Design des Visuals an, um das gewünschte Erscheinungsbild zu erreichen. Nutzen Sie die "GitHub Basic ReadMe" Vorlage für das Design.
Beispiel für die Anpassung des Designs
Sie können die Farben, Schriftarten und andere Design-Elemente nach Ihren Bedürfnissen anpassen. Hier ist ein Beispiel für eine grundlegende Anpassung im GitHub Basic ReadMe Stil:

Hintergrundfarbe: Weiß
Rahmenfarbe: Schwarz
Schriftart: Consolas, 12pt
Pfeilgröße: 32x32px
Fertig! Ihr KPI-Indikator Pfeil Visual sollte jetzt korrekt angezeigt werden und die KPI-Messung entsprechend der Vergleichswerte Value1 und Value2 visualisieren.

Zusammenfassung
Mit dieser Anleitung können Sie in PowerBI visuelle Indikatoren für KPIs erstellen, die die Performance Ihrer Kennzahlen anhand von auf- oder abwärts zeigenden Pfeilen darstellen. Nutzen Sie das Visual "Image Pro by Cloud Scope" und passen Sie das Design nach Ihren Anforderungen an, um aussagekräftige und ansprechende Dashboards zu erstellen.
