---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524974"
---
# <span data-ttu-id="7baf8-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7baf8-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="7baf8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7baf8-102">SYNOPSIS</span></span>
<span data-ttu-id="7baf8-103">Dodaje Harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="7baf8-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7baf8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7baf8-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7baf8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7baf8-105">DESCRIPTION</span></span>
<span data-ttu-id="7baf8-106">Polecenie cmdlet **New-AzureRmRedisCachePatchSchedule** umożliwia dodanie harmonogramu poprawek do pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7baf8-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="7baf8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7baf8-107">EXAMPLES</span></span>

### <span data-ttu-id="7baf8-108">Przykład 1: Tworzenie i Dodawanie harmonogramu poprawek w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="7baf8-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="7baf8-109">To polecenie dodaje Harmonogram poprawek do pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="7baf8-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="7baf8-110">Parametr wpisy przyjmuje jako wartość polecenie, które używa polecenia **New-AzureRmRedisCacheScheduleEntry** w celu utworzenia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="7baf8-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="7baf8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7baf8-111">PARAMETERS</span></span>

### <span data-ttu-id="7baf8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baf8-112">-DefaultProfile</span></span>
<span data-ttu-id="7baf8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7baf8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7baf8-114">-Wpisy</span><span class="sxs-lookup"><span data-stu-id="7baf8-114">-Entries</span></span>
<span data-ttu-id="7baf8-115">Określa tablicę harmonogramów ustawianych przez to polecenie cmdlet w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="7baf8-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="7baf8-116">Aby uzyskać obiekt **PSScheduleEntry** , użyj polecenia cmdlet New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="7baf8-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7baf8-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7baf8-117">-Name</span></span>
<span data-ttu-id="7baf8-118">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="7baf8-118">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7baf8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7baf8-119">-ResourceGroupName</span></span>
<span data-ttu-id="7baf8-120">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="7baf8-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="7baf8-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7baf8-121">-Confirm</span></span>
<span data-ttu-id="7baf8-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7baf8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baf8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7baf8-123">-WhatIf</span></span>
<span data-ttu-id="7baf8-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7baf8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7baf8-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7baf8-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baf8-126">CommonParameters</span></span>
<span data-ttu-id="7baf8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7baf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baf8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7baf8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baf8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7baf8-129">INPUTS</span></span>

### <span data-ttu-id="7baf8-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7baf8-130">None</span></span>
<span data-ttu-id="7baf8-131">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="7baf8-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7baf8-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7baf8-132">OUTPUTS</span></span>

### <span data-ttu-id="7baf8-133">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7baf8-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="7baf8-134">To polecenie cmdlet zwraca wpisy harmonogramu poprawek ustawione w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="7baf8-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="7baf8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7baf8-135">NOTES</span></span>
* <span data-ttu-id="7baf8-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="7baf8-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7baf8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7baf8-137">RELATED LINKS</span></span>

[<span data-ttu-id="7baf8-138">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7baf8-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="7baf8-139">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7baf8-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="7baf8-140">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7baf8-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


