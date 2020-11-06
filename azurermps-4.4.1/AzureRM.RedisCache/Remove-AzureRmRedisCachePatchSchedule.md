---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527326"
---
# <span data-ttu-id="90ba7-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90ba7-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="90ba7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="90ba7-103">Usuwa harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="90ba7-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90ba7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90ba7-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90ba7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="90ba7-106">Polecenie cmdlet **Remove-AzureRmRedisCachePatchSchedule** usuwa harmonogram poprawek z pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="90ba7-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="90ba7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="90ba7-108">Przykład 1: Usuwanie harmonogramu poprawek</span><span class="sxs-lookup"><span data-stu-id="90ba7-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="90ba7-109">To polecenie usuwa harmonogram poprawek z pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="90ba7-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="90ba7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90ba7-110">PARAMETERS</span></span>

### <span data-ttu-id="90ba7-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90ba7-111">-Name</span></span>
<span data-ttu-id="90ba7-112">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="90ba7-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="90ba7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ba7-113">-ResourceGroupName</span></span>
<span data-ttu-id="90ba7-114">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="90ba7-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="90ba7-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90ba7-115">-Confirm</span></span>
<span data-ttu-id="90ba7-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ba7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ba7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ba7-117">-WhatIf</span></span>
<span data-ttu-id="90ba7-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ba7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ba7-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90ba7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ba7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ba7-120">-DefaultProfile</span></span>
<span data-ttu-id="90ba7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90ba7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90ba7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ba7-122">CommonParameters</span></span>
<span data-ttu-id="90ba7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ba7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ba7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ba7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ba7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90ba7-125">INPUTS</span></span>

### <span data-ttu-id="90ba7-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90ba7-126">None</span></span>
<span data-ttu-id="90ba7-127">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="90ba7-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="90ba7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90ba7-128">OUTPUTS</span></span>

### <span data-ttu-id="90ba7-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90ba7-129">None</span></span>

## <span data-ttu-id="90ba7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90ba7-130">NOTES</span></span>
* <span data-ttu-id="90ba7-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="90ba7-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="90ba7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90ba7-132">RELATED LINKS</span></span>

[<span data-ttu-id="90ba7-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90ba7-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="90ba7-134">Nowe — AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90ba7-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="90ba7-135">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="90ba7-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


