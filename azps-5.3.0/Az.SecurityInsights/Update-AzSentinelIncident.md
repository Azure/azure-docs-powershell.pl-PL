---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502945"
---
# <span data-ttu-id="8980c-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8980c-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="8980c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8980c-102">SYNOPSIS</span></span>
<span data-ttu-id="8980c-103">Zaktualizuj zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="8980c-103">Update an Incident.</span></span>

## <span data-ttu-id="8980c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8980c-104">SYNTAX</span></span>

### <span data-ttu-id="8980c-105">IncidentId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8980c-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8980c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="8980c-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8980c-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8980c-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8980c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8980c-108">DESCRIPTION</span></span>
<span data-ttu-id="8980c-109">Polecenie cmdlet **Update-AzSentinelIncident** aktualizuje zdarzenie w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8980c-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="8980c-110">Obiekt **incydentu** można przekazać jako parametr lub za pomocą operatora potoku lub można też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="8980c-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="8980c-111">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8980c-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8980c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8980c-112">EXAMPLES</span></span>

### <span data-ttu-id="8980c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8980c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="8980c-114">Polecenie pobiera zdarzenie przez *IncidentId* i ustawia wartość właściwości *waga* na *wysoki*.</span><span class="sxs-lookup"><span data-stu-id="8980c-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="8980c-115">Pozostałe właściwości pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="8980c-115">All other properties remain the same.</span></span>

## <span data-ttu-id="8980c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8980c-116">PARAMETERS</span></span>

### <span data-ttu-id="8980c-117">-Klasyfikacja</span><span class="sxs-lookup"><span data-stu-id="8980c-117">-Classification</span></span>
<span data-ttu-id="8980c-118">Incydent Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="8980c-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="8980c-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="8980c-119">-ClassificationComment</span></span>
<span data-ttu-id="8980c-120">Komentarz dotyczący incydentu Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="8980c-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="8980c-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="8980c-121">-ClassificationReason</span></span>
<span data-ttu-id="8980c-122">Przyczyna Classificaiton incydentu.</span><span class="sxs-lookup"><span data-stu-id="8980c-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="8980c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8980c-123">-DefaultProfile</span></span>
<span data-ttu-id="8980c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8980c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8980c-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="8980c-125">-Description</span></span>
<span data-ttu-id="8980c-126">Opis.</span><span class="sxs-lookup"><span data-stu-id="8980c-126">Description.</span></span>

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

### <span data-ttu-id="8980c-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="8980c-127">-IncidentID</span></span>
<span data-ttu-id="8980c-128">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8980c-128">Incident Id.</span></span>

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

### <span data-ttu-id="8980c-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8980c-129">-InputObject</span></span>
<span data-ttu-id="8980c-130">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="8980c-130">InputObject.</span></span>

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

### <span data-ttu-id="8980c-131">-Label</span><span class="sxs-lookup"><span data-stu-id="8980c-131">-Label</span></span>
<span data-ttu-id="8980c-132">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8980c-132">Incident Labels.</span></span>

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

### <span data-ttu-id="8980c-133">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="8980c-133">-Owner</span></span>
<span data-ttu-id="8980c-134">Właściciel zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="8980c-134">Incident Owner.</span></span>

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

### <span data-ttu-id="8980c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8980c-135">-ResourceGroupName</span></span>
<span data-ttu-id="8980c-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8980c-136">Resource group name.</span></span>

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

### <span data-ttu-id="8980c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8980c-137">-ResourceId</span></span>
<span data-ttu-id="8980c-138">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8980c-138">Resource Id.</span></span>

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

### <span data-ttu-id="8980c-139">— Ważność</span><span class="sxs-lookup"><span data-stu-id="8980c-139">-Severity</span></span>
<span data-ttu-id="8980c-140">Ważność incydentu.</span><span class="sxs-lookup"><span data-stu-id="8980c-140">Incident Severity.</span></span>

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

### <span data-ttu-id="8980c-141">-Status</span><span class="sxs-lookup"><span data-stu-id="8980c-141">-Status</span></span>
<span data-ttu-id="8980c-142">Status incydentu.</span><span class="sxs-lookup"><span data-stu-id="8980c-142">Incident Status.</span></span>

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

### <span data-ttu-id="8980c-143">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="8980c-143">-Title</span></span>
<span data-ttu-id="8980c-144">Tytuł incydentu.</span><span class="sxs-lookup"><span data-stu-id="8980c-144">Incident Title.</span></span>

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

### <span data-ttu-id="8980c-145">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8980c-145">-WorkspaceName</span></span>
<span data-ttu-id="8980c-146">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8980c-146">Workspace Name.</span></span>

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

### <span data-ttu-id="8980c-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8980c-147">-Confirm</span></span>
<span data-ttu-id="8980c-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8980c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8980c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8980c-149">-WhatIf</span></span>
<span data-ttu-id="8980c-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8980c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8980c-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8980c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8980c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8980c-152">CommonParameters</span></span>
<span data-ttu-id="8980c-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8980c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8980c-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8980c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8980c-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8980c-155">INPUTS</span></span>

### <span data-ttu-id="8980c-156">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8980c-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="8980c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8980c-157">System.String</span></span>

### <span data-ttu-id="8980c-158">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncidentLabel, Microsoft. Azure. PowerShell. cmdlets. SecurityInsights, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8980c-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8980c-159">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="8980c-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="8980c-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8980c-160">OUTPUTS</span></span>

### <span data-ttu-id="8980c-161">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8980c-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="8980c-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8980c-162">NOTES</span></span>

## <span data-ttu-id="8980c-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8980c-163">RELATED LINKS</span></span>
