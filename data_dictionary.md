# Data Dictionary - CRUNCHR Airlines Piloten Data

## Algemene Informatie

Dit bestand beschrijft de belangrijkste variabelen in de dataset die is gebruikt voor het analyseren van het pilotenbestand en het voorspellen van gegevens binnen CRUNCHR Airlines. De variabelen zijn afkomstig uit verschillende notebooks waarin visualisaties, regressiemodellen en machine learning-algoritmes zijn toegepast om het verloop en de kosten van piloten in kaart te brengen.

---

## Beschrijving van de Variabelen

| Variabele                  | Type       | Beschrijving                                                                                               |
|----------------------------|------------|-----------------------------------------------------------------------------------------------------------|
| **Age**                    | Integer    | De leeftijd van de piloot in jaren. Gebruikt voor correlatieanalyses met salaris en andere factoren.       |
| **Base pay (full-time)**   | Float      | Het basissalaris van een piloot bij een voltijdbaan. Gebruikt voor regressie en voorspelling.              |
| **Base pay (part-time)**   | Float      | Het basissalaris van een piloot bij een deeltijdbaan.                                                     |
| **Cost of Employment (TCOE)** | Float   | Totale kosten voor het in dienst hebben van een piloot. Wordt gebruikt voor correlaties met basissalaris. |
| **Direct span**            | Integer    | Direct leidinggevende span (aantal direct rapporterende medewerkers).                                     |
| **Employee engagement**    | Float      | Engagementscore van de piloot, gebruikt om het verband met verloren werkdagen (ziekteverzuim) te analyseren. |
| **Employee grade**         | Integer    | Niveau of rang van de piloot binnen de organisatie.                                                       |
| **Expenses**               | Float      | Maandelijkse uitgaven van de piloot.                                                                      |
| **Expenses (in original currency)** | Float | Uitgaven in de oorspronkelijke valuta.                                                                    |
| **Family related leave**   | Integer    | Aantal dagen verlof gerelateerd aan familieomstandigheden.                                                |
| **FTE**                    | Float      | Full-time equivalent, geeft de werktijd aan in verhouding tot een voltijdse baan.                         |
| **Intent to Leave**        | Boolean    | Indicatie of een piloot van plan is om de organisatie te verlaten.                                        |
| **Is hire**                | Boolean    | Indicatie of de piloot recentelijk is aangenomen.                                                         |
| **Is leaver**              | Boolean    | Indicatie of de piloot de organisatie heeft verlaten.                                                     |
| **Lost working days**      | Integer    | Aantal verloren werkdagen door ziekte of verlof.                                                          |
| **Monthly fly hours**      | Float      | Aantal vlieguren per maand.                                                                               |
| **Overtime**               | Float      | Aantal overuren.                                                                                          |
| **Position grade**         | Integer    | Functie- of positie niveau van de piloot.                                                                 |
| **Recruitment cost**       | Float      | Kosten voor het werven van een piloot.                                                                    |
| **Relative salary position** | Float    | Salarispositie van de piloot in verhouding tot anderen in dezelfde functie.                               |
| **Reporting layer**        | Integer    | Het rapportageniveau in de organisatie.                                                                   |
| **Sales revenue**          | Float      | Omzet gegenereerd door de piloot (indirecte metriek).                                                     |
| **Skill match**            | Float      | Mate waarin de vaardigheden van de piloot aansluiten bij de functie-eisen.                                |
| **Target bonus**           | Float      | Doelbonus voor de piloot.                                                                                 |
| **Time to demotion**       | Integer    | Tijd (in maanden) tot een eventuele degradatie.                                                           |
| **Time to fill**           | Integer    | Tijd (in maanden) die nodig is om een openstaande positie in te vullen.                                   |
| **Time to hire**           | Integer    | Tijd (in maanden) die nodig is om een piloot aan te nemen.                                                |
| **Time to lateral move**   | Integer    | Tijd tot een zijwaartse stap binnen de organisatie mogelijk is.                                           |
| **Time to promotion**      | Integer    | Tijd (in maanden) tot een mogelijke promotie.                                                             |
| **Years in position**      | Integer    | Aantal jaren in de huidige functie.                                                                       |
| **Years of service**       | Integer    | Aantal jaren dat de piloot in dienst is bij de organisatie.                                               |

---

## Enkele gebruikte Visualisaties en Modellen

1. **Correlatiematrix**:
   - Toont de correlatie tussen verschillende variabelen, waaronder salaris, leeftijd, uitgaven, etc.
   - Helpt om sterk gecorreleerde variabelen te identificeren voor verdere analyse.

2. **Scatter Plot - Leeftijd vs. Salaris**:
   - Visualiseert de relatie tussen leeftijd (`Age`) en voltijds basissalaris (`Base pay (full-time)`).
   - Geeft inzicht in trends tussen ervaring (leeftijd) en compensatie.

3. **Regressiemodellen**:
   - Verschillende regressiemodellen zijn toegepast om het basissalaris te voorspellen op basis van variabelen zoals:
     - **Base pay (part-time)** vs. **Base pay (full-time)**
     - **Cost of Employment (TCOE)** vs. **Base pay (full-time)**
     - **Exchange rate** vs. **Base pay (full-time)**
     - **Position grade** vs. **Base pay (full-time)**

4. **SHAP-waarden**:
   - Gebruikt om de invloed van verschillende kenmerken op voorspellingen in machine learning-modellen te evalueren.
   - Belangrijke kenmerken volgens SHAP: `Years in position`, `Years of service`, `Expenses`, `Local base pay (full-time)`, etc.

5. **K-Nearest Neighbour (KNN) Model**:
   - Toegepast op pilootgegevens om een relatie te vinden tussen functiegraad, leeftijd, dienstjaren en basissalaris.
   - Model geëvalueerd met Mean Squared Error (MSE) en R²-score om de nauwkeurigheid van de voorspellingen te beoordelen.
