---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336469"
---
# <span data-ttu-id="5016e-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="5016e-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="5016e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5016e-102">SYNOPSIS</span></span>
<span data-ttu-id="5016e-103">Pobiera harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="5016e-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="5016e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5016e-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5016e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5016e-105">DESCRIPTION</span></span>
<span data-ttu-id="5016e-106">Polecenie cmdlet **Get-AzRedisCachePatchSchedule** pobiera harmonogram poprawek pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="5016e-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="5016e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5016e-107">EXAMPLES</span></span>

### <span data-ttu-id="5016e-108">Przykład 1: pobieranie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="5016e-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="5016e-109">To polecenie pobiera harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="5016e-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="5016e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5016e-110">PARAMETERS</span></span>

### <span data-ttu-id="5016e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5016e-111">-DefaultProfile</span></span>
<span data-ttu-id="5016e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5016e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5016e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5016e-113">-Name</span></span>
<span data-ttu-id="5016e-114">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="5016e-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="5016e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5016e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5016e-116">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="5016e-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="5016e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5016e-117">CommonParameters</span></span>
<span data-ttu-id="5016e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5016e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5016e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5016e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5016e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5016e-120">INPUTS</span></span>

### <span data-ttu-id="5016e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5016e-121">System.String</span></span>

## <span data-ttu-id="5016e-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5016e-122">OUTPUTS</span></span>

### <span data-ttu-id="5016e-123">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="5016e-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="5016e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5016e-124">NOTES</span></span>
* <span data-ttu-id="5016e-125">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="5016e-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="5016e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5016e-126">RELATED LINKS</span></span>

[<span data-ttu-id="5016e-127">Nowe — AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="5016e-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="5016e-128">Nowe — AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="5016e-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="5016e-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="5016e-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


