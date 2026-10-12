# GuildApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteGuild**](GuildApi.md#deleteGuild) | **DELETE** /api/v1/guild/{guildId} | Delete a Guild |
| [**getAllGuilds**](GuildApi.md#getAllGuilds) | **GET** /api/v1/guild | Get All Guilds |
| [**getGuild**](GuildApi.md#getGuild) | **GET** /api/v1/guild/{guildId} | Get a Guild |
| [**saveGuild**](GuildApi.md#saveGuild) | **POST** /api/v1/guild | Save a Guild |
| [**updateGuild**](GuildApi.md#updateGuild) | **PATCH** /api/v1/guild | Update a Guild |


<a id="deleteGuild"></a>
# **deleteGuild**
> deleteGuild(guildId)

Delete a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.GuildApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    GuildApi apiInstance = new GuildApi(defaultClient);
    Long guildId = 56L; // Long | 
    try {
      apiInstance.deleteGuild(guildId);
    } catch (ApiException e) {
      System.err.println("Exception when calling GuildApi#deleteGuild");
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
| **404** | Guild not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="getAllGuilds"></a>
# **getAllGuilds**
> List&lt;GuildDTO&gt; getAllGuilds()

Get All Guilds

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.GuildApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    GuildApi apiInstance = new GuildApi(defaultClient);
    try {
      List<GuildDTO> result = apiInstance.getAllGuilds();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GuildApi#getAllGuilds");
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

[**List&lt;GuildDTO&gt;**](GuildDTO.md)

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

<a id="getGuild"></a>
# **getGuild**
> GuildDTO getGuild(guildId)

Get a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.GuildApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    GuildApi apiInstance = new GuildApi(defaultClient);
    Long guildId = 56L; // Long | 
    try {
      GuildDTO result = apiInstance.getGuild(guildId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GuildApi#getGuild");
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

[**GuildDTO**](GuildDTO.md)

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
| **404** | Guild not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="saveGuild"></a>
# **saveGuild**
> saveGuild(guildDTO)

Save a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.GuildApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    GuildApi apiInstance = new GuildApi(defaultClient);
    GuildDTO guildDTO = new GuildDTO(); // GuildDTO | 
    try {
      apiInstance.saveGuild(guildDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling GuildApi#saveGuild");
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
| **guildDTO** | [**GuildDTO**](GuildDTO.md)|  | |

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

<a id="updateGuild"></a>
# **updateGuild**
> updateGuild(guildDTO)

Update a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.GuildApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    GuildApi apiInstance = new GuildApi(defaultClient);
    GuildDTO guildDTO = new GuildDTO(); // GuildDTO | 
    try {
      apiInstance.updateGuild(guildDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling GuildApi#updateGuild");
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
| **guildDTO** | [**GuildDTO**](GuildDTO.md)|  | |

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
| **404** | Guild not found |  -  |
| **500** | Internal Server Error |  -  |

