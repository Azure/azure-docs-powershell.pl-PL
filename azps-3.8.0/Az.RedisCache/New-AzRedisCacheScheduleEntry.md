---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896090"
---
# <span data-ttu-id="b5868-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b5868-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="b5868-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5868-102">SYNOPSIS</span></span>
<span data-ttu-id="b5868-103">Tworzy wpis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="b5868-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="b5868-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5868-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5868-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5868-105">DESCRIPTION</span></span>
<span data-ttu-id="b5868-106">Polecenie cmdlet **New-AzRedisCacheScheduleEntry** tworzy obiekt **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="b5868-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="b5868-107">Polecenia cmdlet harmonogramu poprawek w pamięci podręcznej usługi Azure Redis, takie jak polecenie cmdlet New-AzRedisCachePatchSchedule, wymagają obiektów wpisów harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="b5868-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="b5868-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5868-108">EXAMPLES</span></span>

### <span data-ttu-id="b5868-109">Przykład 1. tworzenie wpisu harmonogramu dla weekendów</span><span class="sxs-lookup"><span data-stu-id="b5868-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="b5868-110">To polecenie tworzy obiekt **PSScheduleEntry** reprezentujący harmonogram weekendowy o określonej godzinie rozpoczęcia i oknie.</span><span class="sxs-lookup"><span data-stu-id="b5868-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="b5868-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5868-111">PARAMETERS</span></span>

### <span data-ttu-id="b5868-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b5868-112">-DayOfWeek</span></span>
<span data-ttu-id="b5868-113">Określa dzień tygodnia wpisu harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="b5868-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="b5868-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b5868-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5868-115">Codzienne</span><span class="sxs-lookup"><span data-stu-id="b5868-115">Everyday</span></span> 
- <span data-ttu-id="b5868-116">Weekend</span><span class="sxs-lookup"><span data-stu-id="b5868-116">Weekend</span></span> 
- <span data-ttu-id="b5868-117">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="b5868-117">Monday</span></span> 
- <span data-ttu-id="b5868-118">Wtorku</span><span class="sxs-lookup"><span data-stu-id="b5868-118">Tuesday</span></span> 
- <span data-ttu-id="b5868-119">Środa</span><span class="sxs-lookup"><span data-stu-id="b5868-119">Wednesday</span></span> 
- <span data-ttu-id="b5868-120">Czwartek</span><span class="sxs-lookup"><span data-stu-id="b5868-120">Thursday</span></span> 
- <span data-ttu-id="b5868-121">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="b5868-121">Friday</span></span> 
- <span data-ttu-id="b5868-122">Sobota</span><span class="sxs-lookup"><span data-stu-id="b5868-122">Saturday</span></span> 
- <span data-ttu-id="b5868-123">Niedziele</span><span class="sxs-lookup"><span data-stu-id="b5868-123">Sunday</span></span>

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

### <span data-ttu-id="b5868-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5868-124">-DefaultProfile</span></span>
<span data-ttu-id="b5868-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5868-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5868-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="b5868-126">-MaintenanceWindow</span></span>
<span data-ttu-id="b5868-127">Określa przedział czasu, w którym są dozwolone aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="b5868-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="b5868-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="b5868-128">-StartHourUtc</span></span>
<span data-ttu-id="b5868-129">Określa godzinę dnia rozpoczęcia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="b5868-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="b5868-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5868-130">CommonParameters</span></span>
<span data-ttu-id="b5868-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5868-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5868-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5868-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5868-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5868-133">INPUTS</span></span>

### <span data-ttu-id="b5868-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b5868-134">System.String</span></span>

### <span data-ttu-id="b5868-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b5868-135">System.Int32</span></span>

### <span data-ttu-id="b5868-136">System. Nullable "1 [[System. TimeSpan, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b5868-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b5868-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5868-137">OUTPUTS</span></span>

### <span data-ttu-id="b5868-138">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b5868-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="b5868-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5868-139">NOTES</span></span>
* <span data-ttu-id="b5868-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="b5868-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b5868-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5868-141">RELATED LINKS</span></span>

[<span data-ttu-id="b5868-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b5868-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b5868-143">Nowe — AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b5868-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b5868-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b5868-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


