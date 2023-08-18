# mantle-fedex
FedEx shipping gateway integration 

######FedEx Integration for shipping rates, create shipping label, and void shipping label. In this Integration we worked on staging environment. So, the rates may vary from production environment.

###To Simplify:

Load the setup data in data/FedExSetupData.xml Load the demo configuration data in data/FedExZaaDemoData.xml or create your own configuration and load it; if you use the demo data, add your API token (SgoApiToken).

~ request#AccessToken service: This API call is to request new Access Token to authenticate a client, which will be valid for only 3600 seconds(1 hour).

~ get#ShippingRates service: This API returns a rate as per the destination location and parcel attributes.

~ create#ShippingLabel service: This label API will return a URL to a label for a trackingNumber and stores it in ShipmentPackageRouteSeg.

~ void#ShippingLabel service: You will need a trackingCode of shipment and account number of client to cancel a shipment. If the Shipment is too old to be canceled, this request will be denied.
