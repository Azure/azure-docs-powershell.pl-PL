---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 7f2e9a3bb54aab9def9eba7bdc2a84680fe121c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524969"
---
# <span data-ttu-id="6ea18-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ea18-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6ea18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ea18-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea18-103">Usuwanie reguły zapory z pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6ea18-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ea18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ea18-104">SYNTAX</span></span>

### <span data-ttu-id="6ea18-105">NormalParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ea18-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea18-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="6ea18-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea18-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6ea18-107">DESCRIPTION</span></span>
<span data-ttu-id="6ea18-108">Usuwanie reguły zapory z pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6ea18-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="6ea18-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ea18-109">EXAMPLES</span></span>

### <span data-ttu-id="6ea18-110">Przykład 1. Usuń pojedynczą regułę zapory</span><span class="sxs-lookup"><span data-stu-id="6ea18-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="6ea18-111">To polecenie usuwa regułę zapory o nazwie ruleone z pamięci podręcznej Redis o nazwie moja pamięć.</span><span class="sxs-lookup"><span data-stu-id="6ea18-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="6ea18-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ea18-112">PARAMETERS</span></span>

### <span data-ttu-id="6ea18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea18-113">-DefaultProfile</span></span>
<span data-ttu-id="6ea18-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6ea18-115">-InputObject</span></span>
<span data-ttu-id="6ea18-116">Obiekt typu PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ea18-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ea18-117">-Name</span></span>
<span data-ttu-id="6ea18-118">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="6ea18-118">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ea18-119">-PassThru</span></span>
<span data-ttu-id="6ea18-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6ea18-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea18-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ea18-122">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="6ea18-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6ea18-123">-RuleName</span></span>
<span data-ttu-id="6ea18-124">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6ea18-124">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ea18-125">-Confirm</span></span>
<span data-ttu-id="6ea18-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ea18-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea18-127">-WhatIf</span></span>
<span data-ttu-id="6ea18-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ea18-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea18-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ea18-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea18-130">CommonParameters</span></span>
<span data-ttu-id="6ea18-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea18-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea18-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea18-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ea18-133">INPUTS</span></span>

### <span data-ttu-id="6ea18-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea18-134">System.String</span></span>

## <span data-ttu-id="6ea18-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ea18-135">OUTPUTS</span></span>

### <span data-ttu-id="6ea18-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ea18-136">System.Boolean</span></span>

## <span data-ttu-id="6ea18-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ea18-137">NOTES</span></span>

## <span data-ttu-id="6ea18-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ea18-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ea18-139">Nowe — AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ea18-139">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="6ea18-140">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ea18-140">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="6ea18-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ea18-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6ea18-142">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ea18-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6ea18-143">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ea18-143">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6ea18-144">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ea18-144">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
