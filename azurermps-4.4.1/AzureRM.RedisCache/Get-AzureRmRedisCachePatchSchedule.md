---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 1899a35f183f66fb938abe0c6492e826ad661e43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553780"
---
# <span data-ttu-id="621e3-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="621e3-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="621e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="621e3-102">SYNOPSIS</span></span>
<span data-ttu-id="621e3-103">Pobiera harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="621e3-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="621e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="621e3-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="621e3-105">DESCRIPTION</span></span>
<span data-ttu-id="621e3-106">Polecenie cmdlet **Get-AzureRmRedisCachePatchSchedule** pobiera harmonogram poprawek pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="621e3-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="621e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="621e3-107">EXAMPLES</span></span>

### <span data-ttu-id="621e3-108">Przykład 1: pobieranie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="621e3-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="621e3-109">To polecenie pobiera harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="621e3-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="621e3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="621e3-110">PARAMETERS</span></span>

### <span data-ttu-id="621e3-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="621e3-111">-Name</span></span>
<span data-ttu-id="621e3-112">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="621e3-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="621e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="621e3-114">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="621e3-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="621e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621e3-115">-DefaultProfile</span></span>
<span data-ttu-id="621e3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="621e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="621e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621e3-117">CommonParameters</span></span>
<span data-ttu-id="621e3-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621e3-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="621e3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621e3-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="621e3-120">INPUTS</span></span>

### <span data-ttu-id="621e3-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="621e3-121">None</span></span>
<span data-ttu-id="621e3-122">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="621e3-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="621e3-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="621e3-123">OUTPUTS</span></span>

### <span data-ttu-id="621e3-124">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="621e3-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="621e3-125">To polecenie cmdlet zwraca wpisy harmonogramu poprawek ustawione w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="621e3-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="621e3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="621e3-126">NOTES</span></span>
* <span data-ttu-id="621e3-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="621e3-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="621e3-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="621e3-128">RELATED LINKS</span></span>

[<span data-ttu-id="621e3-129">Nowe — AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="621e3-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="621e3-130">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="621e3-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="621e3-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="621e3-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


