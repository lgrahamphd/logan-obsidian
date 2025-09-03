# Yes Energy DS Cloud Schemas

## 1. YESDATA vs YESDS

* **YESDS**
  * Contains the **underlying tables** of the data (where applicable).
  * Tables are generally **more performant** in Snowflake than their secure view counterparts.
  * Recommended to use tables when possible.
  
* **YESDATA**
  * Contains **secure views** of the same data.
  * Views are less performant compared to tables according to Yes Energy.

* **Schema Layout**
  * Tables: Located in the `YESDS` schema.
  * Views: Located in the `YESDATA` schema.

* **References**
  * [DataSignals Cloud Schemas](https://help.yesenergy.com/help/datasignals-cloud-schemas)
  * [Tables and View Features & Characteristics](https://help.yesenergy.com/help/datasignals-cloud-tables-and-view-features-and-characteristics)
## 2. Data Catalog vs Snowflake Objects
- The **Yes Data Catalog** is a tool available in the PowerSignals web application meant to interactively show the full data catalog and how to access its elements. However, it's clearly still in beta mode, and it's unreliable (as of 8/28/2025).
* The **Yes Data Catalog** may not match objects in `YESDATA` or `YESDS` one-to-one.
* Example:
  * `YESDATA -> views -> IIR_OUTAGES` exists in Snowflake.
  * Data Catalog lists:
    * `IIR_OUTAGES_VINTAGE` (deprecated view)
    * `IIR_UNITS_BASE` (deprecated view)
* **Resolution**: Check the [third-party table documentation](https://help.yesenergy.com/help/third-party-table-documentation).
## 3. Missing Tables in Snowflake

* Example: `TS_IIR_ISO_FX` listed in Data Catalog but not visible in DS Cloud.
* Reason:
  * `TS_IIR_ISO_FX` is a **back end function**.
  * `IIR_ISO_TOTAL` is a **functional datatype**.
  * Both are available in **DSAPI** and **PowerSignals**, **not in DS Cloud**.
* Status: Data Catalog is being actively improved; some functions/types are documented but not exposed in Snowflake.
* **Reference**: [Data Catalog Module FAQs](https://help.yesenergy.com/help/data-catalog-module-faqs)
## Key Takeaways
- Use the Excel files for now. Data Catalog isn't production quality in my view.
- Remember that the third party tables (e.g., IIR) have their own Excel file.
## Miscellaneous Notes
- Use `IIR_OUTAGES_VINTAGE` and `IIR_UNITS_BASE`.
	- `IIR_OUTAGES` and `IIR_UNITS` are deprecated (and we would have had no way of knowing this without feedback from Yes Energy support...)