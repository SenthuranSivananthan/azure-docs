---
# Mandatory fields. See more on aka.ms/skyeye/meta.
title: Clouds and regions in which Azure Media Services v3 is available| Microsoft Docs
description: This article talks about Azure clouds and regions in which Azure Media Services v3 is available.  
services: media-services
documentationcenter: ''
author: Juliako
manager: femila
editor: ''

ms.service: media-services
ms.workload: 
ms.topic: article
ms.date: 01/11/2019
ms.author: juliako
---

# Clouds and regions in which Azure Media Services v3 exists

Azure Media Services v3 is available via Azure Resource Manager manifest in global Azure, Azure Government, Azure Germany, Azure China 21Vianet. However, not all Media Services features are available in all the Azure clouds. This document outlines availabilities of main Media Services v3 components.

## Feature availability in Azure clouds

| Feature|Global Azure Regions | Azure Government|Azure Germany|Azure China 21Vianet|
| --- | --- | --- | --- | --- |
| [Azure EventGrid](reacting-to-media-services-events.md) | Available | Not available | Not available | Not available |
| [VideoAnalyzerPreset](analyzing-video-audio-files-concept.md) |  Available | Not available | Not available | Not available |
| [AudioAnalyzerPreset](analyzing-video-audio-files-concept.md) |  Available | Not available | Not available | Not available |
| [StandardEncoderPreset](encoding-concept.md) | Available | Available | Available | Available |
| [LiveEvents](live-streaming-overview.md) | Available | Available | Available | Available |
| [StreamingEndpoints](streaming-endpoint-concept.md) | Available | Available | Available | Available |

## Regions/geographies/locations

* [Azure regions](https://azure.microsoft.com/global-infrastructure/regions/)
* [Product by region](https://azure.microsoft.com/global-infrastructure/services/)
* [Azure geographies](https://azure.microsoft.com/global-infrastructure/geographies/)
* [Azure locations](https://azure.microsoft.com/global-infrastructure/locations/)

## Region code name 

When you need to supply the **location** parameter, you need to provide the region code name as the **location** value. To get the code name of the region that your account is in and that your call should be routed to, you can run the following line in [Azure CLI](https://docs.microsoft.com/cli/azure/?view=azure-cli-latest)

```bash
az account list-locations
```

Once you run the line shown above, you get a list of all Azure regions. Navigate to the Azure region that has the *displayName* you are looking for, and use its *name* value for the **location** parameter.

For example, for the Azure region West US 2 (displayed below), you will use "westus2" for the **location** parameter.

```json
   {
      "displayName": "West US 2",
      "id": "/subscriptions/00000000-23da-4fce-b59c-f6fb9513eeeb/locations/westus2",
      "latitude": "47.233",
      "longitude": "-119.852",
      "name": "westus2",
      "subscriptionId": null
    }
```

## Next steps

[Media Services v3 overview](media-services-overview.md)
