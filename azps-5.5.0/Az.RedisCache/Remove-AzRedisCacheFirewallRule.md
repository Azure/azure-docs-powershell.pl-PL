---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201979"
---
# <span data-ttu-id="16907-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16907-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="16907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16907-102">SYNOPSIS</span></span>
<span data-ttu-id="16907-103">Usuwanie reguły zapory z pamięci podręcznej programu Redis.</span><span class="sxs-lookup"><span data-stu-id="16907-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="16907-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16907-104">SYNTAX</span></span>

### <span data-ttu-id="16907-105">NormalParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="16907-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16907-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="16907-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16907-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="16907-107">DESCRIPTION</span></span>
<span data-ttu-id="16907-108">Usuwanie reguły zapory z pamięci podręcznej programu Redis.</span><span class="sxs-lookup"><span data-stu-id="16907-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="16907-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16907-109">EXAMPLES</span></span>

### <span data-ttu-id="16907-110">Przykład 1. Usuwanie reguły pojedynczej zapory</span><span class="sxs-lookup"><span data-stu-id="16907-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="16907-111">To polecenie usuwa regułę zapory o nazwie ruleone z pamięci podręcznej Redis Cache o nazwie mycache.</span><span class="sxs-lookup"><span data-stu-id="16907-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="16907-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16907-112">PARAMETERS</span></span>

### <span data-ttu-id="16907-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16907-113">-DefaultProfile</span></span>
<span data-ttu-id="16907-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16907-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16907-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16907-115">-InputObject</span></span>
<span data-ttu-id="16907-116">obiekt typu PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16907-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="16907-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="16907-117">-Name</span></span>
<span data-ttu-id="16907-118">Nazwa pamięci podręcznej redis.</span><span class="sxs-lookup"><span data-stu-id="16907-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="16907-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16907-119">-PassThru</span></span>
<span data-ttu-id="16907-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="16907-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="16907-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16907-121">-ResourceGroupName</span></span>
<span data-ttu-id="16907-122">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="16907-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="16907-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="16907-123">-RuleName</span></span>
<span data-ttu-id="16907-124">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="16907-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="16907-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16907-125">-Confirm</span></span>
<span data-ttu-id="16907-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16907-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16907-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16907-127">-WhatIf</span></span>
<span data-ttu-id="16907-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16907-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16907-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16907-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16907-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16907-130">CommonParameters</span></span>
<span data-ttu-id="16907-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16907-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16907-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16907-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16907-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16907-133">INPUTS</span></span>

### <span data-ttu-id="16907-134">System.String</span><span class="sxs-lookup"><span data-stu-id="16907-134">System.String</span></span>

### <span data-ttu-id="16907-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16907-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="16907-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16907-136">OUTPUTS</span></span>

### <span data-ttu-id="16907-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16907-137">System.Boolean</span></span>

## <span data-ttu-id="16907-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16907-138">NOTES</span></span>

## <span data-ttu-id="16907-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16907-139">RELATED LINKS</span></span>

[<span data-ttu-id="16907-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16907-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="16907-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16907-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="16907-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16907-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="16907-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16907-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="16907-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16907-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="16907-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16907-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)