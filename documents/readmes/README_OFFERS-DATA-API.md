# vdp-sample-java-offers-data-api

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.


This is a sample implementation of OffersdataapiApi only for reference purpose.

## Getting Started

### Create an App
First  create an app on [Visa Developer - App Dashboard](https://developer.visa.com/portal/#console)

An application within Visa Developer contains a set of APIs that you can access with one set of credentials.

### Generate Authentication Keys
Visa Developer uses simple and effective authentication and authorization methods.
Based on the APIs you select, use one of the following two standard and supported authentication methods for calling the APIs:

- Two-Way SSL (Mutual Authentication)
- API Key - Shared Secret (x-pay-token)

For more details check: [Visa Developer - Authentication](https://developer.visa.com/guides/vdpguide#two_way_ssl)


Set the relevant mutualAuth authentication keys and execute the API call:


```java
import com.visa.developer.sample.offersdataapi.*;
import com.visa.developer.sample.offersdataapi.api.*;
import com.visa.developer.sample.offersdataapi.auth.HttpBasicAuth;
import com.visa.developer.sample.offersdataapi.auth.ApiKeyAuth;

import java.util.*;
import java.io.IOException;


public class OffersdataapiApi {

    public static void main(String[] args) throws IOException, ApiException {
    
        //Configure HTTP basic authorization: mutualAuth
        HttpBasicAuth authInstance =   new HttpBasicAuth();
        authInstance.setPassword("{SET PASSWORD}");
        authInstance.setUsername("{SET USERNAME}");
        authInstance.setKEYSTORE_PATH("{SET PATH TO KEYSTORE}");
        authInstance.setKEYSTORE_PASSWORD("{SET KEYSTORE PASSWORD}");
        authInstance.setPRIVATE_KEY_PASSWORD("{SET PRIVATE KEY PASSWORD}");
    

        ApiClient apiClient = new ApiClient(authInstance);
        OffersdataapiApi api = new OffersdataapiApi(apiClient);
        api.retrieveAllOffers_Example();
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://sandbox.api.visa.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OffersdataapiApi* | [**retrieveAllOffers**](docs/OffersdataapiApi.md#retrieveAllOffers) | **GET** /vmorc/offers/v1/all | Retrieve All Offers
*OffersdataapiApi* | [**retrieveOffersByContentId**](docs/OffersdataapiApi.md#retrieveOffersByContentId) | **GET** /vmorc/offers/v1/bycontentid | Retrieve Offers by a Content Id
*OffersdataapiApi* | [**retrieveOffersByFilter**](docs/OffersdataapiApi.md#retrieveOffersByFilter) | **GET** /vmorc/offers/v1/byfilter | List of Offers By Filter
*OffersdataapiApi* | [**retrieveOffersByOfferId**](docs/OffersdataapiApi.md#retrieveOffersByOfferId) | **GET** /vmorc/offers/v1/byofferid | Retrieve Offers By Offer Id


## Documentation for Authorization

Authentication schemes defined for the API:
### mutualAuth

- **Type**: HTTP basic authentication

For more details check: [Visa Developer - Authentication](https://developer.visa.com/guides/vdpguide#two_way_ssl)

