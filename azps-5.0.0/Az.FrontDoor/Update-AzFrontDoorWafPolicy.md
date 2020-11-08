---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224402"
---
# <span data-ttu-id="e14f7-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="e14f7-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="e14f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e14f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e14f7-103">Aktualizowanie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="e14f7-103">Update WAF policy</span></span>

## <span data-ttu-id="e14f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e14f7-104">SYNTAX</span></span>

### <span data-ttu-id="e14f7-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e14f7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14f7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e14f7-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14f7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e14f7-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e14f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e14f7-108">DESCRIPTION</span></span>
<span data-ttu-id="e14f7-109">Polecenie cmdlet **Update-AzFrontDoorWafPolicy** aktualizuje istniejące zasady WAF.</span><span class="sxs-lookup"><span data-stu-id="e14f7-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="e14f7-110">Jeśli parametry wejściowe nie są podane, będą używane stare parametry z istniejących zasad WAF.</span><span class="sxs-lookup"><span data-stu-id="e14f7-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="e14f7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e14f7-111">EXAMPLES</span></span>

### <span data-ttu-id="e14f7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e14f7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="e14f7-113">Aktualizowanie istniejącego niestandardowego kodu stanu zasad WAF.</span><span class="sxs-lookup"><span data-stu-id="e14f7-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="e14f7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e14f7-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="e14f7-115">Aktualizowanie istniejącego trybu zasad WAF.</span><span class="sxs-lookup"><span data-stu-id="e14f7-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="e14f7-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e14f7-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="e14f7-117">Aktualizowanie istniejącego stanu i trybu z włączonymi zasadami WAF.</span><span class="sxs-lookup"><span data-stu-id="e14f7-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="e14f7-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e14f7-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="e14f7-119">Aktualizowanie wszystkich zasad WAF w $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14f7-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="e14f7-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e14f7-120">PARAMETERS</span></span>

### <span data-ttu-id="e14f7-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="e14f7-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="e14f7-122">Treść niestandardowej odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="e14f7-122">Custom Response Body</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14f7-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="e14f7-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="e14f7-124">Niestandardowy kod stanu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="e14f7-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14f7-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="e14f7-125">-Customrule</span></span>
<span data-ttu-id="e14f7-126">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="e14f7-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="e14f7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14f7-127">-DefaultProfile</span></span>
<span data-ttu-id="e14f7-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e14f7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14f7-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e14f7-129">-EnabledState</span></span>
<span data-ttu-id="e14f7-130">Czy zasady są w stanie włączonym, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="e14f7-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="e14f7-131">Możliwe wartości obejmują: "wyłączone", "włączone"</span><span class="sxs-lookup"><span data-stu-id="e14f7-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="e14f7-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e14f7-132">-InputObject</span></span>
<span data-ttu-id="e14f7-133">Obiekt FireWallPolicy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="e14f7-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="e14f7-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="e14f7-134">-ManagedRule</span></span>
<span data-ttu-id="e14f7-135">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="e14f7-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="e14f7-136">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="e14f7-136">-Mode</span></span>
<span data-ttu-id="e14f7-137">Opisuje, czy jest w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="e14f7-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="e14f7-138">Możliwe wartości obejmują: "Zapobieganie", "wykrywanie".</span><span class="sxs-lookup"><span data-stu-id="e14f7-138">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14f7-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e14f7-139">-Name</span></span>
<span data-ttu-id="e14f7-140">Nazwa FireWallPolicy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="e14f7-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="e14f7-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="e14f7-141">-RedirectUrl</span></span>
<span data-ttu-id="e14f7-142">Adres URL przekierowania</span><span class="sxs-lookup"><span data-stu-id="e14f7-142">Redirect URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14f7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14f7-143">-ResourceGroupName</span></span>
<span data-ttu-id="e14f7-144">Grupa zasobów, do której należy FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="e14f7-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="e14f7-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e14f7-145">-ResourceId</span></span>
<span data-ttu-id="e14f7-146">Identyfikator zasobu FireWallPolicy do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="e14f7-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e14f7-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e14f7-147">-Confirm</span></span>
<span data-ttu-id="e14f7-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14f7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e14f7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14f7-149">-WhatIf</span></span>
<span data-ttu-id="e14f7-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14f7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e14f7-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e14f7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e14f7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14f7-152">CommonParameters</span></span>
<span data-ttu-id="e14f7-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e14f7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14f7-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e14f7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14f7-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e14f7-155">INPUTS</span></span>

### <span data-ttu-id="e14f7-156">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e14f7-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="e14f7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e14f7-157">System.String</span></span>

## <span data-ttu-id="e14f7-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e14f7-158">OUTPUTS</span></span>

### <span data-ttu-id="e14f7-159">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e14f7-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="e14f7-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e14f7-160">NOTES</span></span>

## <span data-ttu-id="e14f7-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e14f7-161">RELATED LINKS</span></span>

<span data-ttu-id="e14f7-162">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Nowe — AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Nowe — AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="e14f7-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
