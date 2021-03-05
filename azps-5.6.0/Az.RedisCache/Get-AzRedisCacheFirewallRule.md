---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 5e17eced3525a7aa318cbba19b632d3ae11d79a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014929"
---
# <span data-ttu-id="6cb7a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6cb7a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6cb7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb7a-103">Pobierz reguły zapory ustawione w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="6cb7a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6cb7a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb7a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6cb7a-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb7a-106">Jeśli **parametr RuleName** jest podany, polecenie **cmdlet Get-AzRedisCacheFirewallRule** pobiera szczegółowe informacje na temat określonej reguły zapory w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="6cb7a-107">Jeśli zostanie **określona tylko** nazwa, ta operacja uzyskuje dostęp do wszystkich reguł zapory w tej pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="6cb7a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6cb7a-108">EXAMPLES</span></span>

### <span data-ttu-id="6cb7a-109">Przykład 1. Uzyskiwanie reguły pojedynczej zapory</span><span class="sxs-lookup"><span data-stu-id="6cb7a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="6cb7a-110">To polecenie pobiera regułę zapory o nazwie ruleone z pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="6cb7a-111">Przykład 2. Uzyskiwanie wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="6cb7a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="6cb7a-112">To polecenie pobiera wszystkie reguły zapory z pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="6cb7a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cb7a-113">PARAMETERS</span></span>

### <span data-ttu-id="6cb7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb7a-114">-DefaultProfile</span></span>
<span data-ttu-id="6cb7a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cb7a-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6cb7a-116">-Name</span></span>
<span data-ttu-id="6cb7a-117">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="6cb7a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb7a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6cb7a-119">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="6cb7a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6cb7a-120">-RuleName</span></span>
<span data-ttu-id="6cb7a-121">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="6cb7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb7a-122">CommonParameters</span></span>
<span data-ttu-id="6cb7a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb7a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb7a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb7a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cb7a-125">INPUTS</span></span>

### <span data-ttu-id="6cb7a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb7a-126">System.String</span></span>

## <span data-ttu-id="6cb7a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cb7a-127">OUTPUTS</span></span>

### <span data-ttu-id="6cb7a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6cb7a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6cb7a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6cb7a-129">NOTES</span></span>

## <span data-ttu-id="6cb7a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cb7a-130">RELATED LINKS</span></span>

[<span data-ttu-id="6cb7a-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6cb7a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6cb7a-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6cb7a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6cb7a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cb7a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6cb7a-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cb7a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6cb7a-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cb7a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6cb7a-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cb7a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)