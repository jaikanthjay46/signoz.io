---
id: logging
title: Azure Functions Logging
---

## Overview
The following categories of Logs are available to export to Storage Account or EventHub. 

- Function App logs
- Function Authentication logs (beta)


Although, the application logs could be sent directly in the Application Level using a OpenTelemetry Log Appender, this might not an option for managed services.
### Prerequisites

- [EventHub Setup](../../bootstrapping/data-ingestion)
- [Central Collector Setup](../../bootstrapping/collector-setup)

## Setup

1. Navigate to your Azure Function in the Azure portal
2. Search for "Diagnostic settings" in the left navigation menu
3. Click on "Add Diagnostic Setting"
4. Select the desired log categories to export:
    - Function App logs
5. Configure the destination details as "**Stream to an Event Hub**" and select the Event Hub namespace and Event Hub name created during the [EventHub Setup](../../bootstrapping/data-ingestion)
6. Save the diagnostic settings

That's it! You have successfully set up logging for your Azure Function.