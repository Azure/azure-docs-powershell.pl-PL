---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 367327e19ff95132b7b7d6bc2d86970892ab6e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886541"
---
# <span data-ttu-id="35ddc-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="35ddc-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="35ddc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="35ddc-103">Dodaje Harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="35ddc-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="35ddc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35ddc-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ddc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="35ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="35ddc-106">Polecenie cmdlet **New-AzRedisCachePatchSchedule** umożliwia dodanie harmonogramu poprawek do pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="35ddc-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="35ddc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35ddc-107">EXAMPLES</span></span>

### <span data-ttu-id="35ddc-108">Przykład 1: Tworzenie i Dodawanie harmonogramu poprawek w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="35ddc-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="35ddc-109">To polecenie dodaje Harmonogram poprawek do pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="35ddc-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="35ddc-110">Parametr wpisy przyjmuje jako wartość polecenie, które używa polecenia **New-AzRedisCacheScheduleEntry** w celu utworzenia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="35ddc-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="35ddc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35ddc-111">PARAMETERS</span></span>

### <span data-ttu-id="35ddc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ddc-112">-DefaultProfile</span></span>
<span data-ttu-id="35ddc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35ddc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35ddc-114">-Wpisy</span><span class="sxs-lookup"><span data-stu-id="35ddc-114">-Entries</span></span>
<span data-ttu-id="35ddc-115">Określa tablicę harmonogramów ustawianych przez to polecenie cmdlet w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="35ddc-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="35ddc-116">Aby uzyskać obiekt **PSScheduleEntry** , użyj polecenia cmdlet New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="35ddc-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="35ddc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35ddc-117">-Name</span></span>
<span data-ttu-id="35ddc-118">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="35ddc-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="35ddc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ddc-119">-ResourceGroupName</span></span>
<span data-ttu-id="35ddc-120">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="35ddc-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="35ddc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35ddc-121">-Confirm</span></span>
<span data-ttu-id="35ddc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ddc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ddc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ddc-123">-WhatIf</span></span>
<span data-ttu-id="35ddc-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ddc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35ddc-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35ddc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ddc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ddc-126">CommonParameters</span></span>
<span data-ttu-id="35ddc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ddc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ddc-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ddc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ddc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35ddc-129">INPUTS</span></span>

### <span data-ttu-id="35ddc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="35ddc-130">System.String</span></span>

### <span data-ttu-id="35ddc-131">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="35ddc-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="35ddc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35ddc-132">OUTPUTS</span></span>

### <span data-ttu-id="35ddc-133">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="35ddc-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="35ddc-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35ddc-134">NOTES</span></span>
* <span data-ttu-id="35ddc-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="35ddc-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="35ddc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35ddc-136">RELATED LINKS</span></span>

[<span data-ttu-id="35ddc-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="35ddc-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="35ddc-138">Nowe — AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="35ddc-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="35ddc-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="35ddc-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


