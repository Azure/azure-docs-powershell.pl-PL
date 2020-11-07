---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 83fab07a44dd85e000e86597881341cad6c641e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871975"
---
# <span data-ttu-id="a687e-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a687e-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a687e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a687e-102">SYNOPSIS</span></span>
<span data-ttu-id="a687e-103">Usuwa harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="a687e-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="a687e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a687e-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a687e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a687e-105">DESCRIPTION</span></span>
<span data-ttu-id="a687e-106">Polecenie cmdlet **Remove-AzRedisCachePatchSchedule** usuwa harmonogram poprawek z pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a687e-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a687e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a687e-107">EXAMPLES</span></span>

### <span data-ttu-id="a687e-108">Przykład 1: Usuwanie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="a687e-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a687e-109">To polecenie usuwa harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="a687e-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a687e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a687e-110">PARAMETERS</span></span>

### <span data-ttu-id="a687e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a687e-111">-DefaultProfile</span></span>
<span data-ttu-id="a687e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a687e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a687e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a687e-113">-Name</span></span>
<span data-ttu-id="a687e-114">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a687e-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a687e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a687e-115">-PassThru</span></span>
<span data-ttu-id="a687e-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a687e-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a687e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a687e-117">-ResourceGroupName</span></span>
<span data-ttu-id="a687e-118">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="a687e-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a687e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a687e-119">-Confirm</span></span>
<span data-ttu-id="a687e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a687e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a687e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a687e-121">-WhatIf</span></span>
<span data-ttu-id="a687e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a687e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a687e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a687e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a687e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a687e-124">CommonParameters</span></span>
<span data-ttu-id="a687e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a687e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a687e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a687e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a687e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a687e-127">INPUTS</span></span>

### <span data-ttu-id="a687e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a687e-128">System.String</span></span>

## <span data-ttu-id="a687e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a687e-129">OUTPUTS</span></span>

### <span data-ttu-id="a687e-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a687e-130">System.Boolean</span></span>

## <span data-ttu-id="a687e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a687e-131">NOTES</span></span>
* <span data-ttu-id="a687e-132">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="a687e-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a687e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a687e-133">RELATED LINKS</span></span>

[<span data-ttu-id="a687e-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a687e-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a687e-135">Nowe — AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a687e-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a687e-136">Nowe — AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a687e-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


