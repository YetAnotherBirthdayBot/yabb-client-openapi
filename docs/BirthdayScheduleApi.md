# BirthdayScheduleApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**advance**](BirthdayScheduleApi.md#advance) | **PATCH** /api/v1/birthday/schedule/advance/{scheduleGuildId}/{scheduleUserId} | Update schedule for next year |
| [**getActiveSchedules**](BirthdayScheduleApi.md#getActiveSchedules) | **GET** /api/v1/birthday/schedule/active | Get a list of schedules overdue by at most 24 hours |
| [**getExpiredSchedules**](BirthdayScheduleApi.md#getExpiredSchedules) | **GET** /api/v1/birthday/schedule/expired | Get a list of schedules overdue by more than 24 hours |
| [**getUpcomingSchedules**](BirthdayScheduleApi.md#getUpcomingSchedules) | **GET** /api/v1/birthday/schedule/upcoming | Get a list of schedules due in the future |


<a id="advance"></a>
# **advance**
> advance(scheduleGuildId, scheduleUserId)

Update schedule for next year

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
    Long scheduleGuildId = 56L; // Long | 
    Long scheduleUserId = 56L; // Long | 
    try {
      apiInstance.advance(scheduleGuildId, scheduleUserId);
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
| **scheduleGuildId** | **Long**|  | |
| **scheduleUserId** | **Long**|  | |

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

Get a list of schedules overdue by at most 24 hours

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

Get a list of schedules overdue by more than 24 hours

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

<a id="getUpcomingSchedules"></a>
# **getUpcomingSchedules**
> List&lt;BirthdayScheduleDTO&gt; getUpcomingSchedules()

Get a list of schedules due in the future

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

