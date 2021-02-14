---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201722"
---
# <span data-ttu-id="ae975-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="ae975-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="ae975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae975-102">SYNOPSIS</span></span>
<span data-ttu-id="ae975-103">Dodawanie komentarza zdarzenia do zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ae975-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="ae975-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae975-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae975-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae975-105">DESCRIPTION</span></span>
<span data-ttu-id="ae975-106">Polecenie **cmdlet New-AzSentinelIncidentComment** tworzy komentarz zdarzenia z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ae975-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="ae975-107">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae975-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ae975-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae975-108">EXAMPLES</span></span>

### <span data-ttu-id="ae975-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae975-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="ae975-110">W tym przykładzie w określonym obszarze roboczym jest określonej wartości typu **IncidentComment,** a następnie jest on $IncidentComment zmienną.</span><span class="sxs-lookup"><span data-stu-id="ae975-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="ae975-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae975-111">PARAMETERS</span></span>

### <span data-ttu-id="ae975-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae975-112">-DefaultProfile</span></span>
<span data-ttu-id="ae975-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae975-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae975-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="ae975-114">-IncidentCommentId</span></span>
<span data-ttu-id="ae975-115">Identyfikator komentarza zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ae975-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="ae975-116">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="ae975-116">-IncidentId</span></span>
<span data-ttu-id="ae975-117">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ae975-117">Incident Id.</span></span>

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

### <span data-ttu-id="ae975-118">— Wiadomość</span><span class="sxs-lookup"><span data-stu-id="ae975-118">-Message</span></span>
<span data-ttu-id="ae975-119">Komunikat o zdarzeniu.</span><span class="sxs-lookup"><span data-stu-id="ae975-119">Incident Message.</span></span>

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

### <span data-ttu-id="ae975-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae975-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae975-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae975-121">Resource group name.</span></span>

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

### <span data-ttu-id="ae975-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ae975-122">-WorkspaceName</span></span>
<span data-ttu-id="ae975-123">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ae975-123">Workspace Name.</span></span>

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

### <span data-ttu-id="ae975-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae975-124">-Confirm</span></span>
<span data-ttu-id="ae975-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae975-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae975-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae975-126">-WhatIf</span></span>
<span data-ttu-id="ae975-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae975-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae975-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae975-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae975-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae975-129">CommonParameters</span></span>
<span data-ttu-id="ae975-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae975-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae975-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae975-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae975-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae975-132">INPUTS</span></span>

### <span data-ttu-id="ae975-133">Brak</span><span class="sxs-lookup"><span data-stu-id="ae975-133">None</span></span>
## <span data-ttu-id="ae975-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae975-134">OUTPUTS</span></span>

### <span data-ttu-id="ae975-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="ae975-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="ae975-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae975-136">NOTES</span></span>

## <span data-ttu-id="ae975-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae975-137">RELATED LINKS</span></span>
