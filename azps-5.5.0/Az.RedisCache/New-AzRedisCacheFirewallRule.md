---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240234"
---
# <span data-ttu-id="2419a-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2419a-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="2419a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2419a-102">SYNOPSIS</span></span>
<span data-ttu-id="2419a-103">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2419a-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="2419a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2419a-104">SYNTAX</span></span>

### <span data-ttu-id="2419a-105">NormalParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2419a-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2419a-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="2419a-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2419a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2419a-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2419a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2419a-108">DESCRIPTION</span></span>
<span data-ttu-id="2419a-109">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2419a-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="2419a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2419a-110">EXAMPLES</span></span>

### <span data-ttu-id="2419a-111">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="2419a-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="2419a-112">To polecenie tworzy regułę zapory o nazwie ruleone w pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="2419a-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="2419a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2419a-113">PARAMETERS</span></span>

### <span data-ttu-id="2419a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2419a-114">-DefaultProfile</span></span>
<span data-ttu-id="2419a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2419a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2419a-116">— EndIP</span><span class="sxs-lookup"><span data-stu-id="2419a-116">-EndIP</span></span>
<span data-ttu-id="2419a-117">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="2419a-117">Ending IP address.</span></span>

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

### <span data-ttu-id="2419a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2419a-118">-InputObject</span></span>
<span data-ttu-id="2419a-119">obiekt typu RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="2419a-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="2419a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2419a-120">-Name</span></span>
<span data-ttu-id="2419a-121">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="2419a-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="2419a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2419a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2419a-123">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="2419a-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="2419a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2419a-124">-ResourceId</span></span>
<span data-ttu-id="2419a-125">ARM identyfikator pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="2419a-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="2419a-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="2419a-126">-RuleName</span></span>
<span data-ttu-id="2419a-127">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="2419a-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="2419a-128">— StartIP</span><span class="sxs-lookup"><span data-stu-id="2419a-128">-StartIP</span></span>
<span data-ttu-id="2419a-129">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="2419a-129">Starting IP address.</span></span>

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

### <span data-ttu-id="2419a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2419a-130">-Confirm</span></span>
<span data-ttu-id="2419a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2419a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2419a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2419a-132">-WhatIf</span></span>
<span data-ttu-id="2419a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2419a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2419a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2419a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2419a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2419a-135">CommonParameters</span></span>
<span data-ttu-id="2419a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2419a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2419a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2419a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2419a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2419a-138">INPUTS</span></span>

### <span data-ttu-id="2419a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2419a-139">System.String</span></span>

### <span data-ttu-id="2419a-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="2419a-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="2419a-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2419a-141">OUTPUTS</span></span>

### <span data-ttu-id="2419a-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2419a-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="2419a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2419a-143">NOTES</span></span>

## <span data-ttu-id="2419a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2419a-144">RELATED LINKS</span></span>

[<span data-ttu-id="2419a-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2419a-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="2419a-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2419a-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="2419a-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2419a-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2419a-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2419a-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2419a-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2419a-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2419a-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2419a-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)