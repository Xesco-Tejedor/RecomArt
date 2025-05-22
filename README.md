
---

## 💡 La Motivació: Per Què?

Navegar entre el catàleg d'art i el catàleg de la biblioteca pot requerir obrir múltiples pestanyes i repetir cerques. La idea és **estalviar temps** i **fomentar la descoberta** de recursos complementaris de manera més fluida. Encara que la integració ideal no és possible amb aquesta eina simple, vol ser un **ajudant pràctic**.

---

## 🚀 On Hem Arribat (Estat Actual)

*   Una pàgina HTML (`.html`) autocontinguda i funcional.
*   Interfície minimalista en català.
*   Ús de JavaScript bàsic (`Vanilla JS`) per:
    *   Capturar el terme de cerca.
    *   Construir les URLs de cerca adequades per a cada catàleg (basades en l'observació de les URLs públiques).
    *   Obrir els resultats en noves pestanyes (`window.open()`).
*   Cap dependència externa ni necessitat de servidor.

**Tecnologies:** `HTML5`, `CSS3`, `JavaScript (ES6+)`

---

## 🛠️ Com Utilitzar-ho

1.  Clona aquest repositori o descarrega l'arxiu `.html` principal (p. ex., `recomart.html`).
2.  Obre l'arxiu `.html` directament amb el teu navegador web preferit (Chrome, Firefox, Safari, Edge...).
3.  Introdueix el teu terme de cerca al camp de text.
4.  Fes clic al botó "Cerca..."
5.  *Voilà!* S'obriran dues noves pestanyes amb els resultats.

---

## 🚧 El Repte: Les Limitacions Actuals

Aquesta eina és un **facilitador**, no un **integrador**. L'ideal seria mostrar els llibres recomanats *dins* de la mateixa pàgina de resultats de l'obra d'art. Malauradament, això **no és possible** amb aquesta aproximació simple per diverses raons tècniques fonamentals:

1.  **Restriccions de Seguretat del Navegador (CORS):** Els navegadors impedeixen que una pàgina web (com aquesta eina) faci peticions directes per obtenir dades d'un altre domini (com el catàleg de la biblioteca) si aquest últim no ho permet explícitament mitjançant capçaleres CORS. És molt poc probable que els catàlegs del MNAC estiguin configurats per permetre això des de qualsevol origen.
2.  **Absència d'APIs Públiques:** La manera ideal de fer una integració seria a través d'APIs (Interfícies de Programació d'Aplicacions) que oferissin els catàlegs. Aquestes permetrien consultar i rebre dades de forma estructurada (p. ex., JSON). Actualment, no sembla haver-hi APIs públiques documentades per a aquests serveis.
3.  **Fragilitat del Web Scraping:** Intentar extreure dades directament de l'HTML de les pàgines de resultats ("web scraping") des del navegador seria bloquejat per CORS i, a més, qualsevol canvi, per petit que fos, en l'estructura HTML de les pàgines originals trencaria la nostra eina.

---

## ✨ La Visió: On Voldríem Arribar

Tot i les limitacions actuals, la visió ideal de RecomArt (o una funcionalitat similar integrada oficialment pel museu) seria:

*   **✅ Integració Real:** Mentre navegues per una obra al catàleg d'art online, veure directament una secció "Llibres relacionats a la biblioteca" amb títols, autors i enllaços directes.
*   **🧠 Recomanacions Intel·ligents:** Anar més enllà de la simple coincidència de paraules clau. Utilitzar metadades enriquides (autor, època, estil, temàtica de l'obra) per suggerir lectures realment rellevants i contextualitzades.
*   **📊 Disponibilitat en Temps Real:** Indicar si els llibres suggerits estan actualment disponibles per a préstec o consulta a sala a la biblioteca.
*   **🔌 (Idealment) Basat en APIs:** Que el museu desenvolupés i oferís APIs públiques (o internes segures) per als seus catàlegs permetria construir aquestes integracions (i moltes altres eines innovadores) de manera robusta, eficient i sostenible.

RecomArt, en la seva forma actual, és només una petita demostració del potencial que hi ha en connectar millor els diferents recursos digitals del museu.

---

## 🤝 Contribucions

Aquest és un projecte personal molt senzill nascut d'una idea. Si tens suggeriments per millorar el codi, l'explicació, detectes algun error en les URLs de cerca, o simplement vols compartir idees sobre com millorar l'accés a la informació del museu, no dubtis a:

*   Obrir una **Issue** per discutir-ho.
*   Fer un **Fork** del projecte i enviar un **Pull Request** amb les teves millores.

---

## 📜 Llicència

Aquest projecte es distribueix sota la llicència MIT. Vegeu l'arxiu [LICENSE](LICENSE) per a més detalls. (Pots crear un arxiu `LICENSE` amb el text de la llicència MIT si vols).