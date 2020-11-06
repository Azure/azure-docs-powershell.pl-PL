---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 9921cc32530c712f3a1ca69d81b07fa8117ba80a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550248"
---
# <span data-ttu-id="a6eed-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a6eed-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a6eed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6eed-102">SYNOPSIS</span></span>
<span data-ttu-id="a6eed-103">Dodaje Harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="a6eed-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6eed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6eed-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6eed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6eed-105">DESCRIPTION</span></span>
<span data-ttu-id="a6eed-106">Polecenie cmdlet **New-AzureRmRedisCachePatchSchedule** umożliwia dodanie harmonogramu poprawek do pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a6eed-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a6eed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6eed-107">EXAMPLES</span></span>

### <span data-ttu-id="a6eed-108">Przykład 1: Tworzenie i Dodawanie harmonogramu poprawek w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="a6eed-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="a6eed-109">To polecenie dodaje Harmonogram poprawek do pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="a6eed-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="a6eed-110">Parametr wpisy przyjmuje jako wartość polecenie, które używa polecenia **New-AzureRmRedisCacheScheduleEntry** w celu utworzenia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="a6eed-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="a6eed-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6eed-111">PARAMETERS</span></span>

### <span data-ttu-id="a6eed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6eed-112">-DefaultProfile</span></span>
<span data-ttu-id="a6eed-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6eed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6eed-114">-Wpisy</span><span class="sxs-lookup"><span data-stu-id="a6eed-114">-Entries</span></span>
<span data-ttu-id="a6eed-115">Określa tablicę harmonogramów ustawianych przez to polecenie cmdlet w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a6eed-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="a6eed-116">Aby uzyskać obiekt **PSScheduleEntry** , użyj polecenia cmdlet New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="a6eed-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6eed-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6eed-117">-Name</span></span>
<span data-ttu-id="a6eed-118">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a6eed-118">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6eed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6eed-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6eed-120">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="a6eed-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a6eed-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6eed-121">-Confirm</span></span>
<span data-ttu-id="a6eed-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6eed-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6eed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6eed-123">-WhatIf</span></span>
<span data-ttu-id="a6eed-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6eed-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6eed-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6eed-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6eed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6eed-126">CommonParameters</span></span>
<span data-ttu-id="a6eed-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6eed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6eed-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6eed-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6eed-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6eed-129">INPUTS</span></span>

### <span data-ttu-id="a6eed-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a6eed-130">System.String</span></span>

### <span data-ttu-id="a6eed-131">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="a6eed-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="a6eed-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6eed-132">OUTPUTS</span></span>

### <span data-ttu-id="a6eed-133">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a6eed-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="a6eed-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6eed-134">NOTES</span></span>
* <span data-ttu-id="a6eed-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="a6eed-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a6eed-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6eed-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6eed-137">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a6eed-137">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a6eed-138">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a6eed-138">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="a6eed-139">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a6eed-139">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


