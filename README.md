# Mantle RSIS Core REST API Integration

[![license](http://img.shields.io/badge/license-CC0%201.0%20Universal-blue.svg)](https://github.com/moqui/mantle-rsis/blob/master/LICENSE.md)

Mantle USL Mantle Integration for Rock Solid Internet Shipping (RSIS) Core REST API for shipping rates, labels, and tracking across a wide 
variety of carriers including UPS, FedEx, DHL, USPS, and many more.

To add this component to Moqui the easiest approach is to use the Gradle get component task:

    $ ./gradlew getComponent -Pcomponent=mantle-rsis

Or add a dependency in your component.xml file like:

    <depends-on name="mantle-rsis"/>

To use simply:

1. load the setup data in data/RsisSetupData.xml
2. load the demo configuration data in data/RsisZaaDemoData.xml or create your own configuration and load it; if you use the demo data, add your API Key (SgoApiToken option)
3. configure the store shipping gateway with a ShippingGatewayConfig record (see the demo data file for an example)
4. test the gateway with some test orders/shipments, retrieving rates and labels

Note that PopCommerce and various screens in SimpleScreens have support for RSIS and other shipping plugins to mantle-usl.
