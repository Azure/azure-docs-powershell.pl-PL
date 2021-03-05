---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 297966fe0ad59948fd321ec52cf066ad5caa3d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008657"
---
# <span data-ttu-id="bbd02-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd02-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="bbd02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd02-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd02-103">Otrzymuje harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="bbd02-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="bbd02-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bbd02-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbd02-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bbd02-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd02-106">Polecenie **cmdlet Get-AzRedisCachePatchSchedule** pobiera harmonogram poprawek dla pamięci podręcznej w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="bbd02-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="bbd02-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bbd02-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd02-108">Przykład 1. Pobierz harmonogram poprawek</span><span class="sxs-lookup"><span data-stu-id="bbd02-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="bbd02-109">To polecenie pobiera harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="bbd02-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="bbd02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd02-110">PARAMETERS</span></span>

### <span data-ttu-id="bbd02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd02-111">-DefaultProfile</span></span>
<span data-ttu-id="bbd02-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd02-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd02-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bbd02-113">-Name</span></span>
<span data-ttu-id="bbd02-114">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="bbd02-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="bbd02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd02-115">-ResourceGroupName</span></span>
<span data-ttu-id="bbd02-116">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="bbd02-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="bbd02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd02-117">CommonParameters</span></span>
<span data-ttu-id="bbd02-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd02-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd02-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd02-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbd02-120">INPUTS</span></span>

### <span data-ttu-id="bbd02-121">System.String</span><span class="sxs-lookup"><span data-stu-id="bbd02-121">System.String</span></span>

## <span data-ttu-id="bbd02-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbd02-122">OUTPUTS</span></span>

### <span data-ttu-id="bbd02-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="bbd02-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="bbd02-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bbd02-124">NOTES</span></span>
* <span data-ttu-id="bbd02-125">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="bbd02-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bbd02-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbd02-126">RELATED LINKS</span></span>

[<span data-ttu-id="bbd02-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd02-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="bbd02-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="bbd02-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="bbd02-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd02-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


