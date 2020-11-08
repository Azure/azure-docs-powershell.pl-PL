---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233628"
---
# <span data-ttu-id="6d706-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d706-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6d706-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d706-102">SYNOPSIS</span></span>
<span data-ttu-id="6d706-103">Pobierz reguły zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6d706-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="6d706-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d706-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d706-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d706-105">DESCRIPTION</span></span>
<span data-ttu-id="6d706-106">Jeśli parametr **RuleName** jest podany, polecenie cmdlet **Get-AzRedisCacheFirewallRule** pobiera szczegóły dotyczące określonej reguły zapory w pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="6d706-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="6d706-107">Jeśli określono tylko **nazwę** , ta operacja pobiera wszystkie reguły zapory dostępne w tej pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6d706-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="6d706-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d706-108">EXAMPLES</span></span>

### <span data-ttu-id="6d706-109">Przykład 1: uzyskiwanie pojedynczej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="6d706-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="6d706-110">To polecenie pobiera regułę zapory o nazwie ruleone z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="6d706-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="6d706-111">Przykład 2: pobieranie wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="6d706-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="6d706-112">To polecenie pobiera wszystkie reguły zapory z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="6d706-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="6d706-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d706-113">PARAMETERS</span></span>

### <span data-ttu-id="6d706-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d706-114">-DefaultProfile</span></span>
<span data-ttu-id="6d706-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d706-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d706-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d706-116">-Name</span></span>
<span data-ttu-id="6d706-117">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6d706-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="6d706-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d706-118">-ResourceGroupName</span></span>
<span data-ttu-id="6d706-119">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="6d706-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="6d706-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6d706-120">-RuleName</span></span>
<span data-ttu-id="6d706-121">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6d706-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="6d706-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d706-122">CommonParameters</span></span>
<span data-ttu-id="6d706-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d706-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d706-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d706-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d706-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d706-125">INPUTS</span></span>

### <span data-ttu-id="6d706-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6d706-126">System.String</span></span>

## <span data-ttu-id="6d706-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d706-127">OUTPUTS</span></span>

### <span data-ttu-id="6d706-128">Microsoft. Azure. Commands. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d706-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6d706-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d706-129">NOTES</span></span>

## <span data-ttu-id="6d706-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d706-130">RELATED LINKS</span></span>

[<span data-ttu-id="6d706-131">Nowe — AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d706-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6d706-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d706-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6d706-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d706-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6d706-134">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d706-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6d706-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d706-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6d706-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6d706-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)