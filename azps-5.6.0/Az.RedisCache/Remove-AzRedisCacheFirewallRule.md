---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 9c68e89d09d386d6071cb639fa77ba740a6da53f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972666"
---
# <span data-ttu-id="bc259-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bc259-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="bc259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc259-102">SYNOPSIS</span></span>
<span data-ttu-id="bc259-103">Usuwanie reguły zapory z pamięci podręcznej programu Redis.</span><span class="sxs-lookup"><span data-stu-id="bc259-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="bc259-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc259-104">SYNTAX</span></span>

### <span data-ttu-id="bc259-105">NormalParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bc259-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc259-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="bc259-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc259-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc259-107">DESCRIPTION</span></span>
<span data-ttu-id="bc259-108">Usuwanie reguły zapory z pamięci podręcznej programu Redis.</span><span class="sxs-lookup"><span data-stu-id="bc259-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="bc259-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc259-109">EXAMPLES</span></span>

### <span data-ttu-id="bc259-110">Przykład 1. Usuwanie reguły pojedynczej zapory</span><span class="sxs-lookup"><span data-stu-id="bc259-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="bc259-111">To polecenie usuwa regułę zapory o nazwie ruleone z pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="bc259-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="bc259-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc259-112">PARAMETERS</span></span>

### <span data-ttu-id="bc259-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc259-113">-DefaultProfile</span></span>
<span data-ttu-id="bc259-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc259-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc259-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc259-115">-InputObject</span></span>
<span data-ttu-id="bc259-116">obiekt typu PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bc259-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc259-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc259-117">-Name</span></span>
<span data-ttu-id="bc259-118">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="bc259-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="bc259-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc259-119">-PassThru</span></span>
<span data-ttu-id="bc259-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bc259-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc259-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc259-121">-ResourceGroupName</span></span>
<span data-ttu-id="bc259-122">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="bc259-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="bc259-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="bc259-123">-RuleName</span></span>
<span data-ttu-id="bc259-124">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="bc259-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="bc259-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc259-125">-Confirm</span></span>
<span data-ttu-id="bc259-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc259-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc259-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc259-127">-WhatIf</span></span>
<span data-ttu-id="bc259-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc259-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc259-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bc259-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc259-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc259-130">CommonParameters</span></span>
<span data-ttu-id="bc259-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc259-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc259-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc259-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc259-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc259-133">INPUTS</span></span>

### <span data-ttu-id="bc259-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bc259-134">System.String</span></span>

### <span data-ttu-id="bc259-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bc259-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="bc259-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc259-136">OUTPUTS</span></span>

### <span data-ttu-id="bc259-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc259-137">System.Boolean</span></span>

## <span data-ttu-id="bc259-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc259-138">NOTES</span></span>

## <span data-ttu-id="bc259-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc259-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc259-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bc259-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="bc259-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bc259-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="bc259-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bc259-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="bc259-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bc259-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="bc259-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bc259-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="bc259-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bc259-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)