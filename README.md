# Data-oplossing voor CRUNCHR Airlines - Piloten Tekort
Dit is de repository met de data-oplossing voor het businessprobleem van CRUNCHR Airlines: het tekort aan piloten. Deze oplossing bevat verschillende notebooks die de data-analyse, machine learning-modellen en voorspellingen documenteren en toelichten. Door deze opzet is het onderzoek reproduceerbaar en kan de analyse eenvoudig worden herhaald of verder worden uitgebreid.

# Inhoud van de Repository
Piloten.ipynb
In dit notebook wordt de eerste verkenning van de data uitgevoerd. Het bevat een uitgebreide data-exploratie, statistische analyse en visualisaties specifiek gericht op de pilotenpopulatie binnen CRUNCHR Airlines. Dit notebook biedt inzicht in de trends en patronen die relevant zijn voor het businessprobleem. Daarnaast worden datacleaning- en balancingtechnieken toegepast om de data klaar te maken voor verdere analyses.

KNN.ipynb
Dit notebook demonstreert het gebruik van het K-Nearest Neighbours (KNN) model op de piloten data. Het doel van dit model is om te laten zien dat machine learning-technieken succesvol kunnen worden toegepast op de CRUNCHR data. Het model geeft inzicht in hoe vergelijkbare datasets met elkaar in verband staan en biedt een basis voor verdere toepassingen van machine learning-algoritmes binnen de organisatie.

Regressiemodellen.ipynb
In dit notebook worden verschillende regressiemodellen toegepast op de CRUNCHR data om nauwkeurige voorspellingen te doen over het aantal piloten in de toekomst. Elk model wordt geëvalueerd op basis van de prestaties, waarbij metingen zoals de gemiddelde absolute afwijking en de R²-score worden gebruikt om de modellen te vergelijken en het meest geschikte model te selecteren.

Voorspelde_leavers.ipynb
Dit notebook berekent voor elke maand per medewerker hoeveel maanden het duurt voordat zij de organisatie verlaten. Een DecisionTreeRegressor is getraind op de data van vertrokken werknemers, met het doel om dit model toe te passen op medewerkers die nog bij de organisatie zijn. Het notebook bevat een toelichting op de keuze voor de DecisionTreeRegressor, evenals een analyse met behulp van SHAP-waarden om de invloed van variabelen op de uitkomst van het model te begrijpen. Daarnaast wordt de keuze voor SHAP boven de LIME-methode toegelicht.


# Reproduceerbaarheid
Om deze analyse te reproduceren, volg de onderstaande stappen:

Clone de repository
Clone deze repository naar je lokale machine:

bash
Code kopiëren
git clone https://github.com/gebruikersnaam/Data-oplossing-CRUNCHR-Airlines.git
cd Data-oplossing-CRUNCHR-Airlines
Installeer de vereiste packages
Zorg dat je een virtuele omgeving hebt en installeer alle benodigde packages door de requirements.txt file te gebruiken (indien beschikbaar). Een voorbeeld om de packages te installeren:

bash
Code kopiëren
pip install -r requirements.txt

Als er geen requirements.txt is, zorg dan dat je Python-gebruikelijke data science packages hebt geïnstalleerd, zoals:

pandas
numpy
scikit-learn
matplotlib
seaborn
shap (indien je de SHAP-analyse wilt uitvoeren)
Open en voer de notebooks uit
Open de notebooks in Jupyter Notebook of JupyterLab en voer ze stap voor stap uit. Dit zorgt ervoor dat alle analyses en modellen opnieuw worden berekend, wat de reproduceerbaarheid waarborgt.

# Conclusies en Advies
Op basis van de analyse in de verschillende notebooks concluderen we dat het piloten tekort een urgent probleem is dat in de toekomst waarschijnlijk zal verergeren zonder interventie. De voorspellingen laten zien dat er een aanzienlijke daling in het pilotenbestand wordt verwacht. Daarom adviseren we verder onderzoek naar wervingsstrategieën en het ontwikkelen van retentieplannen om het verwachte tekort aan te pakken.
