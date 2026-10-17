Combined breeding dataset: Atlas (MS Access) + DES Backlog
=========================================================

File: combined_atlas_des.parquet  (Parquet, zstd; open with pandas.read_parquet, R arrow, or DuckDB)
One row per species per survey sheet. Every row keeps its source label. Nothing has been deleted:
doubtful rows carry flags, and the column `usable` combines them.

Inputs (shared drive cleaned_csv/)
  Atlas  atlas_accepted_v6.csv (verified complete against the client's raw tables)
  DES    DES_Backlog_Data.xlsx (identical to the verified DES database)
  eBird is excluded (client decision, 11 Oct 2026).

Row basis
source    rows  sheets  survey_sheets  collection_sheets  breeding_rows  usable_rows  species  rows_without_name  first_year  last_year
 Atlas 6532446  573435         309829             263606         339992      6531324      631                  0        1900       2029
   DES  104137    2571           2452                119           2446       102701      417                  1        1976       2026

  DES: 3 DES records have no matched species and are not in this file
  (104,140 DES records received; 104,137 included).

Flag counts (rows)
source  des_misparsed  des_dup_copy  filler_date  bad_dates  no_region
 Atlas              0             0            0       1122          1
   DES            124          1160            0        152        446

Columns
  source            Atlas or DES
  sheet_id          survey sheet, prefixed A (Atlas) or D (DES) so the two never collide
  species_id        899_Species number (the agreed master list; same numbering in both sources)
  common_name, scientific_name   from the client's 899_Species reference. One DES row (sheet D901392) has
                    species_id 298, which is not on the list: 298 is Black Swan's IOC code, so it is probably Black
                    Swan (species 203). That mapping is proposed and awaiting the client, so the row is left as supplied.
  breeding          true if the record carries breeding evidence
  is_collection     true for collections (incidental records), false for surveys
  start_date, end_date, year, month   year and month are taken from start_date
  single_month      sheet starts and ends in the same calendar month
  klat, klon        ten-minute grid square
  region            region code (official region names still to be confirmed with the client)
  observer_id       contributor number only; no names or contact details
  des_misparsed     DES copy of sheet MFS6-26182.044 whose lines were keyed onto the wrong species
  des_dup_copy      second copy of a DES sheet with the same reference, dates, place and observer
  filler_date       Atlas start date 1 Jan 1900 (placeholder)
  bad_dates         end before start, missing start, or end after the source's cutoff
  usable            none of the four flags above is set

How the team analysis uses it
  - Keep rows where usable = true.
  - Reporting rates use surveys only (is_collection = false) in both numerator and denominator.
    Collections still count as breeding evidence.
  - Periods: early = Atlas 1977-1999; recent = Atlas 2000-2020 + DES 2021-2025.
  - Never pool reporting rates across sources; compare timing instead.
  - Results are associations only, with no causal climate claims.

Built by analysis/combined/build_combined.py and analysis/combined/export_combined.py (Yash's working folder).
