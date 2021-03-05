---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: 6cb65832484c7038f5740c481836d8fe889ebc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005649"
---
# <span data-ttu-id="3e379-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="3e379-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="3e379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e379-102">SYNOPSIS</span></span>
<span data-ttu-id="3e379-103">Tworzenie zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-103">Create an Incident.</span></span>

## <span data-ttu-id="3e379-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e379-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e379-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e379-105">DESCRIPTION</span></span>
<span data-ttu-id="3e379-106">Polecenie **cmdlet New-AzSentinelIncident** tworzy zdarzenie z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3e379-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="3e379-107">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e379-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3e379-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e379-108">EXAMPLES</span></span>

### <span data-ttu-id="3e379-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e379-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="3e379-110">W tym przykładzie **zdarzenie jest tworzyne** w określonym obszarze roboczym, a następnie przechowywane w $Incident zmienną.</span><span class="sxs-lookup"><span data-stu-id="3e379-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="3e379-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e379-111">PARAMETERS</span></span>

### <span data-ttu-id="3e379-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="3e379-112">-ClassificationComment</span></span>
<span data-ttu-id="3e379-113">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="3e379-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="3e379-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="3e379-114">-ClassificationReason</span></span>
<span data-ttu-id="3e379-115">Przyczyna zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="3e379-116">-Classificaton</span></span>
<span data-ttu-id="3e379-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="3e379-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e379-118">-DefaultProfile</span></span>
<span data-ttu-id="3e379-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e379-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e379-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="3e379-120">-Description</span></span>
<span data-ttu-id="3e379-121">Opis.</span><span class="sxs-lookup"><span data-stu-id="3e379-121">Description.</span></span>

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

### <span data-ttu-id="3e379-122">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="3e379-122">-IncidentId</span></span>
<span data-ttu-id="3e379-123">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-123">Incident Id.</span></span>

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

### <span data-ttu-id="3e379-124">— Label</span><span class="sxs-lookup"><span data-stu-id="3e379-124">-Label</span></span>
<span data-ttu-id="3e379-125">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3e379-125">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-126">— Właściciel</span><span class="sxs-lookup"><span data-stu-id="3e379-126">-Owner</span></span>
<span data-ttu-id="3e379-127">Właściciel zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e379-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e379-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e379-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-130">— Ważność</span><span class="sxs-lookup"><span data-stu-id="3e379-130">-Severity</span></span>
<span data-ttu-id="3e379-131">Ważność zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-132">— Status</span><span class="sxs-lookup"><span data-stu-id="3e379-132">-Status</span></span>
<span data-ttu-id="3e379-133">Stan zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-134">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="3e379-134">-Title</span></span>
<span data-ttu-id="3e379-135">Tytuł zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="3e379-135">Incident Title.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e379-136">-WorkspaceName</span></span>
<span data-ttu-id="3e379-137">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3e379-137">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e379-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e379-138">-Confirm</span></span>
<span data-ttu-id="3e379-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e379-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e379-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e379-140">-WhatIf</span></span>
<span data-ttu-id="3e379-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e379-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e379-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3e379-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e379-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e379-143">CommonParameters</span></span>
<span data-ttu-id="3e379-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e379-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e379-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e379-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e379-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e379-146">INPUTS</span></span>

### <span data-ttu-id="3e379-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlet.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3e379-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="3e379-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="3e379-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="3e379-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e379-149">OUTPUTS</span></span>

### <span data-ttu-id="3e379-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="3e379-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="3e379-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e379-151">NOTES</span></span>

## <span data-ttu-id="3e379-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e379-152">RELATED LINKS</span></span>
