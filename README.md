# INTEGRA Geschaeftspartner anlegen

Link to INTEGRA master repository  
[INTEGRA](https://github.com/Integra-SUPERB/INTEGRA)


## Goal of this repository
Using the [Geschäftspartner anlegen](https://github.com/Integra-SUPERB/INTEGRA_Geschaeftspartner-anlegen) repository, you can request a new business partner. In Switzerland, both natural persons and juridical persons are considered business partners by the Swiss government. However, if you use this API, you are not actually creating a new business partner directly. Instead, you are sending a request to a team at the Federal Finance Administration (FFA). This team manages the master data and ensures that every person only exists once in the database. If your request is approved, a new business partner will be created.

**Attention!**  
Before you request a new business partner, please use the [search function](https://github.com/Integra-SUPERB/INTEGRA_Geschaeftspartner-suchen) to find existing records.

## How does this API work?
Multiple links to the official sap documentation will help you understand the different parameters and necessary parts of information to use the API successfully. 

To provide a fast and easy reference, we recommend that you start by reviewing our [empty create request XML file](https://github.com/Integra-SUPERB/INTEGRA_Geschaeftspartner-anlegen/blob/main/BusinessPartnerSUITEBulkReplicateRequest_Out.xml). This file is intended to help you understand the structure and format of the request data that you need to provide in order to use the API.

The description for the replication of a business partner **inbound** is found here: [Replicate request in service.](https://api.sap.com/api/OP_BUSINESSPARTNERSUITEBULKREPLIC/resource)

The replication **outbound** is handled here: [Replicate request out service.](https://api.sap.com/api/OP_CO_MDG_BP_RPLCTRQ/resource)

If you want to learn more about the **success message** that the API should return after a successful replication, you can find detailed information in our [Replicate Confirmation](https://github.com/Integra-SUPERB/INTEGRA_Geschaeftspartner-replikation) Repository.

Special fields that were added are as follows...

Entitätstyp BP_SALES:
Attribut | Datenelement | Beschreibung
--- | --- | ---
ZEBILLACC | ZZA_ZXG_EBILLACCOUNTID | EGOV: eBillAccountID/Provider Nummer
ZEMAILVER | ZZA_ZXG_EMAILPDFVER | EGOV: Empfängeradresse für den E-Mail-Ver-sand von Rechnung
ZIEBILACC | ZZA_ZXG_EBILLACCID | EGOV: Interconnect EBillAccountID

Entitätstyp BP_VENGEN:
Attribut | Datenelement | Beschreibung
--- | --- | ---
ZZBILIDDP | ZZA_ZXG_BILLERIDDP | EGOV: BillerID Drittprovider
ZZBILIDSW | ZZA_ZXG_BILLERIDSW | EGOV: BillerID Swisscom
ZZBILLID | ZZA_ZXG_BILLERID | EGOV: BillerID

## Contact information
With the information provided above, you should gain a high-level overview of the capabilities of the API. 

If you wish to use and work with the API, please contact us so that we can review your application and provide you with the necessary credentials and information.

For further assistance with the API, the BIT technical support SAP team is available to answer your questions during normal office hours.

To contact us, please email FachsupportSAP@bit.admin.ch
