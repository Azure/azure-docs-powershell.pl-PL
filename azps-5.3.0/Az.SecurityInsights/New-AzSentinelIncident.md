---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502970"
---
# <span data-ttu-id="43ce1-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="43ce1-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="43ce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="43ce1-103">Tworzenie incydentu.</span><span class="sxs-lookup"><span data-stu-id="43ce1-103">Create an Incident.</span></span>

## <span data-ttu-id="43ce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43ce1-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ce1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="43ce1-106">Polecenie cmdlet **New-AzSentinelIncident** tworzy zdarzenie z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="43ce1-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="43ce1-107">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="43ce1-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="43ce1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43ce1-108">EXAMPLES</span></span>

### <span data-ttu-id="43ce1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43ce1-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="43ce1-110">W tym przykładzie przedstawiono tworzenie **incydentu** w określonym obszarze roboczym, a następnie zapisanie go w zmiennej $Incident.</span><span class="sxs-lookup"><span data-stu-id="43ce1-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="43ce1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43ce1-111">PARAMETERS</span></span>

### <span data-ttu-id="43ce1-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="43ce1-112">-ClassificationComment</span></span>
<span data-ttu-id="43ce1-113">Komentarz dotyczący incydentu Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="43ce1-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="43ce1-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="43ce1-114">-ClassificationReason</span></span>
<span data-ttu-id="43ce1-115">Przyczyna Classificaiton incydentu.</span><span class="sxs-lookup"><span data-stu-id="43ce1-115">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="43ce1-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="43ce1-116">-Classificaton</span></span>
<span data-ttu-id="43ce1-117">Incydent Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="43ce1-117">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="43ce1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ce1-118">-DefaultProfile</span></span>
<span data-ttu-id="43ce1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43ce1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ce1-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="43ce1-120">-Description</span></span>
<span data-ttu-id="43ce1-121">Opis.</span><span class="sxs-lookup"><span data-stu-id="43ce1-121">Description.</span></span>

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

### <span data-ttu-id="43ce1-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="43ce1-122">-IncidentId</span></span>
<span data-ttu-id="43ce1-123">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="43ce1-123">Incident Id.</span></span>

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

### <span data-ttu-id="43ce1-124">-Label</span><span class="sxs-lookup"><span data-stu-id="43ce1-124">-Label</span></span>
<span data-ttu-id="43ce1-125">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="43ce1-125">Incident Labels.</span></span>

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

### <span data-ttu-id="43ce1-126">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="43ce1-126">-Owner</span></span>
<span data-ttu-id="43ce1-127">Właściciel zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="43ce1-127">Incident Owner.</span></span>

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

### <span data-ttu-id="43ce1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ce1-128">-ResourceGroupName</span></span>
<span data-ttu-id="43ce1-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43ce1-129">Resource group name.</span></span>

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

### <span data-ttu-id="43ce1-130">— Ważność</span><span class="sxs-lookup"><span data-stu-id="43ce1-130">-Severity</span></span>
<span data-ttu-id="43ce1-131">Ważność incydentu.</span><span class="sxs-lookup"><span data-stu-id="43ce1-131">Incident Severity.</span></span>

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

### <span data-ttu-id="43ce1-132">-Status</span><span class="sxs-lookup"><span data-stu-id="43ce1-132">-Status</span></span>
<span data-ttu-id="43ce1-133">Status incydentu.</span><span class="sxs-lookup"><span data-stu-id="43ce1-133">Incident Status.</span></span>

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

### <span data-ttu-id="43ce1-134">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="43ce1-134">-Title</span></span>
<span data-ttu-id="43ce1-135">Tytuł incydentu.</span><span class="sxs-lookup"><span data-stu-id="43ce1-135">Incident Title.</span></span>

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

### <span data-ttu-id="43ce1-136">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="43ce1-136">-WorkspaceName</span></span>
<span data-ttu-id="43ce1-137">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="43ce1-137">Workspace Name.</span></span>

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

### <span data-ttu-id="43ce1-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43ce1-138">-Confirm</span></span>
<span data-ttu-id="43ce1-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ce1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ce1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ce1-140">-WhatIf</span></span>
<span data-ttu-id="43ce1-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ce1-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43ce1-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43ce1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ce1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ce1-143">CommonParameters</span></span>
<span data-ttu-id="43ce1-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ce1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ce1-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43ce1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ce1-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43ce1-146">INPUTS</span></span>

### <span data-ttu-id="43ce1-147">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncidentLabel, Microsoft. Azure. PowerShell. cmdlets. SecurityInsights, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="43ce1-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="43ce1-148">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="43ce1-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="43ce1-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43ce1-149">OUTPUTS</span></span>

### <span data-ttu-id="43ce1-150">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="43ce1-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="43ce1-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43ce1-151">NOTES</span></span>

## <span data-ttu-id="43ce1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43ce1-152">RELATED LINKS</span></span>
