---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 91eff9b6a096263b96ecae0cf9901f6dbce26c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550271"
---
# <span data-ttu-id="d8e12-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8e12-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="d8e12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8e12-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e12-103">Pobierz reguły zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d8e12-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8e12-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8e12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8e12-105">DESCRIPTION</span></span>
<span data-ttu-id="d8e12-106">Jeśli parametr **RuleName** jest podany, polecenie cmdlet **Get-AzureRmRedisCacheFirewallRule** pobiera szczegóły dotyczące określonej reguły zapory w pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d8e12-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="d8e12-107">Jeśli określono tylko **nazwę** , ta operacja pobiera wszystkie reguły zapory dostępne w tej pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d8e12-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="d8e12-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8e12-108">EXAMPLES</span></span>

### <span data-ttu-id="d8e12-109">Przykład 1: uzyskiwanie pojedynczej reguły zapory</span><span class="sxs-lookup"><span data-stu-id="d8e12-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="d8e12-110">To polecenie pobiera regułę zapory o nazwie ruleone z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="d8e12-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="d8e12-111">Przykład 2: pobieranie wszystkich reguł zapory</span><span class="sxs-lookup"><span data-stu-id="d8e12-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="d8e12-112">To polecenie pobiera wszystkie reguły zapory z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="d8e12-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="d8e12-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8e12-113">PARAMETERS</span></span>

### <span data-ttu-id="d8e12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e12-114">-DefaultProfile</span></span>
<span data-ttu-id="d8e12-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e12-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8e12-116">-Name</span></span>
<span data-ttu-id="d8e12-117">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="d8e12-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="d8e12-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e12-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8e12-119">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="d8e12-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="d8e12-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d8e12-120">-RuleName</span></span>
<span data-ttu-id="d8e12-121">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="d8e12-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="d8e12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e12-122">CommonParameters</span></span>
<span data-ttu-id="d8e12-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e12-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e12-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e12-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8e12-125">INPUTS</span></span>

### <span data-ttu-id="d8e12-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e12-126">System.String</span></span>

## <span data-ttu-id="d8e12-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8e12-127">OUTPUTS</span></span>

### <span data-ttu-id="d8e12-128">Microsoft. Azure. Commands. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8e12-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="d8e12-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8e12-129">NOTES</span></span>

## <span data-ttu-id="d8e12-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8e12-130">RELATED LINKS</span></span>

[<span data-ttu-id="d8e12-131">Nowe — AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8e12-131">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="d8e12-132">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8e12-132">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="d8e12-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8e12-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d8e12-134">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8e12-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="d8e12-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8e12-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d8e12-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d8e12-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
