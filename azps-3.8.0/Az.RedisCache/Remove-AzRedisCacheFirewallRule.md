---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896082"
---
# <span data-ttu-id="7ac6c-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ac6c-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="7ac6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ac6c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac6c-103">Usuwanie reguły zapory z pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="7ac6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ac6c-104">SYNTAX</span></span>

### <span data-ttu-id="7ac6c-105">NormalParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ac6c-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac6c-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="7ac6c-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac6c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7ac6c-107">DESCRIPTION</span></span>
<span data-ttu-id="7ac6c-108">Usuwanie reguły zapory z pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="7ac6c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ac6c-109">EXAMPLES</span></span>

### <span data-ttu-id="7ac6c-110">Przykład 1. Usuń pojedynczą regułę zapory</span><span class="sxs-lookup"><span data-stu-id="7ac6c-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="7ac6c-111">To polecenie usuwa regułę zapory o nazwie ruleone z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="7ac6c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ac6c-112">PARAMETERS</span></span>

### <span data-ttu-id="7ac6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac6c-113">-DefaultProfile</span></span>
<span data-ttu-id="7ac6c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac6c-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ac6c-115">-InputObject</span></span>
<span data-ttu-id="7ac6c-116">Obiekt typu PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ac6c-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="7ac6c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ac6c-117">-Name</span></span>
<span data-ttu-id="7ac6c-118">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="7ac6c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ac6c-119">-PassThru</span></span>
<span data-ttu-id="7ac6c-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7ac6c-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7ac6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ac6c-122">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="7ac6c-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7ac6c-123">-RuleName</span></span>
<span data-ttu-id="7ac6c-124">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="7ac6c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ac6c-125">-Confirm</span></span>
<span data-ttu-id="7ac6c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac6c-127">-WhatIf</span></span>
<span data-ttu-id="7ac6c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac6c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac6c-130">CommonParameters</span></span>
<span data-ttu-id="7ac6c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac6c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac6c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac6c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac6c-133">INPUTS</span></span>

### <span data-ttu-id="7ac6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7ac6c-134">System.String</span></span>

### <span data-ttu-id="7ac6c-135">Microsoft. Azure. Commands. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ac6c-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="7ac6c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ac6c-136">OUTPUTS</span></span>

### <span data-ttu-id="7ac6c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ac6c-137">System.Boolean</span></span>

## <span data-ttu-id="7ac6c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ac6c-138">NOTES</span></span>

## <span data-ttu-id="7ac6c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac6c-139">RELATED LINKS</span></span>

[<span data-ttu-id="7ac6c-140">Nowe — AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ac6c-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7ac6c-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ac6c-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7ac6c-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ac6c-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7ac6c-143">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ac6c-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7ac6c-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ac6c-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="7ac6c-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ac6c-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)