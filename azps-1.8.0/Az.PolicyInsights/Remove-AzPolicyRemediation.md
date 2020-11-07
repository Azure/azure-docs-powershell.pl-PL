---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 96afdd5e0bdf336dec5f2ff1b2a9ecfccf8bac12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708790"
---
# <span data-ttu-id="883dd-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="883dd-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="883dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="883dd-102">SYNOPSIS</span></span>
<span data-ttu-id="883dd-103">Usuwa korygowanie zasad.</span><span class="sxs-lookup"><span data-stu-id="883dd-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="883dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="883dd-104">SYNTAX</span></span>

### <span data-ttu-id="883dd-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="883dd-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883dd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="883dd-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883dd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="883dd-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="883dd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="883dd-108">DESCRIPTION</span></span>
<span data-ttu-id="883dd-109">Polecenie cmdlet **Remove-AzPolicyRemediation** usuwa korygowanie zasad.</span><span class="sxs-lookup"><span data-stu-id="883dd-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="883dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="883dd-110">EXAMPLES</span></span>

### <span data-ttu-id="883dd-111">Przykład 1: usuwanie korygowania zasad w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="883dd-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="883dd-112">To polecenie usuwa korygowanie o nazwie "remediation1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="883dd-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="883dd-113">Przykład 2: usuwanie korygowania grupy zarządzania za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="883dd-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="883dd-114">To polecenie usuwa korygowanie o nazwie "remediation1" z grupy zarządzania "MG1".</span><span class="sxs-lookup"><span data-stu-id="883dd-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="883dd-115">Przed usunięciem zasobu zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="883dd-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="883dd-116">Przykład 3: Anulowanie i usuwanie korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="883dd-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="883dd-117">To polecenie usuwa korygowanie o nazwie "remediation1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="883dd-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="883dd-118">Jeśli korygowanie jest w toku, zostanie anulowane przed usunięciem.</span><span class="sxs-lookup"><span data-stu-id="883dd-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="883dd-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="883dd-119">PARAMETERS</span></span>

### <span data-ttu-id="883dd-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="883dd-120">-AllowStop</span></span>
<span data-ttu-id="883dd-121">Zezwalanie na anulowanie korygowania, jeśli jest w toku.</span><span class="sxs-lookup"><span data-stu-id="883dd-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="883dd-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="883dd-122">-AsJob</span></span>
<span data-ttu-id="883dd-123">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="883dd-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="883dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883dd-124">-DefaultProfile</span></span>
<span data-ttu-id="883dd-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="883dd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883dd-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="883dd-126">-InputObject</span></span>
<span data-ttu-id="883dd-127">Obiekt korygowania.</span><span class="sxs-lookup"><span data-stu-id="883dd-127">The Remediation object.</span></span>

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

### <span data-ttu-id="883dd-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="883dd-128">-ManagementGroupName</span></span>
<span data-ttu-id="883dd-129">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="883dd-129">Management group ID.</span></span>

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

### <span data-ttu-id="883dd-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="883dd-130">-Name</span></span>
<span data-ttu-id="883dd-131">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="883dd-131">Resource name.</span></span>

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

### <span data-ttu-id="883dd-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="883dd-132">-PassThru</span></span>
<span data-ttu-id="883dd-133">Zwraca wartość true, jeśli polecenie zostało pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="883dd-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="883dd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883dd-134">-ResourceGroupName</span></span>
<span data-ttu-id="883dd-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="883dd-135">Resource group name.</span></span>

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

### <span data-ttu-id="883dd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="883dd-136">-ResourceId</span></span>
<span data-ttu-id="883dd-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="883dd-137">Resource ID.</span></span>

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

### <span data-ttu-id="883dd-138">-Zakres</span><span class="sxs-lookup"><span data-stu-id="883dd-138">-Scope</span></span>
<span data-ttu-id="883dd-139">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="883dd-139">Scope of the resource.</span></span>
<span data-ttu-id="883dd-140">Przykład.</span><span class="sxs-lookup"><span data-stu-id="883dd-140">E.g.</span></span>
<span data-ttu-id="883dd-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="883dd-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="883dd-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="883dd-142">-Confirm</span></span>
<span data-ttu-id="883dd-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="883dd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883dd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883dd-144">-WhatIf</span></span>
<span data-ttu-id="883dd-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="883dd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="883dd-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="883dd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883dd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883dd-147">CommonParameters</span></span>
<span data-ttu-id="883dd-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="883dd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883dd-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="883dd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883dd-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="883dd-150">INPUTS</span></span>

### <span data-ttu-id="883dd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="883dd-151">System.String</span></span>

### <span data-ttu-id="883dd-152">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="883dd-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="883dd-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="883dd-153">OUTPUTS</span></span>

### <span data-ttu-id="883dd-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="883dd-154">System.Boolean</span></span>

## <span data-ttu-id="883dd-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="883dd-155">NOTES</span></span>

## <span data-ttu-id="883dd-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="883dd-156">RELATED LINKS</span></span>
