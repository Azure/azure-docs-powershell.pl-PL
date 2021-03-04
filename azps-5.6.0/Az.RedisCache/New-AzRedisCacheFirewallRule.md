---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: bd0d6995cae0d32a7fb0ce46d42f87a480c275f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956673"
---
# <span data-ttu-id="dacdd-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dacdd-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="dacdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dacdd-102">SYNOPSIS</span></span>
<span data-ttu-id="dacdd-103">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="dacdd-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="dacdd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dacdd-104">SYNTAX</span></span>

### <span data-ttu-id="dacdd-105">NormalParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dacdd-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacdd-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="dacdd-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacdd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dacdd-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacdd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dacdd-108">DESCRIPTION</span></span>
<span data-ttu-id="dacdd-109">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="dacdd-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="dacdd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dacdd-110">EXAMPLES</span></span>

### <span data-ttu-id="dacdd-111">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="dacdd-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="dacdd-112">To polecenie tworzy regułę zapory o nazwie ruleone w pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="dacdd-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="dacdd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dacdd-113">PARAMETERS</span></span>

### <span data-ttu-id="dacdd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacdd-114">-DefaultProfile</span></span>
<span data-ttu-id="dacdd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dacdd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dacdd-116">— EndIP</span><span class="sxs-lookup"><span data-stu-id="dacdd-116">-EndIP</span></span>
<span data-ttu-id="dacdd-117">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="dacdd-117">Ending IP address.</span></span>

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

### <span data-ttu-id="dacdd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dacdd-118">-InputObject</span></span>
<span data-ttu-id="dacdd-119">obiekt typu RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="dacdd-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="dacdd-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dacdd-120">-Name</span></span>
<span data-ttu-id="dacdd-121">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="dacdd-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="dacdd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacdd-122">-ResourceGroupName</span></span>
<span data-ttu-id="dacdd-123">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="dacdd-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="dacdd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dacdd-124">-ResourceId</span></span>
<span data-ttu-id="dacdd-125">ARM identyfikator pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="dacdd-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="dacdd-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="dacdd-126">-RuleName</span></span>
<span data-ttu-id="dacdd-127">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="dacdd-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="dacdd-128">— StartIP</span><span class="sxs-lookup"><span data-stu-id="dacdd-128">-StartIP</span></span>
<span data-ttu-id="dacdd-129">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="dacdd-129">Starting IP address.</span></span>

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

### <span data-ttu-id="dacdd-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dacdd-130">-Confirm</span></span>
<span data-ttu-id="dacdd-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dacdd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacdd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacdd-132">-WhatIf</span></span>
<span data-ttu-id="dacdd-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dacdd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dacdd-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dacdd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacdd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacdd-135">CommonParameters</span></span>
<span data-ttu-id="dacdd-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dacdd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacdd-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dacdd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacdd-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dacdd-138">INPUTS</span></span>

### <span data-ttu-id="dacdd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dacdd-139">System.String</span></span>

### <span data-ttu-id="dacdd-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="dacdd-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="dacdd-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dacdd-141">OUTPUTS</span></span>

### <span data-ttu-id="dacdd-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dacdd-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="dacdd-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dacdd-143">NOTES</span></span>

## <span data-ttu-id="dacdd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dacdd-144">RELATED LINKS</span></span>

[<span data-ttu-id="dacdd-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dacdd-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="dacdd-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dacdd-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="dacdd-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dacdd-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dacdd-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dacdd-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="dacdd-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dacdd-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="dacdd-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dacdd-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)