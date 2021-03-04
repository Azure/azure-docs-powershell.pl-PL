---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: 80badb2e73aa00fd9a221c20372ab42499c1cb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969898"
---
# <span data-ttu-id="18314-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="18314-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="18314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18314-102">SYNOPSIS</span></span>
<span data-ttu-id="18314-103">Usuwanie zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18314-103">Delete an Incident.</span></span>

## <span data-ttu-id="18314-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18314-104">SYNTAX</span></span>

### <span data-ttu-id="18314-105">IncidentId (Default)</span><span class="sxs-lookup"><span data-stu-id="18314-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18314-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="18314-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18314-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="18314-107">DESCRIPTION</span></span>
<span data-ttu-id="18314-108">Polecenie **cmdlet Remove-AzSentinelIncident** trwale usuwa zdarzenie z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="18314-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="18314-109">Obiekt Incident **można** przekazać za pomocą operatora potoku lub ewentualnie określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="18314-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="18314-110">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="18314-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="18314-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18314-111">EXAMPLES</span></span>

### <span data-ttu-id="18314-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18314-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="18314-113">To polecenie usuwa zdarzenie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="18314-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="18314-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18314-114">PARAMETERS</span></span>

### <span data-ttu-id="18314-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18314-115">-DefaultProfile</span></span>
<span data-ttu-id="18314-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18314-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18314-117">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="18314-117">-IncidentId</span></span>
<span data-ttu-id="18314-118">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="18314-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18314-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18314-119">-InputObject</span></span>
<span data-ttu-id="18314-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="18314-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18314-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18314-121">-PassThru</span></span>
<span data-ttu-id="18314-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="18314-122">PassThru</span></span>

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

### <span data-ttu-id="18314-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18314-123">-ResourceGroupName</span></span>
<span data-ttu-id="18314-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18314-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18314-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="18314-125">-WorkspaceName</span></span>
<span data-ttu-id="18314-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="18314-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18314-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18314-127">-Confirm</span></span>
<span data-ttu-id="18314-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="18314-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18314-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18314-129">-WhatIf</span></span>
<span data-ttu-id="18314-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18314-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18314-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="18314-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18314-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18314-132">CommonParameters</span></span>
<span data-ttu-id="18314-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18314-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18314-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18314-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18314-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18314-135">INPUTS</span></span>

### <span data-ttu-id="18314-136">System.String</span><span class="sxs-lookup"><span data-stu-id="18314-136">System.String</span></span>
### <span data-ttu-id="18314-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="18314-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="18314-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18314-138">OUTPUTS</span></span>

### <span data-ttu-id="18314-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18314-139">System.Boolean</span></span>
## <span data-ttu-id="18314-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18314-140">NOTES</span></span>

## <span data-ttu-id="18314-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18314-141">RELATED LINKS</span></span>
