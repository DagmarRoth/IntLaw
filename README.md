# The Shifting Landscape of International Criminal Justice

An analysis of how domestic courts have become the primary venue for prosecuting war crimes, genocide, crimes against humanity, and terrorism—using data from the International Crimes Database.

## Key Findings

- **Domestic courts dominate:** 64% of all international crime prosecutions now happen in national courts, compared to 20% in hybrid tribunals and just 15% in UN ad-hoc bodies.

- **The Rome Statute paradox:** The United States, which never ratified the Rome Statute and "unsigned" the treaty in 2002, prosecutes more international crimes than any other country (96 domestic cases, 27% of the global total).

- **Treaty-free prosecution:** Non-Rome Statute countries account for 139 of 355 domestic prosecutions—nearly 40%—raising questions about the treaty architecture underlying international justice.

## Data Collection

Data was scraped from the [International Crimes Database](http://www.internationalcrimesdatabase.org/), which tracks international crimes adjudicated by national, international, and internationalized courts.

### Scraper Methodology

The scraper was built using Claude Code and follows this process:

1. **Index collection:** Iterates through an alphabetical index (A–Z) on the ICD website to collect links to individual case pages
2. **Metadata extraction:** Parses HTML to extract case name, court, country, crimes charged, parties, and decision date
3. **Court classification:** Categorizes each court into one of four types using regex pattern matching:
   - Domestic courts
   - Hybrid tribunals
   - UN ad-hoc tribunals
   - Regional human rights bodies
4. **Deduplication:** Removes duplicates using exact case number matching and fuzzy name matching (90% similarity threshold)
5. **Export:** Outputs cleaned data to CSV

## Visualizations

### Two-Column Donut Chart (Court Types)

A pie chart showing the distribution of prosecutions across court types.

- Created initial chart in Python
- Edited in Illustrator: added legend, made minor visual adjustments
- Exported via ai2html
- Displayed in two-column flexbox layout alongside descriptive text
- Responsive: columns stack horizontally on mobile

### Genocide Prosecutions Bar Chart

A stacked bar chart showing the top 10 countries by genocide case count.

**Process:**
1. Filtered to countries with more than one genocide case
2. Sorted by genocide count and selected top 10
3. Melted into long format for Plotly Express stacked bar rendering
4. In Illustrator: added backdrop, legend, cleaned up bars
5. Exported via ai2html

### Responsive Rome Statute Bar Chart

A bar chart comparing prosecutions between Rome Statute parties and non-parties.

**Process:**
1. Filtered data by Rome Statute signatory status
2. Created simple bar chart in Python
3. In Illustrator: made visual adjustments, added annotation noting U.S. representation among non-party countries
4. Used responsive chart template with wide and mobile formats
5. Exported via ai2html

## Resources

- [Report on genocide prosecutions](link)
- [The evolving relationship of domestic courts with the ICC](link)

## Reporting Notes

No interviews were conducted for this piece. Analysis relies on database records and the resources listed above.

---

*Data source: International Crimes Database*
