---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716438"
---
# <span data-ttu-id="5e178-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="5e178-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="5e178-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e178-102">SYNOPSIS</span></span>
<span data-ttu-id="5e178-103">aktualizowanie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e178-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e178-104">SYNTAX</span></span>

### <span data-ttu-id="5e178-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e178-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e178-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e178-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e178-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e178-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e178-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e178-108">DESCRIPTION</span></span>
<span data-ttu-id="5e178-109">Polecenie cmdlet **Set-AzureRmFrontDoor** aktualizuje istniejące zasady usługi WAF.</span><span class="sxs-lookup"><span data-stu-id="5e178-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="5e178-110">Jeśli parametry wejściowe nie są podane, będą używane stare parametry z istniejących zasad WAF.</span><span class="sxs-lookup"><span data-stu-id="5e178-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="5e178-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e178-111">EXAMPLES</span></span>

### <span data-ttu-id="5e178-112">Przykład 1: aktualizowanie istniejących zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="5e178-113">Aktualizowanie istniejących zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-113">update an existing WAF policy</span></span>

### <span data-ttu-id="5e178-114">Przykład 2: aktualizowanie istniejących zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="5e178-115">Aktualizowanie istniejących zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-115">update an existing WAF policy</span></span>

### <span data-ttu-id="5e178-116">Przykład 3: aktualizowanie istniejących zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="5e178-117">Aktualizowanie istniejących zasad WAF</span><span class="sxs-lookup"><span data-stu-id="5e178-117">update an existing WAF policy</span></span>

### <span data-ttu-id="5e178-118">Przykład 4: aktualizowanie wszystkich zasad WAF w $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e178-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="5e178-119">Aktualizowanie wszystkich zasad WAF w $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e178-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="5e178-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e178-120">PARAMETERS</span></span>

### <span data-ttu-id="5e178-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="5e178-121">-Customrule</span></span>
<span data-ttu-id="5e178-122">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="5e178-122">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e178-123">-DefaultProfile</span></span>
<span data-ttu-id="5e178-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e178-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e178-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5e178-125">-EnabledState</span></span>
<span data-ttu-id="5e178-126">Czy zasady są w stanie włączonym, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="5e178-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="5e178-127">Możliwe wartości obejmują: "wyłączone", "włączone"</span><span class="sxs-lookup"><span data-stu-id="5e178-127">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e178-128">-InputObject</span></span>
<span data-ttu-id="5e178-129">Obiekt FireWallPolicy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="5e178-129">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5e178-130">-ManagedRule</span></span>
<span data-ttu-id="5e178-131">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="5e178-131">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-132">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="5e178-132">-Mode</span></span>
<span data-ttu-id="5e178-133">Opisuje, czy jest w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="5e178-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="5e178-134">Możliwe wartości obejmują: "Zapobieganie", "wykrywanie".</span><span class="sxs-lookup"><span data-stu-id="5e178-134">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e178-135">-Name</span></span>
<span data-ttu-id="5e178-136">Nazwa FireWallPolicy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="5e178-136">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e178-137">-ResourceGroupName</span></span>
<span data-ttu-id="5e178-138">Grupa zasobów, do której należy FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="5e178-138">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e178-139">-ResourceId</span></span>
<span data-ttu-id="5e178-140">Identyfikator zasobu FireWallPolicy do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="5e178-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e178-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e178-141">-Confirm</span></span>
<span data-ttu-id="5e178-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e178-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e178-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e178-143">-WhatIf</span></span>
<span data-ttu-id="5e178-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e178-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e178-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e178-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e178-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e178-146">CommonParameters</span></span>
<span data-ttu-id="5e178-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e178-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e178-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e178-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e178-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e178-149">INPUTS</span></span>

### <span data-ttu-id="5e178-150">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5e178-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="5e178-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5e178-151">System.String</span></span>

## <span data-ttu-id="5e178-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e178-152">OUTPUTS</span></span>

### <span data-ttu-id="5e178-153">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5e178-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="5e178-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e178-154">NOTES</span></span>

## <span data-ttu-id="5e178-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e178-155">RELATED LINKS</span></span>

<span data-ttu-id="5e178-156">[Nowe — AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Nowe — AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [Nowe — AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="5e178-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
