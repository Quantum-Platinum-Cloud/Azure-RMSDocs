---
title: class FileProfile::Settings 
description: Documents the fileprofile::settings class of the Microsoft Information Protection (MIP) SDK.
author: msmbaldwin
ms.service: information-protection
ms.topic: reference
ms.author: mbaldwin
ms.date: 03/30/2023
---

# class FileProfile::Settings 
Settings used by [FileProfile](class_mip_fileprofile.md) during its creation and throughout its lifetime.
  
## Summary
 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
public Settings(const std::shared_ptr&lt;MipContext&gt;& mipContext, CacheStorageType cacheStorageType, std::shared_ptr&lt;ConsentDelegate&gt; consentDelegate, std::shared_ptr&lt;Observer&gt; observer)  |  [FileProfile::Settings](class_mip_fileprofile_settings.md) constructor.
public CacheStorageType GetCacheStorageType() const  |  Get whether caches are stored in memory or on disk.
public std::shared_ptr&lt;ConsentDelegate&gt; GetConsentDelegate() const  |  Gets the consent delegate used to request user consent connecting to services.
public std::shared_ptr&lt;Observer&gt; GetObserver() const  |  Gets the observer that receives notifications of events related to [FileProfile](class_mip_fileprofile.md).
public std::shared_ptr&lt;MipContext&gt; GetMipContext() const  |  Get MIP context which represents shared state across all profiles.
public std::shared_ptr&lt;HttpDelegate&gt; GetHttpDelegate() const  |  Get the HTTP delegate (if any) provided by the application.
public void SetHttpDelegate(const std::shared_ptr&lt;HttpDelegate&gt;& httpDelegate)  |  Override default HTTP stack with client's own.
public std::shared_ptr&lt;TaskDispatcherDelegate&gt; GetTaskDispatcherDelegate() const  |  Get the TaskDispatcher delegate (if any) provided by the application.
public void SetTaskDispatcherDelegate(const std::shared_ptr&lt;TaskDispatcherDelegate&gt;& taskDispatcherDelegate)  |  Override default asynchonous task dispatching handling with client's own.
public void SetSessionId(const std::string& sessionId)  |  Sets the session ID.
public const std::string& GetSessionId() const  |  Gets the session ID.
public void SetCanCacheLicenses(bool canCacheLicenses)  |  Configures whether or not end user licenses (EULs) will be cached locally.
public bool CanCacheLicenses() const  |  Gets whether or not end user licenses (EULs) are cached locally.
public const std::shared_ptr&lt;void&gt;& GetLoggerContext() const  |  Get logger context that will be opaquely passed to the logger delegate for logs associated with the created profile.
public void SetLoggerContext(const std::shared_ptr&lt;void&gt;& loggerContext)  |  Sets the logger context that will be opaquely passed to the logger delegate for logs associated with the created profile.
public DnsRedirection GetDnsRedirection() const  |  Gets the dns redirect mode.
public void SetDnsRedirection(DnsRedirection dnsRedirection)  |  Sets the dns redirection mode that controls how redirection is handled during online operations.
  
## Members
  
### Settings function
[FileProfile::Settings](class_mip_fileprofile_settings.md) constructor.

Parameters:  
* **mipContext**: Global context settings 


* **cacheStorageType**: Store any cached state in memory or on disk 


* **consentDelegate**: Delegate used to obtain user permission to access external resources 


* **observer**: Observer instance that will receive notifications of events related to [FileProfile](class_mip_fileprofile.md)


  
### GetCacheStorageType function
Get whether caches are stored in memory or on disk.

  
**Returns**: Storage type used
  
### GetConsentDelegate function
Gets the consent delegate used to request user consent connecting to services.

  
**Returns**: Consent delegate used for requesting user consent
  
### GetObserver function
Gets the observer that receives notifications of events related to [FileProfile](class_mip_fileprofile.md).

  
**Returns**: Observer that receives notifications of events related to [FileProfile](class_mip_fileprofile.md)
  
### GetMipContext function
Get MIP context which represents shared state across all profiles.

  
**Returns**: MIP context
  
### GetHttpDelegate function
Get the HTTP delegate (if any) provided by the application.

  
**Returns**: HTTP delegate to be used for HTTP operations
  
### SetHttpDelegate function
Override default HTTP stack with client's own.

Parameters:  
* **httpDelegate**: HTTP callback interface implemented by client application


  
### GetTaskDispatcherDelegate function
Get the TaskDispatcher delegate (if any) provided by the application.

  
**Returns**: TaskDispatcher delegate to be used for executing asynchronous tasks
  
### SetTaskDispatcherDelegate function
Override default asynchonous task dispatching handling with client's own.

Parameters:  
* **taskDispatcherDelegate**: Task dispatching callback interface implemented by client application


tasks can reference profile objects preventing its destruction as a result taskdispatcher queues should not be shared.
  
### SetSessionId function
Sets the session ID.

Parameters:  
* **sessionId**: Session ID that will be used to correlate logs/telemetry


  
### GetSessionId function
Gets the session ID.

  
**Returns**: Session ID that will be used to correlate logs/telemetry
  
### SetCanCacheLicenses function
Configures whether or not end user licenses (EULs) will be cached locally.

Parameters:  
* **canCacheLicenses**: Whether or not engine should cache a license when opening protected content


If true, opening protected content will cache the associated license locally. If false, opening protected content will always perform HTTP operation to acquire the license from the RMS service.
  
### CanCacheLicenses function
Gets whether or not end user licenses (EULs) are cached locally.

  
**Returns**: License caching configuration
  
### GetLoggerContext function
Get logger context that will be opaquely passed to the logger delegate for logs associated with the created profile.

  
**Returns**: The logger context
  
### SetLoggerContext function
Sets the logger context that will be opaquely passed to the logger delegate for logs associated with the created profile.

Parameters:  
* **loggerContext**: The logger context


  
### GetDnsRedirection function
Gets the dns redirect mode.

  
**Returns**: The redirect mode used
  
### SetDnsRedirection function
Sets the dns redirection mode that controls how redirection is handled during online operations.

Parameters:  
* **dnsRedirection**: The redirection mode to use

ode to use

