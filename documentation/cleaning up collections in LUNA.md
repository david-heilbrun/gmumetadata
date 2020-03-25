# Cleanup of LUNA metadata in OpenRefine

---

Use Facet > Text facet to look at column data. Check for blank values.

### How to deal with multiple columns
1. Go to Edit column > Join columns, choose "|" as the separator, select Skip nulls and Delete joined columns.
2. Go to the merged column and Edit cells > Split multi-valued cells, enter the "|" delimiter.
3. Change to records view.
4. Facet, reconcile, clean up the column.
5. Before finishing, reverse the process: Join multi-valued cells and split into several columns by delimiter. Remember to change column names to "Subject#1" etc.

---

### Date
* Make sure that dates align with [EDTF](https://www.loc.gov/standards/datetime/).
* If there is no date, and probable dates cannot be inferred from other parts of the record, leave for further analysis.

### Creator
* Reconcile with LCNAF, format uncontrolled names appropriately.
* If no creator, enter "Unknown"

### Genre
* Reconcile with AAT, change to more general terms if necessary.
* Can have more than one genre.

### Type
* Make sure that terms are in [DCMI Type Vocabulary](https://dublincore.org/specifications/dublin-core/dcmi-type-vocabulary/), prefer narrower terms like Still Image to Image.

### Subject
* Reconcile with LCSH/LCNAF. If appropriate terms cannot be found, leave existing terms (formatted appropriately) and consider adding more general LCSH.
* Move uncontrolled terms to a separate "Keyword" column.
* Add additional terms if you feel that that they would be useful.
* If there are entirely geographical terms, move them to a "Scope" column.
