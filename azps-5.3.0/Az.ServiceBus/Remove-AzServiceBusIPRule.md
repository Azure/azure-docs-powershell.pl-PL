---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502892"
---
# <span data-ttu-id="f8f4c-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="f8f4c-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="f8f4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f4c-103">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f8f4c-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f8f4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8f4c-104">SYNTAX</span></span>

### <span data-ttu-id="f8f4c-105">IPRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8f4c-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8f4c-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8f4c-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8f4c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="f8f4c-108">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f8f4c-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f8f4c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8f4c-109">EXAMPLES</span></span>

### <span data-ttu-id="f8f4c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f8f4c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="f8f4c-111">Usuwa IpMask NetworkRuleSet z danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f8f4c-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="f8f4c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8f4c-112">PARAMETERS</span></span>

### <span data-ttu-id="f8f4c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8f4c-113">-AsJob</span></span>
<span data-ttu-id="f8f4c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8f4c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8f4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f4c-115">-DefaultProfile</span></span>
<span data-ttu-id="f8f4c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8f4c-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="f8f4c-117">-IpMask</span></span>
<span data-ttu-id="f8f4c-118">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="f8f4c-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f4c-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f8f4c-119">-IpRuleObject</span></span>
<span data-ttu-id="f8f4c-120">Obiekt konfiguracji IPRule</span><span class="sxs-lookup"><span data-stu-id="f8f4c-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f4c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8f4c-121">-Name</span></span>
<span data-ttu-id="f8f4c-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f8f4c-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f4c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8f4c-123">-PassThru</span></span>
<span data-ttu-id="f8f4c-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f8f4c-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f8f4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8f4c-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f8f4c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f4c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8f4c-127">-Confirm</span></span>
<span data-ttu-id="f8f4c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8f4c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8f4c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8f4c-129">-WhatIf</span></span>
<span data-ttu-id="f8f4c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8f4c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8f4c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8f4c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8f4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f4c-132">CommonParameters</span></span>
<span data-ttu-id="f8f4c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f8f4c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f4c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f4c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8f4c-135">INPUTS</span></span>

### <span data-ttu-id="f8f4c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f8f4c-136">System.String</span></span>

### <span data-ttu-id="f8f4c-137">Microsoft. Azure. Commands. ServiceBus. models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f8f4c-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="f8f4c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8f4c-138">OUTPUTS</span></span>

### <span data-ttu-id="f8f4c-139">Microsoft. Azure. Commands. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f8f4c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f8f4c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8f4c-140">NOTES</span></span>

## <span data-ttu-id="f8f4c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8f4c-141">RELATED LINKS</span></span>
