//Dokumentation zur Erstellung der KPI-Indikator Pfeilen in PowerBi 

//1. Messurement erstellen mit der Bennenung "Arrow-UP" 
//Code: ArrowUp.txt

//2. Messurement erstellen mit der Benneung "Arrow-Down"
//Code: ArrowDown.txt

3. Messurement erstellen mit der Bennung "KPI"
//Code:
KPI = IF( CALCULATE(
    SUM(Value1)) > SUM(Value2), [ArrowUP], [ArrowDown])
//SUM wird nur benötigt wenn Wert als Summe ∑ angebgen ist 

4. Visual mit der Bezeichnung "Image Pro by Cloud Scope" verwenden und KPI als Source angeben 

