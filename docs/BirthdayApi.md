# BirthdayApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteBirthday**](BirthdayApi.md#deleteBirthday) | **DELETE** /api/v1/birthday/{guildId}/{userId} | Delete a User&#39;s Birthday |
| [**deleteBirthdays**](BirthdayApi.md#deleteBirthdays) | **DELETE** /api/v1/birthday/{guildId} | Delete all Birthdays belonging to a Guild |
| [**getBirthday**](BirthdayApi.md#getBirthday) | **GET** /api/v1/birthday/{guildId}/{userId} | Get Birthday for a User in a Guild |
| [**getBirthdays**](BirthdayApi.md#getBirthdays) | **GET** /api/v1/birthday/{guildId} | Get Birthdays for a Guild |
| [**saveBirthday**](BirthdayApi.md#saveBirthday) | **POST** /api/v1/birthday | Save a Birthday |
| [**updateBirthday**](BirthdayApi.md#updateBirthday) | **PATCH** /api/v1/birthday | Update a Birthday |


<a id="deleteBirthday"></a>
# **deleteBirthday**
> deleteBirthday(guildId, userId)

Delete a User&#39;s Birthday

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayApi apiInstance = new BirthdayApi(defaultClient);
    Long guildId = 56L; // Long | 
    Long userId = 56L; // Long | 
    try {
      apiInstance.deleteBirthday(guildId, userId);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayApi#deleteBirthday");
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
| **userId** | **Long**|  | |

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
| **404** | Birthday not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="deleteBirthdays"></a>
# **deleteBirthdays**
> deleteBirthdays(guildId)

Delete all Birthdays belonging to a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayApi apiInstance = new BirthdayApi(defaultClient);
    Long guildId = 56L; // Long | 
    try {
      apiInstance.deleteBirthdays(guildId);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayApi#deleteBirthdays");
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
 - **Accept**: text/plain, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Validation Errors |  -  |
| **500** | Internal Server Error |  -  |

<a id="getBirthday"></a>
# **getBirthday**
> BirthdayDTO getBirthday(guildId, userId)

Get Birthday for a User in a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayApi apiInstance = new BirthdayApi(defaultClient);
    Long guildId = 56L; // Long | 
    Long userId = 56L; // Long | 
    try {
      BirthdayDTO result = apiInstance.getBirthday(guildId, userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayApi#getBirthday");
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
| **userId** | **Long**|  | |

### Return type

[**BirthdayDTO**](BirthdayDTO.md)

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
| **404** | Birthday or BirthdaySchedule not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="getBirthdays"></a>
# **getBirthdays**
> List&lt;BirthdayDTO&gt; getBirthdays(guildId)

Get Birthdays for a Guild

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayApi apiInstance = new BirthdayApi(defaultClient);
    Long guildId = 56L; // Long | 
    try {
      List<BirthdayDTO> result = apiInstance.getBirthdays(guildId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayApi#getBirthdays");
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

[**List&lt;BirthdayDTO&gt;**](BirthdayDTO.md)

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
| **500** | Internal Server Error |  -  |

<a id="saveBirthday"></a>
# **saveBirthday**
> saveBirthday(birthdayDTO)

Save a Birthday

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayApi apiInstance = new BirthdayApi(defaultClient);
    BirthdayDTO birthdayDTO = new BirthdayDTO(); // BirthdayDTO | 
    try {
      apiInstance.saveBirthday(birthdayDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayApi#saveBirthday");
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
| **birthdayDTO** | [**BirthdayDTO**](BirthdayDTO.md)|  | |

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

<a id="updateBirthday"></a>
# **updateBirthday**
> updateBirthday(birthdayDTO)

Update a Birthday

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayApi apiInstance = new BirthdayApi(defaultClient);
    BirthdayDTO birthdayDTO = new BirthdayDTO(); // BirthdayDTO | 
    try {
      apiInstance.updateBirthday(birthdayDTO);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayApi#updateBirthday");
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
| **birthdayDTO** | [**BirthdayDTO**](BirthdayDTO.md)|  | |

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
| **404** | Birthday or BirthdaySchedule not found |  -  |
| **500** | Internal Server Error |  -  |

