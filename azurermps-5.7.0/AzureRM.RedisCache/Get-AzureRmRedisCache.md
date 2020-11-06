---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544191"
---
# <span data-ttu-id="77857-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="77857-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="77857-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77857-102">SYNOPSIS</span></span>
<span data-ttu-id="77857-103">Pobiera pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="77857-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77857-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77857-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77857-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77857-105">DESCRIPTION</span></span>
<span data-ttu-id="77857-106">Polecenie cmdlet **Get-AzureRmRedisCache** pobiera określoną pamięć podręczną usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="77857-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="77857-107">Jeśli nie określisz żadnych parametrów, ta operacja będzie pobierać wszystkie Redis pamięci podręcznej dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="77857-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="77857-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77857-108">EXAMPLES</span></span>

### <span data-ttu-id="77857-109">Przykład 1: uzyskiwanie pamięci podręcznej Redis według nazwy</span><span class="sxs-lookup"><span data-stu-id="77857-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="77857-110">To polecenie pobiera pamięć podręczną Redis o nazwie Existing.</span><span class="sxs-lookup"><span data-stu-id="77857-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="77857-111">Przykład 2: pobieranie wszystkich Redis pamięci podręcznej w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="77857-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="77857-112">To polecenie pobiera wszystkie Redis pamięci podręcznej w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="77857-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="77857-113">Przykład 3: Uzyskaj co Redis pamięć podręczną w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="77857-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="77857-114">To polecenie pobiera wszystkie Redis pamięci podręcznej w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="77857-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="77857-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77857-115">PARAMETERS</span></span>

### <span data-ttu-id="77857-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77857-116">-DefaultProfile</span></span>
<span data-ttu-id="77857-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77857-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77857-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77857-118">-Name</span></span>
<span data-ttu-id="77857-119">Określa nazwę pamięci podręcznej Redis, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="77857-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="77857-120">Używany z parametrem *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="77857-120">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77857-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77857-121">-ResourceGroupName</span></span>
<span data-ttu-id="77857-122">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="77857-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="77857-123">Jeśli określisz tylko parametr *ResourceGroupName* , ta operacja pobiera wszystkie Redis pamięci podręcznej w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="77857-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77857-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77857-124">CommonParameters</span></span>
<span data-ttu-id="77857-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77857-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77857-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77857-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77857-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77857-127">INPUTS</span></span>

### <span data-ttu-id="77857-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77857-128">None</span></span>
<span data-ttu-id="77857-129">Możesz popotokować dane wejściowe tego polecenia cmdlet za pomocą nazwy, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="77857-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="77857-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77857-130">OUTPUTS</span></span>

### <span data-ttu-id="77857-131">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="77857-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="77857-132">Zwraca tablicę obiektów **RedisCacheAttributes** .</span><span class="sxs-lookup"><span data-stu-id="77857-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="77857-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77857-133">NOTES</span></span>

## <span data-ttu-id="77857-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77857-134">RELATED LINKS</span></span>

[<span data-ttu-id="77857-135">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="77857-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="77857-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="77857-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="77857-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="77857-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


