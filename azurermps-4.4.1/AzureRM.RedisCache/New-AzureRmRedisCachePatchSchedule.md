---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716888"
---
# <span data-ttu-id="b41d9-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b41d9-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="b41d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b41d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b41d9-103">Dodaje Harmonogram poprawek.</span><span class="sxs-lookup"><span data-stu-id="b41d9-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b41d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b41d9-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b41d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b41d9-105">DESCRIPTION</span></span>
<span data-ttu-id="b41d9-106">Polecenie cmdlet **New-AzureRmRedisCachePatchSchedule** umożliwia dodanie harmonogramu poprawek do pamięci podręcznej w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="b41d9-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="b41d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b41d9-107">EXAMPLES</span></span>

### <span data-ttu-id="b41d9-108">Przykład 1: Tworzenie i Dodawanie harmonogramu poprawek w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="b41d9-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="b41d9-109">To polecenie dodaje Harmonogram poprawek do pamięci podręcznej o nazwie RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="b41d9-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="b41d9-110">Parametr wpisy przyjmuje jako wartość polecenie, które używa polecenia **New-AzureRmRedisCacheScheduleEntry** w celu utworzenia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="b41d9-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="b41d9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b41d9-111">PARAMETERS</span></span>

### <span data-ttu-id="b41d9-112">-Wpisy</span><span class="sxs-lookup"><span data-stu-id="b41d9-112">-Entries</span></span>
<span data-ttu-id="b41d9-113">Określa tablicę harmonogramów ustawianych przez to polecenie cmdlet w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b41d9-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="b41d9-114">Aby uzyskać obiekt **PSScheduleEntry** , użyj polecenia cmdlet New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="b41d9-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="b41d9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b41d9-115">-Name</span></span>
<span data-ttu-id="b41d9-116">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b41d9-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="b41d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="b41d9-118">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="b41d9-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="b41d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41d9-119">-DefaultProfile</span></span>
<span data-ttu-id="b41d9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b41d9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b41d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41d9-121">CommonParameters</span></span>
<span data-ttu-id="b41d9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41d9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41d9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41d9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b41d9-124">INPUTS</span></span>

### <span data-ttu-id="b41d9-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b41d9-125">None</span></span>
<span data-ttu-id="b41d9-126">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="b41d9-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b41d9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b41d9-127">OUTPUTS</span></span>

### <span data-ttu-id="b41d9-128">Microsoft. Azure. Commands. RedisCache. models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b41d9-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="b41d9-129">To polecenie cmdlet zwraca wpisy harmonogramu poprawek ustawione w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b41d9-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="b41d9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b41d9-130">NOTES</span></span>
* <span data-ttu-id="b41d9-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="b41d9-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b41d9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b41d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b41d9-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b41d9-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="b41d9-134">Nowe — AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b41d9-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="b41d9-135">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b41d9-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


