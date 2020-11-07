---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: ac1184dcdcc55a0b5cac28f996c29c3476ba3613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718283"
---
# <span data-ttu-id="a3709-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a3709-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a3709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3709-102">SYNOPSIS</span></span>
<span data-ttu-id="a3709-103">Pobiera harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="a3709-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3709-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3709-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3709-105">DESCRIPTION</span></span>
<span data-ttu-id="a3709-106">Polecenie cmdlet **Get-AzureRmRedisCachePatchSchedule** pobiera harmonogram poprawek pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a3709-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a3709-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3709-107">EXAMPLES</span></span>

### <span data-ttu-id="a3709-108">Przykład 1: pobieranie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="a3709-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a3709-109">To polecenie pobiera harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="a3709-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a3709-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3709-110">PARAMETERS</span></span>

### <span data-ttu-id="a3709-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3709-111">-DefaultProfile</span></span>
<span data-ttu-id="a3709-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3709-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3709-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3709-113">-Name</span></span>
<span data-ttu-id="a3709-114">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a3709-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a3709-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3709-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3709-116">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="a3709-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a3709-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3709-117">CommonParameters</span></span>
<span data-ttu-id="a3709-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3709-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3709-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3709-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3709-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3709-120">INPUTS</span></span>

### <span data-ttu-id="a3709-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a3709-121">System.String</span></span>

## <span data-ttu-id="a3709-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3709-122">OUTPUTS</span></span>

### <span data-ttu-id="a3709-123">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a3709-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="a3709-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3709-124">NOTES</span></span>
* <span data-ttu-id="a3709-125">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="a3709-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a3709-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3709-126">RELATED LINKS</span></span>

[<span data-ttu-id="a3709-127">Nowe — AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a3709-127">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a3709-128">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a3709-128">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="a3709-129">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a3709-129">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


