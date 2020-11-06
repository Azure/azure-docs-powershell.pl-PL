---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 07bfc520cfabc33ed4f72f1d0d4c46c9104a5253
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527341"
---
# <span data-ttu-id="156d0-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="156d0-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="156d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="156d0-102">SYNOPSIS</span></span>
<span data-ttu-id="156d0-103">Tworzy wpis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="156d0-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="156d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="156d0-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="156d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="156d0-105">DESCRIPTION</span></span>
<span data-ttu-id="156d0-106">Polecenie cmdlet **New-AzureRmRedisCacheScheduleEntry** tworzy obiekt **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="156d0-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="156d0-107">Polecenia cmdlet harmonogramu poprawek w pamięci podręcznej usługi Azure Redis, takie jak polecenie cmdlet New-AzureRmRedisCachePatchSchedule, wymagają obiektów wpisów harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="156d0-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="156d0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="156d0-108">EXAMPLES</span></span>

### <span data-ttu-id="156d0-109">Przykład 1. tworzenie wpisu harmonogramu dla weekendów</span><span class="sxs-lookup"><span data-stu-id="156d0-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="156d0-110">To polecenie tworzy obiekt **PSScheduleEntry** reprezentujący harmonogram weekendowy o określonej godzinie rozpoczęcia i oknie.</span><span class="sxs-lookup"><span data-stu-id="156d0-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="156d0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="156d0-111">PARAMETERS</span></span>

### <span data-ttu-id="156d0-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="156d0-112">-DayOfWeek</span></span>
<span data-ttu-id="156d0-113">Określa dzień tygodnia wpisu harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="156d0-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="156d0-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="156d0-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="156d0-115">Codzienne</span><span class="sxs-lookup"><span data-stu-id="156d0-115">Everyday</span></span> 
- <span data-ttu-id="156d0-116">Weekend</span><span class="sxs-lookup"><span data-stu-id="156d0-116">Weekend</span></span> 
- <span data-ttu-id="156d0-117">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="156d0-117">Monday</span></span> 
- <span data-ttu-id="156d0-118">Wtorku</span><span class="sxs-lookup"><span data-stu-id="156d0-118">Tuesday</span></span> 
- <span data-ttu-id="156d0-119">Środa</span><span class="sxs-lookup"><span data-stu-id="156d0-119">Wednesday</span></span> 
- <span data-ttu-id="156d0-120">Czwartek</span><span class="sxs-lookup"><span data-stu-id="156d0-120">Thursday</span></span> 
- <span data-ttu-id="156d0-121">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="156d0-121">Friday</span></span> 
- <span data-ttu-id="156d0-122">Sobota</span><span class="sxs-lookup"><span data-stu-id="156d0-122">Saturday</span></span> 
- <span data-ttu-id="156d0-123">Niedziele</span><span class="sxs-lookup"><span data-stu-id="156d0-123">Sunday</span></span>

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

### <span data-ttu-id="156d0-124">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="156d0-124">-MaintenanceWindow</span></span>
<span data-ttu-id="156d0-125">Określa przedział czasu, w którym są dozwolone aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="156d0-125">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="156d0-126">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="156d0-126">-StartHourUtc</span></span>
<span data-ttu-id="156d0-127">Określa godzinę dnia rozpoczęcia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="156d0-127">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="156d0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156d0-128">-DefaultProfile</span></span>
<span data-ttu-id="156d0-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="156d0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156d0-130">CommonParameters</span></span>
<span data-ttu-id="156d0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156d0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156d0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156d0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="156d0-133">INPUTS</span></span>

### <span data-ttu-id="156d0-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="156d0-134">None</span></span>
<span data-ttu-id="156d0-135">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="156d0-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="156d0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="156d0-136">OUTPUTS</span></span>

### <span data-ttu-id="156d0-137">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="156d0-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="156d0-138">To polecenie cmdlet zwraca obiekt wpisu harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="156d0-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="156d0-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="156d0-139">NOTES</span></span>
* <span data-ttu-id="156d0-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="156d0-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="156d0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="156d0-141">RELATED LINKS</span></span>

[<span data-ttu-id="156d0-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="156d0-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="156d0-143">Nowe — AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="156d0-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="156d0-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="156d0-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


