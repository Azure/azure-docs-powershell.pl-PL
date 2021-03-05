---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980202"
---
# <span data-ttu-id="bc0a7-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="bc0a7-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="bc0a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0a7-103">Pobieranie zdarzeń dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="bc0a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc0a7-104">SYNTAX</span></span>

### <span data-ttu-id="bc0a7-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="bc0a7-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc0a7-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc0a7-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc0a7-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bc0a7-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc0a7-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="bc0a7-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc0a7-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="bc0a7-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc0a7-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc0a7-110">DESCRIPTION</span></span>
<span data-ttu-id="bc0a7-111">Polecenie Get-AzActivityLog pobiera zdarzenia dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="bc0a7-112">Zdarzenia mogą być skojarzone z bieżącym identyfikatorem subskrypcji, identyfikatorem korelacji, grupą zasobów, identyfikatorem zasobu lub dostawcą zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="bc0a7-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc0a7-113">EXAMPLES</span></span>

### <span data-ttu-id="bc0a7-114">Przykład 1. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bc0a7-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzActivityLog
```

<span data-ttu-id="bc0a7-115">To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-116">Przykład 2. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="bc0a7-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="bc0a7-117">To polecenie zawiera listę co najwyżej 100 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-118">Przykład 3. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="bc0a7-119">To polecenie zawiera listę co najmniej 1000 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce w dniu lub po 06-06-01T10:30 czasu lokalnego, jeśli ta data/godzina nie jest starsza niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-120">Przykład 4. Uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="bc0a7-121">To polecenie wyświetla co najwyżej 1000 zdarzeń skojarzonych z identyfikatorem subskrypcji użytkownika, które miały miejsce w czasie lokalnym 2017-04-01T10:30 i przed godziną 2017-04-14T11:30, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, czyli okresu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="bc0a7-122">Przykład 5. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji</span><span class="sxs-lookup"><span data-stu-id="bc0a7-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="bc0a7-123">To polecenie wyszczególnia co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem korelacji, który miał miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="bc0a7-124">**UWAGA:** zazwyczaj jest to tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="bc0a7-125">Przykład 6. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="bc0a7-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="bc0a7-126">To polecenie wyszczególnia co najwyżej 100 zdarzeń skojarzonych z określonym identyfikatorem korelacji, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="bc0a7-127">**UWAGA:** zazwyczaj jest to tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="bc0a7-128">Przykład 7. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji i godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="bc0a7-129">To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem korelacji, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="bc0a7-130">**UWAGA:** zazwyczaj jest to tylko jedno zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="bc0a7-131">Przykład 8. Uzyskiwanie dziennika zdarzeń za pomocą identyfikatora korelacji z godziną rozpoczęcia i zakończenia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="bc0a7-132">To polecenie wyszczególnia co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem korelacji, który miał miejsce w czasie lokalnym 2017-04-15T04:30, ale przed godziną 2017-04-25T12:30 czasu lokalnego, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="bc0a7-133">Przykład 9. Uzyskiwanie dziennika zdarzeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bc0a7-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="bc0a7-134">To polecenie zawiera najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-135">Przykład 10. Uzyskiwanie dziennika zdarzeń dla grupy zasobów z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="bc0a7-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="bc0a7-136">To polecenie wyświetla listę co najwyżej 100 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-137">Przykład 11. Uzyskiwanie dziennika zdarzeń dla grupy zasobów według czasu rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="bc0a7-138">To polecenie wyświetla listę co najmniej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-139">Przykład 12. Uzyskiwanie dziennika zdarzeń dla grupy zasobów z godziną rozpoczęcia i zakończenia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="bc0a7-140">To polecenie zawiera listę co najmniej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w czasie lokalnym w godzinach 2017–04–15T04:30, ale przed godziną 2017-04-25T12:30, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="bc0a7-141">Przykład 13. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="bc0a7-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="bc0a7-142">To polecenie wyświetla listę co najwyżej 1000 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-143">Przykład 14. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="bc0a7-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="bc0a7-144">To polecenie zawiera listę co najwyżej 100 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-145">Przykład 15. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="bc0a7-146">To polecenie zawiera listę co najmniej 1000 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-147">Przykład 16. Uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia i godziną zakończenia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="bc0a7-148">To polecenie wyświetla listę co najmniej 1000 zdarzeń skojarzonych z określonym identyfikatorem zasobu, które miały miejsce w czasie lokalnym w godzinach 2017-04-15T04:30, ale przed godziną 2017-04-25T12:30 czasu lokalnego, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="bc0a7-149">Przykład 17. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="bc0a7-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="bc0a7-150">To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-151">Przykład 18. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów z maksymalną liczbą zdarzeń</span><span class="sxs-lookup"><span data-stu-id="bc0a7-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="bc0a7-152">To polecenie zawiera listę co najwyżej 100 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-153">Przykład 19. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów z godziną rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="bc0a7-154">To polecenie wyświetla listę co najmniej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce w dniu lub po 22T04:30:00 czasu lokalnego lub po nim, jeśli czas rozpoczęcia nie jest starszy niż 90 dni od bieżącej daty/godziny.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="bc0a7-155">Przykład 20. Uzyskiwanie dziennika zdarzeń według dostawcy zasobów z godziną rozpoczęcia i zakończenia</span><span class="sxs-lookup"><span data-stu-id="bc0a7-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="bc0a7-156">To polecenie zawiera listę co najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, które miały miejsce w czasie lokalnym w godzinach 2017-04-15T04:30, ale przed godziną 2017-04-25T12:30, jeśli cały zakres dat i godzin nie jest starszy niż 90 dni od bieżącej daty/godziny, to jest: okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="bc0a7-157">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc0a7-157">PARAMETERS</span></span>

### <span data-ttu-id="bc0a7-158">— wywołujący</span><span class="sxs-lookup"><span data-stu-id="bc0a7-158">-Caller</span></span>
<span data-ttu-id="bc0a7-159">Wywołujący zdarzenia do pobrania</span><span class="sxs-lookup"><span data-stu-id="bc0a7-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="bc0a7-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="bc0a7-160">-CorrelationId</span></span>
<span data-ttu-id="bc0a7-161">Identyfikator korelacji</span><span class="sxs-lookup"><span data-stu-id="bc0a7-161">The CorrelationId</span></span>

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

### <span data-ttu-id="bc0a7-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0a7-162">-DefaultProfile</span></span>
<span data-ttu-id="bc0a7-163">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc0a7-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="bc0a7-164">-DetailedOutput</span></span>
<span data-ttu-id="bc0a7-165">Zwróć obiekt ze wszystkimi szczegółami zdarzeń (domyślnie są zwracane tylko niektóre atrybuty, czyli bez szczegółów)</span><span class="sxs-lookup"><span data-stu-id="bc0a7-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="bc0a7-166">- EndTime</span><span class="sxs-lookup"><span data-stu-id="bc0a7-166">-EndTime</span></span>
<span data-ttu-id="bc0a7-167">Czas zakończenia kwerendy</span><span class="sxs-lookup"><span data-stu-id="bc0a7-167">The endTime of the query</span></span>

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

### <span data-ttu-id="bc0a7-168">- MaxRecord</span><span class="sxs-lookup"><span data-stu-id="bc0a7-168">-MaxRecord</span></span>
<span data-ttu-id="bc0a7-169">Maksymalna liczba rekordów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="bc0a7-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="bc0a7-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="bc0a7-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc0a7-171">-ResourceGroupName</span></span>
<span data-ttu-id="bc0a7-172">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bc0a7-172">The resource group name</span></span>

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

### <span data-ttu-id="bc0a7-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc0a7-173">-ResourceId</span></span>
<span data-ttu-id="bc0a7-174">The ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc0a7-174">The ResourceId</span></span>

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

### <span data-ttu-id="bc0a7-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="bc0a7-175">-ResourceProvider</span></span>
<span data-ttu-id="bc0a7-176">Nazwa zasobuProvider</span><span class="sxs-lookup"><span data-stu-id="bc0a7-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="bc0a7-177">— StartTime</span><span class="sxs-lookup"><span data-stu-id="bc0a7-177">-StartTime</span></span>
<span data-ttu-id="bc0a7-178">Identyfikator korelacji zapytania</span><span class="sxs-lookup"><span data-stu-id="bc0a7-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="bc0a7-179">— Status</span><span class="sxs-lookup"><span data-stu-id="bc0a7-179">-Status</span></span>
<span data-ttu-id="bc0a7-180">Stan zdarzeń do pobrania</span><span class="sxs-lookup"><span data-stu-id="bc0a7-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="bc0a7-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0a7-181">CommonParameters</span></span>
<span data-ttu-id="bc0a7-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0a7-183">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc0a7-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0a7-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc0a7-184">INPUTS</span></span>

### <span data-ttu-id="bc0a7-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc0a7-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc0a7-186">System.String</span><span class="sxs-lookup"><span data-stu-id="bc0a7-186">System.String</span></span>

### <span data-ttu-id="bc0a7-187">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="bc0a7-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bc0a7-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bc0a7-188">System.Int32</span></span>

## <span data-ttu-id="bc0a7-189">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc0a7-189">OUTPUTS</span></span>

### <span data-ttu-id="bc0a7-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="bc0a7-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="bc0a7-191">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc0a7-191">NOTES</span></span>

## <span data-ttu-id="bc0a7-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc0a7-192">RELATED LINKS</span></span>
