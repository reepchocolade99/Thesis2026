# Thesis 2026

**Author:** @reepchocolade99  
**Institution:** University of Amsterdam (UvA)  

This repository contains the code, models, and analysis for my 2026 thesis project, conducted in collaboration with the University of Amsterdam.

## Data Availability and Privacy

Please note that the raw and processed datasets used in this project are not included in this repository and are ignored via `.gitignore`.

Due to the University of Amsterdam's strict data management guidelines and GDPR compliance, sensitive or proprietary research data cannot be hosted publicly on GitHub. To run the analysis scripts locally, you must obtain the dataset separately and place it in the designated `data/` directory.

## Dataset Structure

While the data files cannot be pushed to GitHub, the scripts expect a specific data format to function correctly. The analysis pipelines ingest two distinct domain-specific CSV data layouts (semi-colon separated: `;`). Below are the required schemas detailing exactly how the columns look:

### 1. Vacation Rental Domain (`vakantieverhuur.csv`)

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| **Octopus zaaknummer** | `String` | Unique administrative identification case number. |
| **Zaaktype** | `String` | Institutional category of the file (e.g., *Bezwaar*). |
| **Onderwerp** | `String` | Fine-grained legal legal matter subcategory. |
| **Primair Besluit** | `String` | Reference tracker code for the initial municipal ruling. |
| **Verzenddatum primair besluit**| `String` | Dispatched calendar date of the primary decision. |
| **Dictum** | `String` | Legal outcome of the review (*Gegrond*, *Ongegrond*, etc.). |
| **Zaakstatus** | `String` | State of the legal action process (e.g., *Afgehandeld*). |
| **Startdatum** | `String` | Official initiation date of the objection review procedure. |
| **Datum zitting** | `String` | Calendar date of the formal municipal hearing session. |
| **Verzendatum besluit** | `String` | Dispatch date for the definitive decision letter response. |
| **Planningsdatum** | `String` | Target administrative scheduling tracking mark. |
| **Afronddatum** | `String` | Final closing timestamp for the tracking record. |
| **Omschrijving** | `String` | Short descriptive summary or free-text brief notes. |
| **Richtung** | `String` | Document transmission flow parameter direction (*UIT* / *IN*). |
| **Document afgebroken** | `String` | Status flag noting if texts were cut due to system cell caps. |
| **geanonimiseerd_doc_inhoud** | `String` | Full text payload containing the anonymised legal report. |

### 2. Housing Allocation Domain (`WRV_bezwaren_.csv`)

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| **Octopus zaaknummer** | `String` | Unique administrative identification case number. |
| **Zaaktype** | `String` | Institutional category of the file (e.g., *Bezwaar*). |
| **Onderwerp** | `String` | Context metadata category regarding specific housing rules. |
| **Primair Besluit** | `String` | Reference tracker code for the initial municipal ruling. |
| **Verzenddatum primair besluit**| `String` | Dispatched timestamp of the primary decision. |
| **Dictum** | `String` | Legal outcome of the review (*Gegrond*, *Ongegrond*, etc.). |
| **Zaakstatus** | `String` | State of the legal action process (e.g., *Afgehandeld*). |
| **Behandelaar** | `String` | Anonymised string code or mask of the handling legal officer. |
| **Startdatum** | `String` | Official initiation date of the objection review procedure. |
| **Datum zitting** | `String` | Calendar date of the formal municipal hearing session. |
| **Verzendatum besluit** | `String` | Dispatch date for the definitive decision letter response. |
| **Planningsdatum** | `String` | Target administrative scheduling tracking mark. |
| **Afronddatum** | `String` | Final closing timestamp for the tracking record. |
| **geanonimiseerd_doc_inhoud** | `String` | Full text payload containing the anonymised legal report. |

---


## Getting Started

1. Clone the repository:
```bash
   git clone [https://github.com/reepchocolade99/Thesis2026.git](https://github.com/reepchocolade99/Thesis2026.git)
   cd Thesis2026
```
2. Install dependencies:

```bash
   pip install -r requirements.txt
Add your data: Place the .csv dataset into the /data folder.
```

3. Add your data: Create a local folder named data/ in the root directory and drop your target files inside:

```bash
data/vakantieverhuur.csv
data/WRV_bezwaren_.csv
```
4. Run the notebooks

