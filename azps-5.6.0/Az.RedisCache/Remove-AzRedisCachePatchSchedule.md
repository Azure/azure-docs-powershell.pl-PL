---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 42f91d45bf93f453e4c6368abaabcb64f9234771
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000938"
---
# <span data-ttu-id="2dd9a-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd9a-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="2dd9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd9a-103">Usuwa harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="2dd9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2dd9a-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd9a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2dd9a-105">DESCRIPTION</span></span>
<span data-ttu-id="2dd9a-106">Polecenie **cmdlet Remove-AzRedisCachePatchSchedule** usuwa harmonogram poprawek z pamięci podręcznej w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="2dd9a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2dd9a-107">EXAMPLES</span></span>

### <span data-ttu-id="2dd9a-108">Przykład 1. Usunięcie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="2dd9a-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="2dd9a-109">To polecenie usuwa harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="2dd9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dd9a-110">PARAMETERS</span></span>

### <span data-ttu-id="2dd9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd9a-111">-DefaultProfile</span></span>
<span data-ttu-id="2dd9a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dd9a-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2dd9a-113">-Name</span></span>
<span data-ttu-id="2dd9a-114">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="2dd9a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dd9a-115">-PassThru</span></span>
<span data-ttu-id="2dd9a-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2dd9a-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2dd9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="2dd9a-118">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="2dd9a-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dd9a-119">-Confirm</span></span>
<span data-ttu-id="2dd9a-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd9a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd9a-121">-WhatIf</span></span>
<span data-ttu-id="2dd9a-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd9a-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd9a-124">CommonParameters</span></span>
<span data-ttu-id="2dd9a-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd9a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dd9a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd9a-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd9a-127">INPUTS</span></span>

### <span data-ttu-id="2dd9a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2dd9a-128">System.String</span></span>

## <span data-ttu-id="2dd9a-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd9a-129">OUTPUTS</span></span>

### <span data-ttu-id="2dd9a-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2dd9a-130">System.Boolean</span></span>

## <span data-ttu-id="2dd9a-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2dd9a-131">NOTES</span></span>
* <span data-ttu-id="2dd9a-132">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="2dd9a-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2dd9a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd9a-133">RELATED LINKS</span></span>

[<span data-ttu-id="2dd9a-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd9a-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="2dd9a-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd9a-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="2dd9a-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="2dd9a-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


