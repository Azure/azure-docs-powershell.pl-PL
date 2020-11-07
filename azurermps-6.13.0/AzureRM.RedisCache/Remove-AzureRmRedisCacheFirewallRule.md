---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 25c3d0c72539ecd74e25ed455b4afcf4211c0718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717908"
---
# <span data-ttu-id="e7deb-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7deb-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="e7deb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7deb-102">SYNOPSIS</span></span>
<span data-ttu-id="e7deb-103">Usuwanie reguły zapory z pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="e7deb-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7deb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7deb-104">SYNTAX</span></span>

### <span data-ttu-id="e7deb-105">NormalParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7deb-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7deb-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="e7deb-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7deb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7deb-107">DESCRIPTION</span></span>
<span data-ttu-id="e7deb-108">Usuwanie reguły zapory z pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="e7deb-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="e7deb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7deb-109">EXAMPLES</span></span>

### <span data-ttu-id="e7deb-110">Przykład 1. Usuń pojedynczą regułę zapory</span><span class="sxs-lookup"><span data-stu-id="e7deb-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="e7deb-111">To polecenie usuwa regułę zapory o nazwie ruleone z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="e7deb-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="e7deb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7deb-112">PARAMETERS</span></span>

### <span data-ttu-id="e7deb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7deb-113">-DefaultProfile</span></span>
<span data-ttu-id="e7deb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7deb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7deb-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e7deb-115">-InputObject</span></span>
<span data-ttu-id="e7deb-116">Obiekt typu PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7deb-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="e7deb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7deb-117">-Name</span></span>
<span data-ttu-id="e7deb-118">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="e7deb-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="e7deb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7deb-119">-PassThru</span></span>
<span data-ttu-id="e7deb-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e7deb-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e7deb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7deb-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7deb-122">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="e7deb-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="e7deb-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e7deb-123">-RuleName</span></span>
<span data-ttu-id="e7deb-124">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="e7deb-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="e7deb-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7deb-125">-Confirm</span></span>
<span data-ttu-id="e7deb-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7deb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7deb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7deb-127">-WhatIf</span></span>
<span data-ttu-id="e7deb-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7deb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7deb-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7deb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7deb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7deb-130">CommonParameters</span></span>
<span data-ttu-id="e7deb-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7deb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7deb-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7deb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7deb-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7deb-133">INPUTS</span></span>

### <span data-ttu-id="e7deb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e7deb-134">System.String</span></span>

### <span data-ttu-id="e7deb-135">Microsoft. Azure. Commands. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7deb-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>
<span data-ttu-id="e7deb-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7deb-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e7deb-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7deb-137">OUTPUTS</span></span>

### <span data-ttu-id="e7deb-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7deb-138">System.Boolean</span></span>

## <span data-ttu-id="e7deb-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7deb-139">NOTES</span></span>

## <span data-ttu-id="e7deb-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7deb-140">RELATED LINKS</span></span>

[<span data-ttu-id="e7deb-141">Nowe — AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7deb-141">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e7deb-142">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7deb-142">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e7deb-143">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e7deb-143">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="e7deb-144">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e7deb-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e7deb-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e7deb-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e7deb-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e7deb-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
