---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717907"
---
# <span data-ttu-id="825f4-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="825f4-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="825f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="825f4-102">SYNOPSIS</span></span>
<span data-ttu-id="825f4-103">Usuwa harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="825f4-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="825f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="825f4-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="825f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="825f4-105">DESCRIPTION</span></span>
<span data-ttu-id="825f4-106">Polecenie cmdlet **Remove-AzureRmRedisCachePatchSchedule** usuwa harmonogram poprawek z pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="825f4-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="825f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="825f4-107">EXAMPLES</span></span>

### <span data-ttu-id="825f4-108">Przykład 1: Usuwanie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="825f4-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="825f4-109">To polecenie usuwa harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="825f4-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="825f4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="825f4-110">PARAMETERS</span></span>

### <span data-ttu-id="825f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825f4-111">-DefaultProfile</span></span>
<span data-ttu-id="825f4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="825f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="825f4-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="825f4-113">-Name</span></span>
<span data-ttu-id="825f4-114">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="825f4-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="825f4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="825f4-115">-PassThru</span></span>
<span data-ttu-id="825f4-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="825f4-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="825f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="825f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="825f4-118">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="825f4-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="825f4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="825f4-119">-Confirm</span></span>
<span data-ttu-id="825f4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="825f4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="825f4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="825f4-121">-WhatIf</span></span>
<span data-ttu-id="825f4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="825f4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="825f4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="825f4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="825f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825f4-124">CommonParameters</span></span>
<span data-ttu-id="825f4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825f4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825f4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825f4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="825f4-127">INPUTS</span></span>

### <span data-ttu-id="825f4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="825f4-128">System.String</span></span>

## <span data-ttu-id="825f4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="825f4-129">OUTPUTS</span></span>

### <span data-ttu-id="825f4-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="825f4-130">System.Boolean</span></span>

## <span data-ttu-id="825f4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="825f4-131">NOTES</span></span>
* <span data-ttu-id="825f4-132">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="825f4-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="825f4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="825f4-133">RELATED LINKS</span></span>

[<span data-ttu-id="825f4-134">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="825f4-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="825f4-135">Nowe — AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="825f4-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="825f4-136">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="825f4-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


