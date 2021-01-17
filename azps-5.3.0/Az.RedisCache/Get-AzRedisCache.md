---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490750"
---
# <span data-ttu-id="e41f0-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e41f0-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="e41f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e41f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e41f0-103">Pobiera pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="e41f0-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="e41f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e41f0-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e41f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e41f0-105">DESCRIPTION</span></span>
<span data-ttu-id="e41f0-106">Polecenie cmdlet **Get-AzRedisCache** pobiera określoną pamięć podręczną usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e41f0-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="e41f0-107">Jeśli nie określisz żadnych parametrów, ta operacja będzie pobierać wszystkie Redis pamięci podręcznej dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e41f0-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="e41f0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e41f0-108">EXAMPLES</span></span>

### <span data-ttu-id="e41f0-109">Przykład 1: uzyskiwanie pamięci podręcznej Redis według nazwy</span><span class="sxs-lookup"><span data-stu-id="e41f0-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

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

<span data-ttu-id="e41f0-110">To polecenie pobiera pamięć podręczną Redis o nazwie Existing.</span><span class="sxs-lookup"><span data-stu-id="e41f0-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="e41f0-111">Przykład 2: pobieranie wszystkich Redis pamięci podręcznej w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e41f0-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="e41f0-112">To polecenie pobiera wszystkie Redis pamięci podręcznej w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e41f0-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="e41f0-113">Przykład 3: Uzyskaj co Redis pamięć podręczną w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e41f0-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

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

<span data-ttu-id="e41f0-114">To polecenie pobiera wszystkie Redis pamięci podręcznej w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e41f0-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="e41f0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e41f0-115">PARAMETERS</span></span>

### <span data-ttu-id="e41f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e41f0-116">-DefaultProfile</span></span>
<span data-ttu-id="e41f0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e41f0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e41f0-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e41f0-118">-Name</span></span>
<span data-ttu-id="e41f0-119">Określa nazwę pamięci podręcznej Redis, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="e41f0-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="e41f0-120">Używany z parametrem *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e41f0-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="e41f0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e41f0-121">-ResourceGroupName</span></span>
<span data-ttu-id="e41f0-122">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="e41f0-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="e41f0-123">Jeśli określisz tylko parametr *ResourceGroupName* , ta operacja pobiera wszystkie Redis pamięci podręcznej w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e41f0-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="e41f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41f0-124">CommonParameters</span></span>
<span data-ttu-id="e41f0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e41f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41f0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e41f0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41f0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e41f0-127">INPUTS</span></span>

### <span data-ttu-id="e41f0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e41f0-128">System.String</span></span>

## <span data-ttu-id="e41f0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e41f0-129">OUTPUTS</span></span>

### <span data-ttu-id="e41f0-130">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="e41f0-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="e41f0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e41f0-131">NOTES</span></span>

## <span data-ttu-id="e41f0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e41f0-132">RELATED LINKS</span></span>

[<span data-ttu-id="e41f0-133">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e41f0-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e41f0-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e41f0-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="e41f0-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e41f0-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


