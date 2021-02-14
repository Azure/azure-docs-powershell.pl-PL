---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201723"
---
# <span data-ttu-id="8122b-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8122b-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="8122b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8122b-102">SYNOPSIS</span></span>
<span data-ttu-id="8122b-103">Tworzenie zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-103">Create an Incident.</span></span>

## <span data-ttu-id="8122b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8122b-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8122b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8122b-105">DESCRIPTION</span></span>
<span data-ttu-id="8122b-106">Polecenie **cmdlet New-AzSentinelIncident** tworzy zdarzenie z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8122b-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="8122b-107">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8122b-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8122b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8122b-108">EXAMPLES</span></span>

### <span data-ttu-id="8122b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8122b-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="8122b-110">W tym przykładzie **zdarzenie jest tworzyne** w określonym obszarze roboczym, a następnie przechowywane w $Incident zmienną.</span><span class="sxs-lookup"><span data-stu-id="8122b-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="8122b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8122b-111">PARAMETERS</span></span>

### <span data-ttu-id="8122b-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="8122b-112">-ClassificationComment</span></span>
<span data-ttu-id="8122b-113">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="8122b-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="8122b-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="8122b-114">-ClassificationReason</span></span>
<span data-ttu-id="8122b-115">Przyczyna zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-115">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="8122b-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="8122b-116">-Classificaton</span></span>
<span data-ttu-id="8122b-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="8122b-117">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="8122b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8122b-118">-DefaultProfile</span></span>
<span data-ttu-id="8122b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8122b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8122b-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="8122b-120">-Description</span></span>
<span data-ttu-id="8122b-121">Opis.</span><span class="sxs-lookup"><span data-stu-id="8122b-121">Description.</span></span>

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

### <span data-ttu-id="8122b-122">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="8122b-122">-IncidentId</span></span>
<span data-ttu-id="8122b-123">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-123">Incident Id.</span></span>

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

### <span data-ttu-id="8122b-124">— Label</span><span class="sxs-lookup"><span data-stu-id="8122b-124">-Label</span></span>
<span data-ttu-id="8122b-125">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8122b-125">Incident Labels.</span></span>

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

### <span data-ttu-id="8122b-126">— Właściciel</span><span class="sxs-lookup"><span data-stu-id="8122b-126">-Owner</span></span>
<span data-ttu-id="8122b-127">Właściciel zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-127">Incident Owner.</span></span>

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

### <span data-ttu-id="8122b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8122b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8122b-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8122b-129">Resource group name.</span></span>

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

### <span data-ttu-id="8122b-130">— Ważność</span><span class="sxs-lookup"><span data-stu-id="8122b-130">-Severity</span></span>
<span data-ttu-id="8122b-131">Ważność zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-131">Incident Severity.</span></span>

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

### <span data-ttu-id="8122b-132">— Status</span><span class="sxs-lookup"><span data-stu-id="8122b-132">-Status</span></span>
<span data-ttu-id="8122b-133">Stan zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-133">Incident Status.</span></span>

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

### <span data-ttu-id="8122b-134">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="8122b-134">-Title</span></span>
<span data-ttu-id="8122b-135">Tytuł zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8122b-135">Incident Title.</span></span>

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

### <span data-ttu-id="8122b-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8122b-136">-WorkspaceName</span></span>
<span data-ttu-id="8122b-137">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8122b-137">Workspace Name.</span></span>

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

### <span data-ttu-id="8122b-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8122b-138">-Confirm</span></span>
<span data-ttu-id="8122b-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8122b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8122b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8122b-140">-WhatIf</span></span>
<span data-ttu-id="8122b-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8122b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8122b-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8122b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8122b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8122b-143">CommonParameters</span></span>
<span data-ttu-id="8122b-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8122b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8122b-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8122b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8122b-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8122b-146">INPUTS</span></span>

### <span data-ttu-id="8122b-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlet.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8122b-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="8122b-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="8122b-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="8122b-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8122b-149">OUTPUTS</span></span>

### <span data-ttu-id="8122b-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8122b-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="8122b-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8122b-151">NOTES</span></span>

## <span data-ttu-id="8122b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8122b-152">RELATED LINKS</span></span>
