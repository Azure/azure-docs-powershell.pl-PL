---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2eb9d5a11b160a1061bbd769f337cf053b6ad805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989059"
---
# <span data-ttu-id="ff23f-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ff23f-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="ff23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff23f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff23f-103">Anulowanie rozwiązywania problemów z zasadami w toku.</span><span class="sxs-lookup"><span data-stu-id="ff23f-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="ff23f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff23f-104">SYNTAX</span></span>

### <span data-ttu-id="ff23f-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="ff23f-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff23f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff23f-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff23f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff23f-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff23f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff23f-108">DESCRIPTION</span></span>
<span data-ttu-id="ff23f-109">Polecenie **cmdlet Stop-AzPolicyRemediation** anuluje działania naprawcze dotyczące zasad w toku.</span><span class="sxs-lookup"><span data-stu-id="ff23f-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="ff23f-110">Aktywne wdrożenia zostaną anulowane i nie zostaną utworzone żadne nowe wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff23f-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="ff23f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff23f-111">EXAMPLES</span></span>

### <span data-ttu-id="ff23f-112">Przykład 1. Anulowanie działania naprawczego zasad w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ff23f-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="ff23f-113">To polecenie anuluje działania naprawcze o nazwie "remediacja1" w grupie zasobów "mójRG".</span><span class="sxs-lookup"><span data-stu-id="ff23f-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="ff23f-114">Przykład 2. Anulowanie rozwiązywania problemów grupy zarządzania za pośrednictwem instalacji rurowych</span><span class="sxs-lookup"><span data-stu-id="ff23f-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="ff23f-115">To polecenie anuluje działania naprawcze o nazwie "remediacja1" w grupie zarządzania "mg1".</span><span class="sxs-lookup"><span data-stu-id="ff23f-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="ff23f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff23f-116">PARAMETERS</span></span>

### <span data-ttu-id="ff23f-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ff23f-117">-AsJob</span></span>
<span data-ttu-id="ff23f-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="ff23f-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ff23f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff23f-119">-DefaultProfile</span></span>
<span data-ttu-id="ff23f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff23f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff23f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff23f-121">-InputObject</span></span>
<span data-ttu-id="ff23f-122">Obiekt Remediation.</span><span class="sxs-lookup"><span data-stu-id="ff23f-122">The Remediation object.</span></span>

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

### <span data-ttu-id="ff23f-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ff23f-123">-ManagementGroupName</span></span>
<span data-ttu-id="ff23f-124">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ff23f-124">Management group ID.</span></span>

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

### <span data-ttu-id="ff23f-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff23f-125">-Name</span></span>
<span data-ttu-id="ff23f-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff23f-126">Resource name.</span></span>

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

### <span data-ttu-id="ff23f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff23f-127">-PassThru</span></span>
<span data-ttu-id="ff23f-128">Jeśli polecenie zostanie pomyślnie ukończone, zwróć wartość Prawda.</span><span class="sxs-lookup"><span data-stu-id="ff23f-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="ff23f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff23f-129">-ResourceGroupName</span></span>
<span data-ttu-id="ff23f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff23f-130">Resource group name.</span></span>

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

### <span data-ttu-id="ff23f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff23f-131">-ResourceId</span></span>
<span data-ttu-id="ff23f-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff23f-132">Resource ID.</span></span>

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

### <span data-ttu-id="ff23f-133">— Zakres</span><span class="sxs-lookup"><span data-stu-id="ff23f-133">-Scope</span></span>
<span data-ttu-id="ff23f-134">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff23f-134">Scope of the resource.</span></span>
<span data-ttu-id="ff23f-135">Np.</span><span class="sxs-lookup"><span data-stu-id="ff23f-135">E.g.</span></span>
<span data-ttu-id="ff23f-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="ff23f-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="ff23f-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff23f-137">-Confirm</span></span>
<span data-ttu-id="ff23f-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff23f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff23f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff23f-139">-WhatIf</span></span>
<span data-ttu-id="ff23f-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff23f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff23f-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ff23f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff23f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff23f-142">CommonParameters</span></span>
<span data-ttu-id="ff23f-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff23f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff23f-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff23f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff23f-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff23f-145">INPUTS</span></span>

### <span data-ttu-id="ff23f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ff23f-146">System.String</span></span>

### <span data-ttu-id="ff23f-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="ff23f-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="ff23f-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff23f-148">OUTPUTS</span></span>

### <span data-ttu-id="ff23f-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff23f-149">System.Boolean</span></span>

## <span data-ttu-id="ff23f-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff23f-150">NOTES</span></span>

## <span data-ttu-id="ff23f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff23f-151">RELATED LINKS</span></span>
