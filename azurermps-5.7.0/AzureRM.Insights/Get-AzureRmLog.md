---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: bdafc4ba051383a270c361f3a88453022504fe9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525101"
---
# <span data-ttu-id="d3eca-101">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="d3eca-101">Get-AzureRmLog</span></span>

## <span data-ttu-id="d3eca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3eca-102">SYNOPSIS</span></span>
<span data-ttu-id="d3eca-103">Pobiera dziennik zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="d3eca-103">Gets a log of events.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3eca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3eca-104">SYNTAX</span></span>

### <span data-ttu-id="d3eca-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="d3eca-105">GetByCorrelationId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3eca-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3eca-106">GetByResourceId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3eca-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d3eca-107">GetByResourceGroup</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3eca-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d3eca-108">GetByResourceProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3eca-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="d3eca-109">GetBySubscription</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3eca-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d3eca-110">DESCRIPTION</span></span>
<span data-ttu-id="d3eca-111">Polecenie cmdlet **Get-AzureRmLog** pobiera dziennik zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="d3eca-111">The **Get-AzureRmLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="d3eca-112">Zdarzenia można kojarzyć z bieżącym IDENTYFIKATORem subskrypcji, IDENTYFIKATORem korelacji, grupą zasobów, IDENTYFIKATORem zasobu lub dostawcą zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3eca-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="d3eca-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3eca-113">EXAMPLES</span></span>

### <span data-ttu-id="d3eca-114">Przykład 1: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d3eca-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzureRmLog
```

<span data-ttu-id="d3eca-115">To polecenie zawiera listę najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-116">Przykład 2: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="d3eca-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

<span data-ttu-id="d3eca-117">To polecenie zawiera listę najwyżej 100 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-118">Przykład 3: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="d3eca-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="d3eca-119">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który miał miejsce w dniu lub po cenie 2017 – 06-01T10:30 czas lokalny, jeśli ta data/godzina nie jest starsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-120">Przykład 4: uzyskiwanie dziennika zdarzeń według identyfikatora abonamentu z godziną rozpoczęcia i godziną zakończenia.</span><span class="sxs-lookup"><span data-stu-id="d3eca-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="d3eca-121">To polecenie wyświetla najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który miał miejsce w dniu lub po dniu 2017 – 04 – 01T10:30 czas lokalny, a przed 2017em – 04 – 14T11:30 czas lokalny, jeśli cały zakres daty/godziny nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d3eca-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d3eca-122">Przykład 5: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji</span><span class="sxs-lookup"><span data-stu-id="d3eca-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="d3eca-123">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="d3eca-124">**Uwaga** : jest to zwykle tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="d3eca-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d3eca-125">Przykład 6: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="d3eca-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="d3eca-126">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który nastąpił 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="d3eca-127">**Uwaga** : jest to zwykle tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="d3eca-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d3eca-128">Przykład 7: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji i godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="d3eca-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="d3eca-129">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="d3eca-130">**Uwaga** : jest to zwykle tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="d3eca-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d3eca-131">Przykład 8: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="d3eca-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="d3eca-132">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który miał miejsce w dniu lub po cenie 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres daty/godziny nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d3eca-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d3eca-133">Przykład 9: uzyskiwanie dziennika zdarzeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d3eca-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="d3eca-134">To polecenie wyświetla najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w ciągu 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-135">Przykład 10: uzyskiwanie dziennika zdarzeń dla grupy zasobów z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="d3eca-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="d3eca-136">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-137">Przykład 11: pobieranie dziennika zdarzeń dla grupy zasobów według czasu rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="d3eca-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="d3eca-138">To polecenie zawiera najwyżej 1000 Evetns skojarzone z określoną grupą zasobów, które miały miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-139">Przykład 12: pobieranie dziennika zdarzeń dla grupy zasobów z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="d3eca-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d3eca-140">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po cenie 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017em – 04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d3eca-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d3eca-141">Przykład 13: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d3eca-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="d3eca-142">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-143">Przykład 14: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="d3eca-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="d3eca-144">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-145">Przykład 15: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="d3eca-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="d3eca-146">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-147">Przykład 16: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="d3eca-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d3eca-148">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce w dniu lub po dniu 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d3eca-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d3eca-149">Przykład 17: uzyskiwanie dziennika zdarzeń według dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="d3eca-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="d3eca-150">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-151">Przykład 18: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="d3eca-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="d3eca-152">To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-153">Przykład 19: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów przy użyciu godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="d3eca-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="d3eca-154">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="d3eca-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d3eca-155">Przykład 20: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="d3eca-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d3eca-156">To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce w dniu lub po dniu 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d3eca-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="d3eca-157">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3eca-157">PARAMETERS</span></span>

### <span data-ttu-id="d3eca-158">— Rozmówca</span><span class="sxs-lookup"><span data-stu-id="d3eca-158">-Caller</span></span>
<span data-ttu-id="d3eca-159">Określa rozmówcę.</span><span class="sxs-lookup"><span data-stu-id="d3eca-159">Specifies a caller.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-160">-Identyfikator korelacji</span><span class="sxs-lookup"><span data-stu-id="d3eca-160">-CorrelationId</span></span>
<span data-ttu-id="d3eca-161">Określa identyfikator korelacji.</span><span class="sxs-lookup"><span data-stu-id="d3eca-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="d3eca-162">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d3eca-162">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: GetByCorrelationId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3eca-163">-DefaultProfile</span></span>
<span data-ttu-id="d3eca-164">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d3eca-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="d3eca-165">-DetailedOutput</span></span>
<span data-ttu-id="d3eca-166">Wskazuje, że w tym poleceniu cmdlet są wyświetlane szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="d3eca-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="d3eca-167">Domyślnie dane wyjściowe są sumowane.</span><span class="sxs-lookup"><span data-stu-id="d3eca-167">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d3eca-168">-EndTime</span></span>
<span data-ttu-id="d3eca-169">Określa godzinę zakończenia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="d3eca-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="d3eca-170">Wartość domyślna to bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="d3eca-170">The default value is the current time.</span></span>
<span data-ttu-id="d3eca-171">Wartość musi być późniejsza niż czas *rozpoczęcia*.</span><span class="sxs-lookup"><span data-stu-id="d3eca-171">The value must be later than *StartTime*.</span></span>

<span data-ttu-id="d3eca-172">Możesz użyć polecenia cmdlet Get-Date, aby uzyskać obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d3eca-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="d3eca-173">-MaxRecord</span></span>
<span data-ttu-id="d3eca-174">Określa całkowitą liczbę rekordów do pobrania dla określonego filtru.</span><span class="sxs-lookup"><span data-stu-id="d3eca-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="d3eca-175">Wartość domyślna to 1000, a maksymalna akceptowana wartość to 100000.</span><span class="sxs-lookup"><span data-stu-id="d3eca-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="d3eca-176">Wartości ujemne i 0 są ignorowane i zostanie wykorzystana wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="d3eca-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxRecords, MaxEvents

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3eca-177">-ResourceGroupName</span></span>
<span data-ttu-id="d3eca-178">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3eca-178">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3eca-179">-ResourceId</span></span>
<span data-ttu-id="d3eca-180">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d3eca-180">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d3eca-181">-ResourceProvider</span></span>
<span data-ttu-id="d3eca-182">Określa filtr według dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3eca-182">Specifies a filter by resource provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceProvider
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d3eca-183">-StartTime</span></span>
<span data-ttu-id="d3eca-184">Określa godzinę rozpoczęcia kwerendy w czasie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="d3eca-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="d3eca-185">Wartość domyślna to *Endtime* minus siedem dni.</span><span class="sxs-lookup"><span data-stu-id="d3eca-185">The default value is *EndTime* minus seven days.</span></span>

<span data-ttu-id="d3eca-186">Możesz użyć polecenia cmdlet Get-Date, aby uzyskać obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d3eca-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-187">-Status</span><span class="sxs-lookup"><span data-stu-id="d3eca-187">-Status</span></span>
<span data-ttu-id="d3eca-188">Określa stan.</span><span class="sxs-lookup"><span data-stu-id="d3eca-188">Specifies the status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eca-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3eca-189">CommonParameters</span></span>
<span data-ttu-id="d3eca-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3eca-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3eca-191">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3eca-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3eca-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3eca-192">INPUTS</span></span>

### <span data-ttu-id="d3eca-193">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d3eca-193">None</span></span>

### <span data-ttu-id="d3eca-194">Lista<Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData></span><span class="sxs-lookup"><span data-stu-id="d3eca-194">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData></span></span>

### <span data-ttu-id="d3eca-195">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d3eca-195">None</span></span>

## <span data-ttu-id="d3eca-196">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3eca-196">NOTES</span></span>

## <span data-ttu-id="d3eca-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3eca-197">RELATED LINKS</span></span>
