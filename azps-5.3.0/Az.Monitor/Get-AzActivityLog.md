---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501418"
---
# <span data-ttu-id="dcec6-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="dcec6-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="dcec6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcec6-102">SYNOPSIS</span></span>
<span data-ttu-id="dcec6-103">Pobieranie zdarzeń dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="dcec6-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="dcec6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcec6-104">SYNTAX</span></span>

### <span data-ttu-id="dcec6-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="dcec6-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcec6-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcec6-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcec6-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcec6-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcec6-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="dcec6-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcec6-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="dcec6-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcec6-110">Opis</span><span class="sxs-lookup"><span data-stu-id="dcec6-110">DESCRIPTION</span></span>
<span data-ttu-id="dcec6-111">Polecenie cmdlet Get-AzActivityLog pobierania zdarzeń dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="dcec6-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="dcec6-112">Zdarzenia można kojarzyć z bieżącym IDENTYFIKATORem subskrypcji, IDENTYFIKATORem korelacji, grupą zasobów, IDENTYFIKATORem zasobu lub dostawcą zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcec6-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="dcec6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcec6-113">EXAMPLES</span></span>

### <span data-ttu-id="dcec6-114">Przykład 1: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dcec6-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="dcec6-115">To polecenie zawiera listę najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-116">Przykład 2: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="dcec6-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="dcec6-117">To polecenie zawiera listę najwyżej 100 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-118">Przykład 3: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="dcec6-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="dcec6-119">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który miał miejsce w dniu lub po cenie 2017 – 06-01T10:30 czas lokalny, jeśli ta data/godzina nie jest starsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-120">Przykład 4: uzyskiwanie dziennika zdarzeń według identyfikatora abonamentu z godziną rozpoczęcia i godziną zakończenia.</span><span class="sxs-lookup"><span data-stu-id="dcec6-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="dcec6-121">To polecenie wyświetla najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który miał miejsce w dniu lub po dniu 2017 – 04 – 01T10:30 czas lokalny, a przed 2017em – 04 – 14T11:30 czas lokalny, jeśli cały zakres daty/godziny nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="dcec6-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="dcec6-122">Przykład 5: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji</span><span class="sxs-lookup"><span data-stu-id="dcec6-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="dcec6-123">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="dcec6-124">**Uwaga**: jest to zwykle tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="dcec6-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="dcec6-125">Przykład 6: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="dcec6-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="dcec6-126">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="dcec6-127">**Uwaga**: jest to zwykle tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="dcec6-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="dcec6-128">Przykład 7: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji i godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="dcec6-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="dcec6-129">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="dcec6-130">**Uwaga**: jest to zwykle tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="dcec6-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="dcec6-131">Przykład 8: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="dcec6-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="dcec6-132">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który miał miejsce w dniu lub po cenie 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres daty/godziny nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="dcec6-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="dcec6-133">Przykład 9: uzyskiwanie dziennika zdarzeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dcec6-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="dcec6-134">To polecenie wyświetla najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w ciągu 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-135">Przykład 10: uzyskiwanie dziennika zdarzeń dla grupy zasobów z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="dcec6-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="dcec6-136">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-137">Przykład 11: pobieranie dziennika zdarzeń dla grupy zasobów według czasu rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="dcec6-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="dcec6-138">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-139">Przykład 12: pobieranie dziennika zdarzeń dla grupy zasobów z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="dcec6-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="dcec6-140">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po cenie 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017em – 04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="dcec6-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="dcec6-141">Przykład 13: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="dcec6-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="dcec6-142">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-143">Przykład 14: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="dcec6-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="dcec6-144">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-145">Przykład 15: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="dcec6-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="dcec6-146">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-147">Przykład 16: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="dcec6-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="dcec6-148">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce w dniu lub po dniu 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="dcec6-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="dcec6-149">Przykład 17: uzyskiwanie dziennika zdarzeń według dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="dcec6-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="dcec6-150">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-151">Przykład 18: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="dcec6-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="dcec6-152">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-153">Przykład 19: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów przy użyciu godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="dcec6-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="dcec6-154">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="dcec6-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="dcec6-155">Przykład 20: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="dcec6-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="dcec6-156">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce w dniu lub po dniu 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="dcec6-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="dcec6-157">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcec6-157">PARAMETERS</span></span>

### <span data-ttu-id="dcec6-158">— Rozmówca</span><span class="sxs-lookup"><span data-stu-id="dcec6-158">-Caller</span></span>
<span data-ttu-id="dcec6-159">Rozmówca zdarzeń do pobrania</span><span class="sxs-lookup"><span data-stu-id="dcec6-159">The caller of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-160">-Identyfikator korelacji</span><span class="sxs-lookup"><span data-stu-id="dcec6-160">-CorrelationId</span></span>
<span data-ttu-id="dcec6-161">Identyfikator korelacji</span><span class="sxs-lookup"><span data-stu-id="dcec6-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcec6-162">-DefaultProfile</span></span>
<span data-ttu-id="dcec6-163">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcec6-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="dcec6-164">-DetailedOutput</span></span>
<span data-ttu-id="dcec6-165">Zwraca obiekt ze wszystkimi szczegółami zdarzeń (domyślnie zostaną zwrócone tylko niektóre atrybuty, tzn. Brak szczegółów).</span><span class="sxs-lookup"><span data-stu-id="dcec6-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dcec6-166">-EndTime</span></span>
<span data-ttu-id="dcec6-167">EndTime kwerendy</span><span class="sxs-lookup"><span data-stu-id="dcec6-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="dcec6-168">-MaxRecord</span></span>
<span data-ttu-id="dcec6-169">Maksymalna liczba rekordów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="dcec6-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="dcec6-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="dcec6-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcec6-171">-ResourceGroupName</span></span>
<span data-ttu-id="dcec6-172">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dcec6-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcec6-173">-ResourceId</span></span>
<span data-ttu-id="dcec6-174">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="dcec6-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="dcec6-175">-ResourceProvider</span></span>
<span data-ttu-id="dcec6-176">Nazwa ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="dcec6-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dcec6-177">-StartTime</span></span>
<span data-ttu-id="dcec6-178">Identyfikator korelacji zapytania</span><span class="sxs-lookup"><span data-stu-id="dcec6-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-179">-Status</span><span class="sxs-lookup"><span data-stu-id="dcec6-179">-Status</span></span>
<span data-ttu-id="dcec6-180">Stan zdarzeń do pobrania</span><span class="sxs-lookup"><span data-stu-id="dcec6-180">The status of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec6-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcec6-181">CommonParameters</span></span>
<span data-ttu-id="dcec6-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcec6-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcec6-183">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcec6-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcec6-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcec6-184">INPUTS</span></span>

### <span data-ttu-id="dcec6-185">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dcec6-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dcec6-186">System. String</span><span class="sxs-lookup"><span data-stu-id="dcec6-186">System.String</span></span>

### <span data-ttu-id="dcec6-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dcec6-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dcec6-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dcec6-188">System.Int32</span></span>

## <span data-ttu-id="dcec6-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcec6-189">OUTPUTS</span></span>

### <span data-ttu-id="dcec6-190">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="dcec6-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="dcec6-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcec6-191">NOTES</span></span>

## <span data-ttu-id="dcec6-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcec6-192">RELATED LINKS</span></span>
