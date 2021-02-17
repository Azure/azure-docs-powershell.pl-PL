---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: a3358681fd501602833f0168a6920dc2c3ec7864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243515"
---
# <span data-ttu-id="478da-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="478da-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="478da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478da-102">SYNOPSIS</span></span>
<span data-ttu-id="478da-103">Aktualizowanie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="478da-103">Update WAF policy</span></span>

## <span data-ttu-id="478da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="478da-104">SYNTAX</span></span>

### <span data-ttu-id="478da-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="478da-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478da-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="478da-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478da-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="478da-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478da-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="478da-108">DESCRIPTION</span></span>
<span data-ttu-id="478da-109">Polecenie **cmdlet Update-AzFrontDoorWafPolicy** aktualizuje istniejące zasady WAF.</span><span class="sxs-lookup"><span data-stu-id="478da-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="478da-110">Jeśli parametry wejściowe nie zostaną podane, zostaną użyte stare parametry z istniejących zasad SAF.</span><span class="sxs-lookup"><span data-stu-id="478da-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="478da-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="478da-111">EXAMPLES</span></span>

### <span data-ttu-id="478da-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="478da-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="478da-113">Aktualizowanie istniejącego niestandardowego kodu stanu zasad WAF.</span><span class="sxs-lookup"><span data-stu-id="478da-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="478da-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="478da-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="478da-115">Aktualizowanie istniejącego trybu zasad SAF.</span><span class="sxs-lookup"><span data-stu-id="478da-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="478da-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="478da-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="478da-117">Aktualizowanie stanu i trybu z włączonymi zasadami WAF.</span><span class="sxs-lookup"><span data-stu-id="478da-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="478da-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="478da-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="478da-119">Aktualizowanie wszystkich zasad SAF w programie $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478da-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="478da-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="478da-120">PARAMETERS</span></span>

### <span data-ttu-id="478da-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="478da-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="478da-122">Niestandardowa treść odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="478da-122">Custom Response Body</span></span>

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

### <span data-ttu-id="478da-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="478da-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="478da-124">Niestandardowy kod stanu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="478da-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="478da-125">— Customrule</span><span class="sxs-lookup"><span data-stu-id="478da-125">-Customrule</span></span>
<span data-ttu-id="478da-126">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="478da-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="478da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478da-127">-DefaultProfile</span></span>
<span data-ttu-id="478da-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="478da-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="478da-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="478da-129">-EnabledState</span></span>
<span data-ttu-id="478da-130">Czy zasady są w stanie włączonym, czy wyłączonym.</span><span class="sxs-lookup"><span data-stu-id="478da-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="478da-131">Możliwe wartości: "Wyłączone", "Włączone"</span><span class="sxs-lookup"><span data-stu-id="478da-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="478da-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="478da-132">-InputObject</span></span>
<span data-ttu-id="478da-133">Obiekt FireWallPolicy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="478da-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="478da-134">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="478da-134">-ManagedRule</span></span>
<span data-ttu-id="478da-135">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="478da-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="478da-136">— tryb</span><span class="sxs-lookup"><span data-stu-id="478da-136">-Mode</span></span>
<span data-ttu-id="478da-137">W tym artykule opisano, czy jest on w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="478da-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="478da-138">Możliwe wartości to: 'Zapobieganie', 'Wykrywanie'.</span><span class="sxs-lookup"><span data-stu-id="478da-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="478da-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="478da-139">-Name</span></span>
<span data-ttu-id="478da-140">Nazwa aktualizacji firewallpolicy.</span><span class="sxs-lookup"><span data-stu-id="478da-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="478da-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="478da-141">-RedirectUrl</span></span>
<span data-ttu-id="478da-142">Adres URL przekierowania</span><span class="sxs-lookup"><span data-stu-id="478da-142">Redirect URL</span></span>

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

### <span data-ttu-id="478da-143">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="478da-143">-RequestBodyCheck</span></span>
<span data-ttu-id="478da-144">Definiuje, czy treść powinna być sprawdzana przez reguły zarządzane.</span><span class="sxs-lookup"><span data-stu-id="478da-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="478da-145">Możliwe wartości: "Włączone", "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="478da-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="478da-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478da-146">-ResourceGroupName</span></span>
<span data-ttu-id="478da-147">Grupa zasobów, do której należy grupa FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="478da-147">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="478da-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="478da-148">-ResourceId</span></span>
<span data-ttu-id="478da-149">Identyfikator zasobu aktualizacji FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="478da-149">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="478da-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="478da-150">-Confirm</span></span>
<span data-ttu-id="478da-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="478da-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478da-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478da-152">-WhatIf</span></span>
<span data-ttu-id="478da-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="478da-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478da-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="478da-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478da-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478da-155">CommonParameters</span></span>
<span data-ttu-id="478da-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478da-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478da-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="478da-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478da-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="478da-158">INPUTS</span></span>

### <span data-ttu-id="478da-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="478da-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="478da-160">System.String</span><span class="sxs-lookup"><span data-stu-id="478da-160">System.String</span></span>

## <span data-ttu-id="478da-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="478da-161">OUTPUTS</span></span>

### <span data-ttu-id="478da-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="478da-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="478da-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="478da-163">NOTES</span></span>

## <span data-ttu-id="478da-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="478da-164">RELATED LINKS</span></span>

<span data-ttu-id="478da-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="478da-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
