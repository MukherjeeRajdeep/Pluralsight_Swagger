# DefaultApi

All URIs are relative to *http://api.globalmantics.com/crm/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**customerPost**](DefaultApi.md#customerPost) | **POST** /customer | This is to create a request for customer&#39;s data
[**deleteCustomer**](DefaultApi.md#deleteCustomer) | **DELETE** /customer/{customerId} | delete a scpeific customer with the ID.
[**getCustomer**](DefaultApi.md#getCustomer) | **GET** /customer | This is to read customer&#39;s data
[**updateCustomer**](DefaultApi.md#updateCustomer) | **PUT** /customer/{customerId} | update existing customer


<a name="customerPost"></a>
# **customerPost**
> Integer customerPost(body)

This is to create a request for customer&#39;s data

This method is being used post the data in JSON mode. The data should be in the JSON format

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.DefaultApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure HTTP basic authorization: BasicAuth
HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
BasicAuth.setUsername("YOUR USERNAME");
BasicAuth.setPassword("YOUR PASSWORD");

DefaultApi apiInstance = new DefaultApi();
Customer body = new Customer(); // Customer | the new customer data in JSON format
try {
    Integer result = apiInstance.customerPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#customerPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Customer**](Customer.md)| the new customer data in JSON format |

### Return type

**Integer**

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain

<a name="deleteCustomer"></a>
# **deleteCustomer**
> Customer deleteCustomer(customerId)

delete a scpeific customer with the ID.

Deletes an existing customer from the app.

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.DefaultApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure HTTP basic authorization: BasicAuth
HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
BasicAuth.setUsername("YOUR USERNAME");
BasicAuth.setPassword("YOUR PASSWORD");

DefaultApi apiInstance = new DefaultApi();
Integer customerId = 56; // Integer | the id of the customer to delete the data
try {
    Customer result = apiInstance.deleteCustomer(customerId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#deleteCustomer");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customerId** | **Integer**| the id of the customer to delete the data |

### Return type

[**Customer**](Customer.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getCustomer"></a>
# **getCustomer**
> Customer getCustomer(customerId)

This is to read customer&#39;s data

This method is being used to fetch the customer data in JSON mode. It can be be questioned by other controller or some other user  using this API as a service

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.DefaultApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure HTTP basic authorization: BasicAuth
HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
BasicAuth.setUsername("YOUR USERNAME");
BasicAuth.setPassword("YOUR PASSWORD");

DefaultApi apiInstance = new DefaultApi();
Integer customerId = 56; // Integer | pass an optional customer id
try {
    Customer result = apiInstance.getCustomer(customerId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#getCustomer");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customerId** | **Integer**| pass an optional customer id |

### Return type

[**Customer**](Customer.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="updateCustomer"></a>
# **updateCustomer**
> updateCustomer(body, customerId)

update existing customer

Updates an existing customer with the Id

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.DefaultApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure HTTP basic authorization: BasicAuth
HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
BasicAuth.setUsername("YOUR USERNAME");
BasicAuth.setPassword("YOUR PASSWORD");

DefaultApi apiInstance = new DefaultApi();
Customer body = new Customer(); // Customer | the updated customer data inside the app
Integer customerId = 56; // Integer | the id of the cusotmer to update
try {
    apiInstance.updateCustomer(body, customerId);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#updateCustomer");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Customer**](Customer.md)| the updated customer data inside the app |
 **customerId** | **Integer**| the id of the cusotmer to update |

### Return type

null (empty response body)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

