---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: ebc51005bcffdde2ad5f64764e90440e8d1e7583
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961722"
---
# <span data-ttu-id="d5ea3-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d5ea3-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="d5ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ea3-103">Dodaje harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="d5ea3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5ea3-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5ea3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ea3-106">Polecenie **cmdlet New-AzRedisCachePatchSchedule** dodaje harmonogram poprawek do pamięci podręcznej w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="d5ea3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="d5ea3-108">Przykład 1. Tworzenie i dodawanie harmonogramu poprawek w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="d5ea3-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="d5ea3-109">To polecenie dodaje harmonogram poprawek do pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="d5ea3-110">Parametr Entries przyjmuje jako wartość polecenie, które tworzy harmonogram za pomocą polecenia **New-AzRedisCacheScheduleEntry.**</span><span class="sxs-lookup"><span data-stu-id="d5ea3-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="d5ea3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5ea3-111">PARAMETERS</span></span>

### <span data-ttu-id="d5ea3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ea3-112">-DefaultProfile</span></span>
<span data-ttu-id="d5ea3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5ea3-114">— Wpisy</span><span class="sxs-lookup"><span data-stu-id="d5ea3-114">-Entries</span></span>
<span data-ttu-id="d5ea3-115">Określa tablicę harmonogramów ustawianych przez to polecenie cmdlet w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="d5ea3-116">Aby uzyskać **obiekt PSScheduleEntry,** użyj New-AzRedisCacheScheduleEntry cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="d5ea3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5ea3-117">-Name</span></span>
<span data-ttu-id="d5ea3-118">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d5ea3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ea3-119">-ResourceGroupName</span></span>
<span data-ttu-id="d5ea3-120">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="d5ea3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5ea3-121">-Confirm</span></span>
<span data-ttu-id="d5ea3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ea3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ea3-123">-WhatIf</span></span>
<span data-ttu-id="d5ea3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5ea3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ea3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ea3-126">CommonParameters</span></span>
<span data-ttu-id="d5ea3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ea3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ea3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ea3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ea3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5ea3-129">INPUTS</span></span>

### <span data-ttu-id="d5ea3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d5ea3-130">System.String</span></span>

### <span data-ttu-id="d5ea3-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="d5ea3-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="d5ea3-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5ea3-132">OUTPUTS</span></span>

### <span data-ttu-id="d5ea3-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d5ea3-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="d5ea3-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5ea3-134">NOTES</span></span>
* <span data-ttu-id="d5ea3-135">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="d5ea3-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d5ea3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5ea3-136">RELATED LINKS</span></span>

[<span data-ttu-id="d5ea3-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d5ea3-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="d5ea3-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d5ea3-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="d5ea3-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d5ea3-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


