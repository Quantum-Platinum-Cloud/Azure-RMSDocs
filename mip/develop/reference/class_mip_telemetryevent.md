---
title: class TelemetryEvent 
description: Documents the telemetryevent::undefined class of the Microsoft Information Protection (MIP) SDK.
author: msmbaldwin
ms.service: information-protection
ms.topic: reference
ms.author: mbaldwin
ms.date: 03/30/2023
---

# class TelemetryEvent 
A single telemetry event.
  
## Summary
 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
public const std::string& GetName() const  |  Get event name.
public EventLevel GetLevel() const  |  Get level of event, indicating whether it is considered necessary service data (NSD) or not.
public const std::chrono::steady_clock::time_point& GetStartTime() const  |  Get event start time.
public void AddProperty(const std::shared_ptr&lt;EventProperty&gt;& prop)  |  Add a property to the event.
public void AddProperty(const std::string& name, bool value)  |  Add a bool property to the event.
public void AddProperty(const std::string& name, double value, Pii pii)  |  Add a double property to the event.
public void AddProperty(const std::string& name, int64_t value, Pii pii)  |  Add an int64 property to the event.
public void AddProperty(const std::string& name, const std::string& value, Pii pii)  |  Add a string property to the event.
public void AddAuditOnlyProperty(const std::string& name, const std::string& value)  |  Add an audit-only string property to the event.
public std::vector&lt;std::shared_ptr&lt;EventProperty&gt;&gt; GetProperties() const  |  Get all event properties.
public std::shared_ptr&lt;EventProperty&gt; GetProperty(const std::string& name)  |  Get property with the given name, if any.
  
## Members
  
### GetName function
Get event name.

  
**Returns**: [Event](class_mip_event.md) name
  
### GetLevel function
Get level of event, indicating whether it is considered necessary service data (NSD) or not.

  
**Returns**: Level of event
  
### GetStartTime function
Get event start time.

  
**Returns**: [Event](class_mip_event.md) start time
  
### AddProperty function
Add a property to the event.

Parameters:  
* **prop**: Property to add


  
### AddProperty function
Add a bool property to the event.

Parameters:  
* **name**: Property name 


* **value**: Property value


  
### AddProperty function
Add a double property to the event.

Parameters:  
* **name**: Property name 


* **value**: Property value 


* **pii**: PII classification


  
### AddProperty function
Add an int64 property to the event.

Parameters:  
* **name**: Property name 


* **value**: Property value 


* **pii**: PII classification


  
### AddProperty function
Add a string property to the event.

Parameters:  
* **name**: Property name 


* **value**: Property value 


* **pii**: PII classification


  
### AddAuditOnlyProperty function
Add an audit-only string property to the event.

Parameters:  
* **name**: Property name 


* **value**: Property value


An audit-only property contains sensitive information and must not be written to file logs or to any pipeline except for audit until it is manually scrubbed.
  
### GetProperties function
Get all event properties.

  
**Returns**: [Event](class_mip_event.md) properties
  
### GetProperty function
Get property with the given name, if any.

Parameters:  
* **name**: Name of the property to get



  
**Returns**: Property with the given name, or nullptr if none.