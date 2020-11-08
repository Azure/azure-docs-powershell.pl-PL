---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053012"
---
# <span data-ttu-id="514f0-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="514f0-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="514f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="514f0-102">SYNOPSIS</span></span>
<span data-ttu-id="514f0-103">Usuwa zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="514f0-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="514f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="514f0-104">SYNTAX</span></span>

### <span data-ttu-id="514f0-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="514f0-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514f0-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="514f0-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514f0-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="514f0-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="514f0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="514f0-108">DESCRIPTION</span></span>
<span data-ttu-id="514f0-109">Polecenie cmdlet **Remove-AzFirewallPolicy** usuwa zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="514f0-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="514f0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="514f0-110">EXAMPLES</span></span>

### <span data-ttu-id="514f0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="514f0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="514f0-112">W tym przykładzie usunięto zasady zapory o nazwie "firewallpolicy" w przystawce Resources "TestRg".</span><span class="sxs-lookup"><span data-stu-id="514f0-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="514f0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="514f0-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="514f0-114">W tym przykładzie zasada zapory jest usuwana według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="514f0-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="514f0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="514f0-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="514f0-116">W tym przykładzie $fp zasad zapory jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="514f0-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="514f0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="514f0-117">PARAMETERS</span></span>

### <span data-ttu-id="514f0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="514f0-118">-AsJob</span></span>
<span data-ttu-id="514f0-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="514f0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="514f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514f0-120">-DefaultProfile</span></span>
<span data-ttu-id="514f0-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="514f0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="514f0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="514f0-122">-Force</span></span>
<span data-ttu-id="514f0-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="514f0-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="514f0-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="514f0-124">-InputObject</span></span>
<span data-ttu-id="514f0-125">Zasady AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="514f0-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="514f0-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="514f0-126">-Name</span></span>
<span data-ttu-id="514f0-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="514f0-127">The resource name.</span></span>

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

### <span data-ttu-id="514f0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="514f0-128">-PassThru</span></span>
<span data-ttu-id="514f0-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="514f0-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="514f0-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="514f0-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="514f0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="514f0-131">-ResourceGroupName</span></span>
<span data-ttu-id="514f0-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="514f0-132">The resource group name.</span></span>

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

### <span data-ttu-id="514f0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="514f0-133">-ResourceId</span></span>
<span data-ttu-id="514f0-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="514f0-134">The resource Id.</span></span>

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

### <span data-ttu-id="514f0-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="514f0-135">-Confirm</span></span>
<span data-ttu-id="514f0-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="514f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="514f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="514f0-137">-WhatIf</span></span>
<span data-ttu-id="514f0-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="514f0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="514f0-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="514f0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="514f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514f0-140">CommonParameters</span></span>
<span data-ttu-id="514f0-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514f0-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="514f0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514f0-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="514f0-143">INPUTS</span></span>

### <span data-ttu-id="514f0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="514f0-144">System.String</span></span>

### <span data-ttu-id="514f0-145">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="514f0-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="514f0-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="514f0-146">OUTPUTS</span></span>

### <span data-ttu-id="514f0-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="514f0-147">System.Boolean</span></span>

## <span data-ttu-id="514f0-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="514f0-148">NOTES</span></span>

## <span data-ttu-id="514f0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="514f0-149">RELATED LINKS</span></span>
