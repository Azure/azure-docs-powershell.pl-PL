---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222975"
---
# <span data-ttu-id="a6602-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a6602-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="a6602-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6602-102">SYNOPSIS</span></span>
<span data-ttu-id="a6602-103">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="a6602-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="a6602-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6602-104">SYNTAX</span></span>

### <span data-ttu-id="a6602-105">NormalParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a6602-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6602-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="a6602-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6602-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6602-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6602-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a6602-108">DESCRIPTION</span></span>
<span data-ttu-id="a6602-109">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="a6602-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="a6602-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6602-110">EXAMPLES</span></span>

### <span data-ttu-id="a6602-111">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="a6602-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="a6602-112">To polecenie tworzy regułę zapory o nazwie ruleone w pamięci podręcznej Redis o nazwie mój bufor.</span><span class="sxs-lookup"><span data-stu-id="a6602-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="a6602-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6602-113">PARAMETERS</span></span>

### <span data-ttu-id="a6602-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6602-114">-DefaultProfile</span></span>
<span data-ttu-id="a6602-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6602-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6602-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="a6602-116">-EndIP</span></span>
<span data-ttu-id="a6602-117">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="a6602-117">Ending IP address.</span></span>

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

### <span data-ttu-id="a6602-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6602-118">-InputObject</span></span>
<span data-ttu-id="a6602-119">Obiekt typu RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="a6602-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6602-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6602-120">-Name</span></span>
<span data-ttu-id="a6602-121">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="a6602-121">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6602-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6602-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6602-123">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="a6602-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6602-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6602-124">-ResourceId</span></span>
<span data-ttu-id="a6602-125">Identyfikator ARM Redis pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="a6602-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6602-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a6602-126">-RuleName</span></span>
<span data-ttu-id="a6602-127">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a6602-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="a6602-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="a6602-128">-StartIP</span></span>
<span data-ttu-id="a6602-129">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="a6602-129">Starting IP address.</span></span>

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

### <span data-ttu-id="a6602-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6602-130">-Confirm</span></span>
<span data-ttu-id="a6602-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6602-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6602-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6602-132">-WhatIf</span></span>
<span data-ttu-id="a6602-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6602-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6602-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6602-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6602-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6602-135">CommonParameters</span></span>
<span data-ttu-id="a6602-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6602-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6602-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6602-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6602-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6602-138">INPUTS</span></span>

### <span data-ttu-id="a6602-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a6602-139">System.String</span></span>

### <span data-ttu-id="a6602-140">Microsoft. Azure. Commands. RedisCache. models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="a6602-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="a6602-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6602-141">OUTPUTS</span></span>

### <span data-ttu-id="a6602-142">Microsoft. Azure. Commands. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a6602-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="a6602-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6602-143">NOTES</span></span>

## <span data-ttu-id="a6602-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6602-144">RELATED LINKS</span></span>

[<span data-ttu-id="a6602-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a6602-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="a6602-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a6602-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="a6602-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a6602-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="a6602-148">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a6602-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="a6602-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a6602-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a6602-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a6602-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)