---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221670"
---
# <span data-ttu-id="9a4c5-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9a4c5-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="9a4c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4c5-103">Tworzy wpis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="9a4c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a4c5-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a4c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4c5-106">Polecenie cmdlet **New-AzRedisCacheScheduleEntry** tworzy obiekt **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="9a4c5-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="9a4c5-107">Polecenia cmdlet harmonogramu poprawek w pamięci podręcznej usługi Azure Redis, takie jak polecenie cmdlet New-AzRedisCachePatchSchedule, wymagają obiektów wpisów harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="9a4c5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a4c5-108">EXAMPLES</span></span>

### <span data-ttu-id="9a4c5-109">Przykład 1. tworzenie wpisu harmonogramu dla weekendów</span><span class="sxs-lookup"><span data-stu-id="9a4c5-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="9a4c5-110">To polecenie tworzy obiekt **PSScheduleEntry** reprezentujący harmonogram weekendowy o określonej godzinie rozpoczęcia i oknie.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="9a4c5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a4c5-111">PARAMETERS</span></span>

### <span data-ttu-id="9a4c5-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9a4c5-112">-DayOfWeek</span></span>
<span data-ttu-id="9a4c5-113">Określa dzień tygodnia wpisu harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="9a4c5-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9a4c5-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a4c5-115">Codzienne</span><span class="sxs-lookup"><span data-stu-id="9a4c5-115">Everyday</span></span> 
- <span data-ttu-id="9a4c5-116">Weekend</span><span class="sxs-lookup"><span data-stu-id="9a4c5-116">Weekend</span></span> 
- <span data-ttu-id="9a4c5-117">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="9a4c5-117">Monday</span></span> 
- <span data-ttu-id="9a4c5-118">Wtorku</span><span class="sxs-lookup"><span data-stu-id="9a4c5-118">Tuesday</span></span> 
- <span data-ttu-id="9a4c5-119">Środa</span><span class="sxs-lookup"><span data-stu-id="9a4c5-119">Wednesday</span></span> 
- <span data-ttu-id="9a4c5-120">Czwartek</span><span class="sxs-lookup"><span data-stu-id="9a4c5-120">Thursday</span></span> 
- <span data-ttu-id="9a4c5-121">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="9a4c5-121">Friday</span></span> 
- <span data-ttu-id="9a4c5-122">Sobota</span><span class="sxs-lookup"><span data-stu-id="9a4c5-122">Saturday</span></span> 
- <span data-ttu-id="9a4c5-123">Niedziele</span><span class="sxs-lookup"><span data-stu-id="9a4c5-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4c5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4c5-124">-DefaultProfile</span></span>
<span data-ttu-id="9a4c5-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a4c5-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="9a4c5-126">-MaintenanceWindow</span></span>
<span data-ttu-id="9a4c5-127">Określa przedział czasu, w którym są dozwolone aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4c5-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="9a4c5-128">-StartHourUtc</span></span>
<span data-ttu-id="9a4c5-129">Określa godzinę dnia rozpoczęcia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4c5-130">CommonParameters</span></span>
<span data-ttu-id="9a4c5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4c5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4c5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4c5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a4c5-133">INPUTS</span></span>

### <span data-ttu-id="9a4c5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9a4c5-134">System.String</span></span>

### <span data-ttu-id="9a4c5-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9a4c5-135">System.Int32</span></span>

### <span data-ttu-id="9a4c5-136">System. Nullable "1 [[System. TimeSpan, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9a4c5-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9a4c5-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a4c5-137">OUTPUTS</span></span>

### <span data-ttu-id="9a4c5-138">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9a4c5-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="9a4c5-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a4c5-139">NOTES</span></span>
* <span data-ttu-id="9a4c5-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="9a4c5-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9a4c5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a4c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="9a4c5-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4c5-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9a4c5-143">Nowe — AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4c5-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9a4c5-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9a4c5-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


