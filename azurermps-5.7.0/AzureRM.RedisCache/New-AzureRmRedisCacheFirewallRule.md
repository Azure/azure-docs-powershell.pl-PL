---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716986"
---
# <span data-ttu-id="5817c-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5817c-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="5817c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5817c-102">SYNOPSIS</span></span>
<span data-ttu-id="5817c-103">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="5817c-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5817c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5817c-104">SYNTAX</span></span>

### <span data-ttu-id="5817c-105">NormalParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5817c-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5817c-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="5817c-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5817c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5817c-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5817c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5817c-108">DESCRIPTION</span></span>
<span data-ttu-id="5817c-109">Utwórz regułę zapory w pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="5817c-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="5817c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5817c-110">EXAMPLES</span></span>

### <span data-ttu-id="5817c-111">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="5817c-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="5817c-112">To polecenie tworzy regułę zapory o nazwie ruleone w pamięci podręcznej Redis o nazwie mój bufor.</span><span class="sxs-lookup"><span data-stu-id="5817c-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="5817c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5817c-113">PARAMETERS</span></span>

### <span data-ttu-id="5817c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5817c-114">-DefaultProfile</span></span>
<span data-ttu-id="5817c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5817c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5817c-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="5817c-116">-EndIP</span></span>
<span data-ttu-id="5817c-117">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="5817c-117">Ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5817c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5817c-118">-InputObject</span></span>
<span data-ttu-id="5817c-119">Obiekt typu RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="5817c-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5817c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5817c-120">-Name</span></span>
<span data-ttu-id="5817c-121">Nazwa pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="5817c-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="5817c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5817c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5817c-123">Nazwa grupy zasobów, w której istnieje pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="5817c-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="5817c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5817c-124">-ResourceId</span></span>
<span data-ttu-id="5817c-125">Identyfikator ARM Redis pamięć podręczna.</span><span class="sxs-lookup"><span data-stu-id="5817c-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5817c-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5817c-126">-RuleName</span></span>
<span data-ttu-id="5817c-127">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="5817c-127">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5817c-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="5817c-128">-StartIP</span></span>
<span data-ttu-id="5817c-129">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="5817c-129">Starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5817c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5817c-130">-Confirm</span></span>
<span data-ttu-id="5817c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5817c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5817c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5817c-132">-WhatIf</span></span>
<span data-ttu-id="5817c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5817c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5817c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5817c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5817c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5817c-135">CommonParameters</span></span>
<span data-ttu-id="5817c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5817c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5817c-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5817c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5817c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5817c-138">INPUTS</span></span>

### <span data-ttu-id="5817c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5817c-139">System.String</span></span>

## <span data-ttu-id="5817c-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5817c-140">OUTPUTS</span></span>

### <span data-ttu-id="5817c-141">Microsoft. Azure. Commands. RedisCache. models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5817c-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="5817c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5817c-142">NOTES</span></span>

## <span data-ttu-id="5817c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5817c-143">RELATED LINKS</span></span>

[<span data-ttu-id="5817c-144">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5817c-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="5817c-145">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5817c-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="5817c-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5817c-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="5817c-147">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5817c-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="5817c-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5817c-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="5817c-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5817c-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
