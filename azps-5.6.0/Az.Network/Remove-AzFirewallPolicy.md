---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: 69d9e49c83b2f1231be4fe2b1ffc3cba25c2cf2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993770"
---
# <span data-ttu-id="c0478-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c0478-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="c0478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0478-102">SYNOPSIS</span></span>
<span data-ttu-id="c0478-103">Usuwa zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c0478-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="c0478-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0478-104">SYNTAX</span></span>

### <span data-ttu-id="c0478-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0478-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0478-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0478-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0478-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0478-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0478-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0478-108">DESCRIPTION</span></span>
<span data-ttu-id="c0478-109">Polecenie **cmdlet Remove-AzFirewallPolicy** usuwa zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0478-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="c0478-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0478-110">EXAMPLES</span></span>

### <span data-ttu-id="c0478-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0478-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="c0478-112">W tym przykładzie zasady zapory o nazwie "firewallpolicy" w grupie zasobów "TestRg"</span><span class="sxs-lookup"><span data-stu-id="c0478-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="c0478-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c0478-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="c0478-114">W tym przykładzie zasady zapory są usuwane za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="c0478-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="c0478-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c0478-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="c0478-116">W tym przykładzie zasady zapory są $fp</span><span class="sxs-lookup"><span data-stu-id="c0478-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="c0478-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0478-117">PARAMETERS</span></span>

### <span data-ttu-id="c0478-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c0478-118">-AsJob</span></span>
<span data-ttu-id="c0478-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c0478-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0478-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0478-120">-DefaultProfile</span></span>
<span data-ttu-id="c0478-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0478-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0478-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c0478-122">-Force</span></span>
<span data-ttu-id="c0478-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0478-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c0478-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0478-124">-InputObject</span></span>
<span data-ttu-id="c0478-125">Zasady AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c0478-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0478-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0478-126">-Name</span></span>
<span data-ttu-id="c0478-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c0478-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0478-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0478-128">-PassThru</span></span>
<span data-ttu-id="c0478-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c0478-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0478-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c0478-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0478-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0478-131">-ResourceGroupName</span></span>
<span data-ttu-id="c0478-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0478-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0478-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0478-133">-ResourceId</span></span>
<span data-ttu-id="c0478-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c0478-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0478-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0478-135">-Confirm</span></span>
<span data-ttu-id="c0478-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0478-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0478-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0478-137">-WhatIf</span></span>
<span data-ttu-id="c0478-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0478-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0478-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0478-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0478-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0478-140">CommonParameters</span></span>
<span data-ttu-id="c0478-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0478-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0478-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0478-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0478-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0478-143">INPUTS</span></span>

### <span data-ttu-id="c0478-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c0478-144">System.String</span></span>

### <span data-ttu-id="c0478-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c0478-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="c0478-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0478-146">OUTPUTS</span></span>

### <span data-ttu-id="c0478-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0478-147">System.Boolean</span></span>

## <span data-ttu-id="c0478-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0478-148">NOTES</span></span>

## <span data-ttu-id="c0478-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0478-149">RELATED LINKS</span></span>
