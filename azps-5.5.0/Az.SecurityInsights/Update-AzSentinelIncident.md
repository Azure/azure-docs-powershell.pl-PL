---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189123"
---
# <span data-ttu-id="18c24-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="18c24-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="18c24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18c24-102">SYNOPSIS</span></span>
<span data-ttu-id="18c24-103">Zaktualizuj zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="18c24-103">Update an Incident.</span></span>

## <span data-ttu-id="18c24-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18c24-104">SYNTAX</span></span>

### <span data-ttu-id="18c24-105">IncidentId (Default)</span><span class="sxs-lookup"><span data-stu-id="18c24-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c24-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="18c24-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c24-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="18c24-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18c24-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="18c24-108">DESCRIPTION</span></span>
<span data-ttu-id="18c24-109">Polecenie **cmdlet Update-AzSentinelIncident** aktualizuje zdarzenie w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="18c24-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="18c24-110">Obiekt Incident **można** przekazać jako parametr lub za pomocą operatora potoku albo określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="18c24-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="18c24-111">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="18c24-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="18c24-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18c24-112">EXAMPLES</span></span>

### <span data-ttu-id="18c24-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18c24-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="18c24-114">Polecenie pobiera wartość Incident by *IncidentId* i ustawia dla *właściwości Ważność* wartość *Wysoka.*</span><span class="sxs-lookup"><span data-stu-id="18c24-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="18c24-115">Wszystkie pozostałe właściwości pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="18c24-115">All other properties remain the same.</span></span>

## <span data-ttu-id="18c24-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18c24-116">PARAMETERS</span></span>

### <span data-ttu-id="18c24-117">— Klasyfikacja</span><span class="sxs-lookup"><span data-stu-id="18c24-117">-Classification</span></span>
<span data-ttu-id="18c24-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="18c24-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="18c24-119">-ClassificationComment</span></span>
<span data-ttu-id="18c24-120">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="18c24-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="18c24-121">-ClassificationReason</span></span>
<span data-ttu-id="18c24-122">Przyczyna zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18c24-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c24-123">-DefaultProfile</span></span>
<span data-ttu-id="18c24-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18c24-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="18c24-125">-Description</span></span>
<span data-ttu-id="18c24-126">Opis.</span><span class="sxs-lookup"><span data-stu-id="18c24-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-127">- IncidentID</span><span class="sxs-lookup"><span data-stu-id="18c24-127">-IncidentID</span></span>
<span data-ttu-id="18c24-128">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18c24-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18c24-129">-InputObject</span></span>
<span data-ttu-id="18c24-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="18c24-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-131">— Label</span><span class="sxs-lookup"><span data-stu-id="18c24-131">-Label</span></span>
<span data-ttu-id="18c24-132">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="18c24-132">Incident Labels.</span></span>

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

### <span data-ttu-id="18c24-133">— Właściciel</span><span class="sxs-lookup"><span data-stu-id="18c24-133">-Owner</span></span>
<span data-ttu-id="18c24-134">Właściciel zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18c24-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c24-135">-ResourceGroupName</span></span>
<span data-ttu-id="18c24-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18c24-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18c24-137">-ResourceId</span></span>
<span data-ttu-id="18c24-138">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="18c24-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-139">— Ważność</span><span class="sxs-lookup"><span data-stu-id="18c24-139">-Severity</span></span>
<span data-ttu-id="18c24-140">Ważność zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18c24-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-141">— Status</span><span class="sxs-lookup"><span data-stu-id="18c24-141">-Status</span></span>
<span data-ttu-id="18c24-142">Stan zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18c24-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-143">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="18c24-143">-Title</span></span>
<span data-ttu-id="18c24-144">Tytuł zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18c24-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="18c24-145">-WorkspaceName</span></span>
<span data-ttu-id="18c24-146">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="18c24-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18c24-147">-Confirm</span></span>
<span data-ttu-id="18c24-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="18c24-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c24-149">-WhatIf</span></span>
<span data-ttu-id="18c24-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18c24-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c24-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="18c24-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c24-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c24-152">CommonParameters</span></span>
<span data-ttu-id="18c24-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c24-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c24-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18c24-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c24-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18c24-155">INPUTS</span></span>

### <span data-ttu-id="18c24-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="18c24-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="18c24-157">System.String</span><span class="sxs-lookup"><span data-stu-id="18c24-157">System.String</span></span>

### <span data-ttu-id="18c24-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlet.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="18c24-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="18c24-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="18c24-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="18c24-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18c24-160">OUTPUTS</span></span>

### <span data-ttu-id="18c24-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="18c24-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="18c24-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18c24-162">NOTES</span></span>

## <span data-ttu-id="18c24-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18c24-163">RELATED LINKS</span></span>
