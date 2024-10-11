# IDEPC FHIR STI RLC
The file "idepc-fhir-sti.rlc" in this repository is used for loading MDH's "IDEPC FHIR STI" Rhapsody configuration into a Rhapsody environment.

The following Rhapsody components are included in the Rhapsody RLC:
* Route: IDEPC Map FhirStiToMif
    * The main route which includes a single JavaScript filter
* Shared JavaScript Library: IDEPC_FHIR_STI_v002
    * Handles the main mapping / translation code of FHIR R4 JSON data to the MIF (MEDSS Integration Format) which is XML based. The translation / mapping is detailed in the "Hennepin County FHIR R4 STI to MIF XML Data Translation.xlsx" Excel Spreadsheet.
* Lookup Table: IDEPC_FhirStiQuestions
    * Use to validate the data coming from Hennepin is in the correct format for MDH's MEDSS system.
    
MNIT at MDH's Rhapsody system contains global configuration that handles the routing of incoming data (including data from Hennepin) and global configuration that handles sending data into MDH's MEDSS system. Detailing these is outside the scope of this README and repository.