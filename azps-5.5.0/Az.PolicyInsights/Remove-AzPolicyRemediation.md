---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240330"
---
# <span data-ttu-id="271d2-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="271d2-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="271d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="271d2-102">SYNOPSIS</span></span>
<span data-ttu-id="271d2-103">Usuwa działania naprawcze dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="271d2-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="271d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="271d2-104">SYNTAX</span></span>

### <span data-ttu-id="271d2-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="271d2-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="271d2-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="271d2-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="271d2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="271d2-108">DESCRIPTION</span></span>
<span data-ttu-id="271d2-109">Polecenie **cmdlet Remove-AzPolicyRemediation** usuwa działania naprawcze dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="271d2-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="271d2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="271d2-110">EXAMPLES</span></span>

### <span data-ttu-id="271d2-111">Przykład 1. Usunięcie działania naprawczego zasad w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="271d2-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="271d2-112">To polecenie usuwa działania naprawcze o nazwie "remediacja1" w grupie zasobów "mójRG".</span><span class="sxs-lookup"><span data-stu-id="271d2-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="271d2-113">Przykład 2. Usuwanie środków zaradczych grupy zarządzania za pośrednictwem funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="271d2-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="271d2-114">To polecenie usuwa działania naprawcze o nazwie "remediacja1" z grupy zarządzania "mg1".</span><span class="sxs-lookup"><span data-stu-id="271d2-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="271d2-115">Przed usunięciem zasobu zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="271d2-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="271d2-116">Przykład 3. Anulowanie i usuwanie działań naprawczych zasad</span><span class="sxs-lookup"><span data-stu-id="271d2-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="271d2-117">To polecenie usuwa działania naprawcze o nazwie "remediacja1" w grupie zasobów "mójRG".</span><span class="sxs-lookup"><span data-stu-id="271d2-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="271d2-118">Jeśli działania naprawcze są w toku, zostaną one anulowane przed usunięciem.</span><span class="sxs-lookup"><span data-stu-id="271d2-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="271d2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="271d2-119">PARAMETERS</span></span>

### <span data-ttu-id="271d2-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="271d2-120">-AllowStop</span></span>
<span data-ttu-id="271d2-121">Zezwalaj na anulowanie działania naprawczego, jeśli jest ono w toku.</span><span class="sxs-lookup"><span data-stu-id="271d2-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="271d2-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="271d2-122">-AsJob</span></span>
<span data-ttu-id="271d2-123">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="271d2-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="271d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271d2-124">-DefaultProfile</span></span>
<span data-ttu-id="271d2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="271d2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="271d2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="271d2-126">-InputObject</span></span>
<span data-ttu-id="271d2-127">Obiekt Remediation.</span><span class="sxs-lookup"><span data-stu-id="271d2-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="271d2-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="271d2-128">-ManagementGroupName</span></span>
<span data-ttu-id="271d2-129">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="271d2-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="271d2-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="271d2-130">-Name</span></span>
<span data-ttu-id="271d2-131">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="271d2-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="271d2-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="271d2-132">-PassThru</span></span>
<span data-ttu-id="271d2-133">Jeśli polecenie zostanie pomyślnie ukończone, zwróć wartość Prawda.</span><span class="sxs-lookup"><span data-stu-id="271d2-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="271d2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271d2-134">-ResourceGroupName</span></span>
<span data-ttu-id="271d2-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="271d2-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="271d2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="271d2-136">-ResourceId</span></span>
<span data-ttu-id="271d2-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="271d2-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="271d2-138">— Zakres</span><span class="sxs-lookup"><span data-stu-id="271d2-138">-Scope</span></span>
<span data-ttu-id="271d2-139">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="271d2-139">Scope of the resource.</span></span>
<span data-ttu-id="271d2-140">Np.</span><span class="sxs-lookup"><span data-stu-id="271d2-140">E.g.</span></span>
<span data-ttu-id="271d2-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="271d2-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="271d2-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="271d2-142">-Confirm</span></span>
<span data-ttu-id="271d2-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="271d2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="271d2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="271d2-144">-WhatIf</span></span>
<span data-ttu-id="271d2-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="271d2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="271d2-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="271d2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="271d2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271d2-147">CommonParameters</span></span>
<span data-ttu-id="271d2-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271d2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271d2-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="271d2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271d2-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="271d2-150">INPUTS</span></span>

### <span data-ttu-id="271d2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="271d2-151">System.String</span></span>

### <span data-ttu-id="271d2-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="271d2-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="271d2-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="271d2-153">OUTPUTS</span></span>

### <span data-ttu-id="271d2-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="271d2-154">System.Boolean</span></span>

## <span data-ttu-id="271d2-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="271d2-155">NOTES</span></span>

## <span data-ttu-id="271d2-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="271d2-156">RELATED LINKS</span></span>
