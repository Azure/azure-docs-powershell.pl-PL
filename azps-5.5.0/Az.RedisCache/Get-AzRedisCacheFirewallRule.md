---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191242"
---
# <span data-ttu-id="234bd-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="234bd-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="234bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="234bd-102">SYNOPSIS</span></span>
<span data-ttu-id="234bd-103">Pobierz reguły zapory ustawione w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="234bd-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="234bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="234bd-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="234bd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="234bd-105">DESCRIPTION</span></span>
<span data-ttu-id="234bd-106">Jeśli **parametr RuleName** jest podany, polecenie **cmdlet Get-AzRedisCacheFirewallRule** pobiera szczegółowe informacje na temat określonej reguły zapory w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="234bd-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="234bd-107">Jeśli zostanie **określona tylko** nazwa, ta operacja uzyskuje dostęp do wszystkich reguł zapory w tej pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="234bd-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="234bd-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="234bd-108">EXAMPLES</span></span>

### <span data-ttu-id="234bd-109">Przykład 1. Uzyskiwanie reguły pojedynczej zapory</span><span class="sxs-lookup"><span data-stu-id="234bd-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="234bd-110">To polecenie pobiera regułę zapory o nazwie ruleone z pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="234bd-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="234bd-111">Przykład 2. Uzyskiwanie wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="234bd-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="234bd-112">To polecenie pobiera wszystkie reguły zapory z pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="234bd-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="234bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="234bd-113">PARAMETERS</span></span>

### <span data-ttu-id="234bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234bd-114">-DefaultProfile</span></span>
<span data-ttu-id="234bd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="234bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="234bd-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="234bd-116">-Name</span></span>
<span data-ttu-id="234bd-117">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="234bd-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="234bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="234bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="234bd-119">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="234bd-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="234bd-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="234bd-120">-RuleName</span></span>
<span data-ttu-id="234bd-121">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="234bd-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="234bd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234bd-122">CommonParameters</span></span>
<span data-ttu-id="234bd-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="234bd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234bd-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="234bd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234bd-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="234bd-125">INPUTS</span></span>

### <span data-ttu-id="234bd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="234bd-126">System.String</span></span>

## <span data-ttu-id="234bd-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="234bd-127">OUTPUTS</span></span>

### <span data-ttu-id="234bd-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="234bd-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="234bd-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="234bd-129">NOTES</span></span>

## <span data-ttu-id="234bd-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="234bd-130">RELATED LINKS</span></span>

[<span data-ttu-id="234bd-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="234bd-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="234bd-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="234bd-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="234bd-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="234bd-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="234bd-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="234bd-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="234bd-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="234bd-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="234bd-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="234bd-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)