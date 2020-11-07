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
ms.locfileid: "93708509"
---
# <span data-ttu-id="cb53e-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cb53e-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="cb53e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb53e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb53e-103">Dodaje Harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="cb53e-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="cb53e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb53e-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb53e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cb53e-105">DESCRIPTION</span></span>
<span data-ttu-id="cb53e-106">Polecenie cmdlet **New-AzRedisCachePatchSchedule** umożliwia dodanie harmonogramu poprawek do pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="cb53e-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="cb53e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb53e-107">EXAMPLES</span></span>

### <span data-ttu-id="cb53e-108">Przykład 1: Tworzenie i Dodawanie harmonogramu poprawek w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="cb53e-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="cb53e-109">To polecenie dodaje Harmonogram poprawek do pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="cb53e-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="cb53e-110">Parametr wpisy przyjmuje jako wartość polecenie, które używa polecenia **New-AzRedisCacheScheduleEntry** w celu utworzenia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="cb53e-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="cb53e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb53e-111">PARAMETERS</span></span>

### <span data-ttu-id="cb53e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb53e-112">-DefaultProfile</span></span>
<span data-ttu-id="cb53e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb53e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb53e-114">-Wpisy</span><span class="sxs-lookup"><span data-stu-id="cb53e-114">-Entries</span></span>
<span data-ttu-id="cb53e-115">Określa tablicę harmonogramów ustawianych przez to polecenie cmdlet w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="cb53e-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="cb53e-116">Aby uzyskać obiekt **PSScheduleEntry** , użyj polecenia cmdlet New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="cb53e-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="cb53e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb53e-117">-Name</span></span>
<span data-ttu-id="cb53e-118">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="cb53e-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="cb53e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb53e-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb53e-120">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="cb53e-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="cb53e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb53e-121">-Confirm</span></span>
<span data-ttu-id="cb53e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb53e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb53e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb53e-123">-WhatIf</span></span>
<span data-ttu-id="cb53e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb53e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb53e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb53e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb53e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb53e-126">CommonParameters</span></span>
<span data-ttu-id="cb53e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb53e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb53e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb53e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb53e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb53e-129">INPUTS</span></span>

### <span data-ttu-id="cb53e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cb53e-130">System.String</span></span>

### <span data-ttu-id="cb53e-131">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="cb53e-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="cb53e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb53e-132">OUTPUTS</span></span>

### <span data-ttu-id="cb53e-133">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="cb53e-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="cb53e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb53e-134">NOTES</span></span>
* <span data-ttu-id="cb53e-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="cb53e-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="cb53e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb53e-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb53e-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cb53e-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="cb53e-138">Nowe — AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="cb53e-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="cb53e-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cb53e-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


