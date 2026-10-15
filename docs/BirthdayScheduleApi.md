# BirthdayScheduleApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**advance**](BirthdayScheduleApi.md#advance) | **PATCH** /api/v1/birthday/schedule/advance/{guildId}/{userId} | Update birthday schedule for next year |
| [**getActiveSchedules**](BirthdayScheduleApi.md#getActiveSchedules) | **GET** /api/v1/birthday/schedule/active | Get a list of birthday schedules overdue by at most 24 hours |
| [**getExpiredSchedules**](BirthdayScheduleApi.md#getExpiredSchedules) | **GET** /api/v1/birthday/schedule/expired | Get a list of birthday schedules overdue by more than 24 hours |
| [**getSchedule**](BirthdayScheduleApi.md#getSchedule) | **GET** /api/v1/birthday/schedule/{guildId}/{userId} | Get birthday schedule for a particular guild and user |
| [**getUpcomingSchedules**](BirthdayScheduleApi.md#getUpcomingSchedules) | **GET** /api/v1/birthday/schedule/upcoming | Get a list of birthday schedules due in the future |


<a id="advance"></a>
# **advance**
> advance(guildId, userId)

Update birthday schedule for next year

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayScheduleApi apiInstance = new BirthdayScheduleApi(defaultClient);
    Long guildId = 56L; // Long | 
    Long userId = 56L; // Long | 
    try {
      apiInstance.advance(guildId, userId);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayScheduleApi#advance");
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
| **404** | Schedule not found |  -  |
| **500** | Internal Server Error |  -  |

<a id="getActiveSchedules"></a>
# **getActiveSchedules**
> List&lt;BirthdayScheduleDTO&gt; getActiveSchedules()

Get a list of birthday schedules overdue by at most 24 hours

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayScheduleApi apiInstance = new BirthdayScheduleApi(defaultClient);
    try {
      List<BirthdayScheduleDTO> result = apiInstance.getActiveSchedules();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayScheduleApi#getActiveSchedules");
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

[**List&lt;BirthdayScheduleDTO&gt;**](BirthdayScheduleDTO.md)

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

<a id="getExpiredSchedules"></a>
# **getExpiredSchedules**
> List&lt;BirthdayScheduleDTO&gt; getExpiredSchedules()

Get a list of birthday schedules overdue by more than 24 hours

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayScheduleApi apiInstance = new BirthdayScheduleApi(defaultClient);
    try {
      List<BirthdayScheduleDTO> result = apiInstance.getExpiredSchedules();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayScheduleApi#getExpiredSchedules");
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

[**List&lt;BirthdayScheduleDTO&gt;**](BirthdayScheduleDTO.md)

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

<a id="getSchedule"></a>
# **getSchedule**
> List&lt;BirthdayScheduleDTO&gt; getSchedule(guildId, userId)

Get birthday schedule for a particular guild and user

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayScheduleApi apiInstance = new BirthdayScheduleApi(defaultClient);
    Long guildId = 56L; // Long | 
    Long userId = 56L; // Long | 
    try {
      List<BirthdayScheduleDTO> result = apiInstance.getSchedule(guildId, userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayScheduleApi#getSchedule");
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

[**List&lt;BirthdayScheduleDTO&gt;**](BirthdayScheduleDTO.md)

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

<a id="getUpcomingSchedules"></a>
# **getUpcomingSchedules**
> List&lt;BirthdayScheduleDTO&gt; getUpcomingSchedules()

Get a list of birthday schedules due in the future

### Example
```java
// Import classes:
import io.github.eggy03.yabb.client.ApiClient;
import io.github.eggy03.yabb.client.ApiException;
import io.github.eggy03.yabb.client.Configuration;
import io.github.eggy03.yabb.client.models.*;
import io.github.eggy03.yabb.client.api.BirthdayScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    BirthdayScheduleApi apiInstance = new BirthdayScheduleApi(defaultClient);
    try {
      List<BirthdayScheduleDTO> result = apiInstance.getUpcomingSchedules();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BirthdayScheduleApi#getUpcomingSchedules");
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

[**List&lt;BirthdayScheduleDTO&gt;**](BirthdayScheduleDTO.md)

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

