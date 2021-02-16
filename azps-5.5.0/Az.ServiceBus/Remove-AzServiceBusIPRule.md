---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201635"
---
# <span data-ttu-id="49009-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="49009-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="49009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49009-102">SYNOPSIS</span></span>
<span data-ttu-id="49009-103">Usuwanie jednej reguły IP do zestawu NetworkRuleSet danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="49009-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="49009-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49009-104">SYNTAX</span></span>

### <span data-ttu-id="49009-105">IPRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="49009-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49009-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49009-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49009-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="49009-107">DESCRIPTION</span></span>
<span data-ttu-id="49009-108">Usuwanie jednej reguły IP do zestawu NetworkRuleSet danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="49009-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="49009-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49009-109">EXAMPLES</span></span>

### <span data-ttu-id="49009-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49009-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="49009-111">Usuwamas ip (IpMask) zestawu NetworkRuleSet danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="49009-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="49009-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49009-112">PARAMETERS</span></span>

### <span data-ttu-id="49009-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="49009-113">-AsJob</span></span>
<span data-ttu-id="49009-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49009-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49009-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49009-115">-DefaultProfile</span></span>
<span data-ttu-id="49009-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49009-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49009-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="49009-117">-IpMask</span></span>
<span data-ttu-id="49009-118">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="49009-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="49009-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="49009-119">-IpRuleObject</span></span>
<span data-ttu-id="49009-120">Obiekt konfiguracji protokołu IPRule</span><span class="sxs-lookup"><span data-stu-id="49009-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="49009-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49009-121">-Name</span></span>
<span data-ttu-id="49009-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="49009-122">Namespace Name</span></span>

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

### <span data-ttu-id="49009-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49009-123">-PassThru</span></span>
<span data-ttu-id="49009-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="49009-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="49009-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49009-125">-ResourceGroupName</span></span>
<span data-ttu-id="49009-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="49009-126">Resource Group Name</span></span>

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

### <span data-ttu-id="49009-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49009-127">-Confirm</span></span>
<span data-ttu-id="49009-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49009-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49009-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49009-129">-WhatIf</span></span>
<span data-ttu-id="49009-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49009-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49009-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49009-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49009-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49009-132">CommonParameters</span></span>
<span data-ttu-id="49009-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49009-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49009-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49009-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49009-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49009-135">INPUTS</span></span>

### <span data-ttu-id="49009-136">System.String</span><span class="sxs-lookup"><span data-stu-id="49009-136">System.String</span></span>

### <span data-ttu-id="49009-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="49009-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="49009-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49009-138">OUTPUTS</span></span>

### <span data-ttu-id="49009-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="49009-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="49009-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49009-140">NOTES</span></span>

## <span data-ttu-id="49009-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49009-141">RELATED LINKS</span></span>
