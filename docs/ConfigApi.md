# ConfigApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteConfig**](ConfigApi.md#deleteConfig) | **DELETE** /api/v1/config/{guildId} | Delete a Config |
| [**getAllConfigs**](ConfigApi.md#getAllConfigs) | **GET** /api/v1/config | Get All Configs |
| [**getConfig**](ConfigApi.md#getConfig) | **GET** /api/v1/config/{guildId} | Get a saved Config |
| [**saveConfig**](ConfigApi.md#saveConfig) | **POST** /api/v1/config | Save a Config |
| [**updateConfig**](ConfigApi.md#updateConfig) | **PATCH** /api/v1/config | Update a Config |


<a id="deleteConfig"></a>
# **deleteConfig**
> deleteConfig(guildId)

Delete a Config

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.ConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ConfigApi apiInstance = new ConfigApi(defaultClient);
    Long guildId = 56L; // Long | 
    try {
      apiInstance.deleteConfig(guildId);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConfigApi#deleteConfig");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **guildId** | **Long**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Success |  -  |
| **400** | Validation Errors |  -  |
| **404** | Config not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="getAllConfigs"></a>
# **getAllConfigs**
> List&lt;ConfigDTO&gt; getAllConfigs()

Get All Configs

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.ConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ConfigApi apiInstance = new ConfigApi(defaultClient);
    try {
      List<ConfigDTO> result = apiInstance.getAllConfigs();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConfigApi#getAllConfigs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;ConfigDTO&gt;**](ConfigDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **500** | Internal Server Error |  -  |

<a id="getConfig"></a>
# **getConfig**
> ConfigDTO getConfig(guildId)

Get a saved Config

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.ConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ConfigApi apiInstance = new ConfigApi(defaultClient);
    Long guildId = 56L; // Long | 
    try {
      ConfigDTO result = apiInstance.getConfig(guildId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConfigApi#getConfig");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **guildId** | **Long**|  | |

### Return type

[**ConfigDTO**](ConfigDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Validation Errors |  -  |
| **404** | Config not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="saveConfig"></a>
# **saveConfig**
> saveConfig(configDTO)

Save a Config

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.ConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ConfigApi apiInstance = new ConfigApi(defaultClient);
    ConfigDTO configDTO = new ConfigDTO(); // ConfigDTO | 
    try {
      apiInstance.saveConfig(configDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConfigApi#saveConfig");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **configDTO** | [**ConfigDTO**](ConfigDTO.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **400** | Validation Errors |  -  |
| **409** | Constraint Violation Errors |  -  |
| **500** | Internal Server Error |  -  |

<a id="updateConfig"></a>
# **updateConfig**
> updateConfig(configDTO)

Update a Config

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.ConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ConfigApi apiInstance = new ConfigApi(defaultClient);
    ConfigDTO configDTO = new ConfigDTO(); // ConfigDTO | 
    try {
      apiInstance.updateConfig(configDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling ConfigApi#updateConfig");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **configDTO** | [**ConfigDTO**](ConfigDTO.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Success |  -  |
| **400** | Validation Errors |  -  |
| **404** | Config not found |  -  |
| **500** | Internal Server Error |  -  |

