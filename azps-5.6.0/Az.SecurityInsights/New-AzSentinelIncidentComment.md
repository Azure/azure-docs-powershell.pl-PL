---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 0fe04e773e02a8b6b61f9c57d8316ac8936f05aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963674"
---
# <span data-ttu-id="0e144-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="0e144-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="0e144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e144-102">SYNOPSIS</span></span>
<span data-ttu-id="0e144-103">Dodawanie komentarza zdarzenia do zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="0e144-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="0e144-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e144-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e144-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e144-105">DESCRIPTION</span></span>
<span data-ttu-id="0e144-106">Polecenie **cmdlet New-AzSentinelIncidentComment** tworzy komentarz zdarzenia z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0e144-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="0e144-107">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e144-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0e144-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e144-108">EXAMPLES</span></span>

### <span data-ttu-id="0e144-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e144-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="0e144-110">W tym przykładzie w określonym obszarze roboczym jest określonej wartości typu **IncidentComment,** a następnie jest on $IncidentComment zmienną.</span><span class="sxs-lookup"><span data-stu-id="0e144-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="0e144-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e144-111">PARAMETERS</span></span>

### <span data-ttu-id="0e144-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e144-112">-DefaultProfile</span></span>
<span data-ttu-id="0e144-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e144-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e144-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="0e144-114">-IncidentCommentId</span></span>
<span data-ttu-id="0e144-115">Identyfikator komentarza zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="0e144-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="0e144-116">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="0e144-116">-IncidentId</span></span>
<span data-ttu-id="0e144-117">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="0e144-117">Incident Id.</span></span>

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

### <span data-ttu-id="0e144-118">— Wiadomość</span><span class="sxs-lookup"><span data-stu-id="0e144-118">-Message</span></span>
<span data-ttu-id="0e144-119">Komunikat o zdarzeniu.</span><span class="sxs-lookup"><span data-stu-id="0e144-119">Incident Message.</span></span>

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

### <span data-ttu-id="0e144-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e144-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e144-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e144-121">Resource group name.</span></span>

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

### <span data-ttu-id="0e144-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e144-122">-WorkspaceName</span></span>
<span data-ttu-id="0e144-123">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0e144-123">Workspace Name.</span></span>

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

### <span data-ttu-id="0e144-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e144-124">-Confirm</span></span>
<span data-ttu-id="0e144-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e144-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e144-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e144-126">-WhatIf</span></span>
<span data-ttu-id="0e144-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e144-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e144-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0e144-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e144-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e144-129">CommonParameters</span></span>
<span data-ttu-id="0e144-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e144-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e144-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e144-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e144-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e144-132">INPUTS</span></span>

### <span data-ttu-id="0e144-133">Brak</span><span class="sxs-lookup"><span data-stu-id="0e144-133">None</span></span>
## <span data-ttu-id="0e144-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e144-134">OUTPUTS</span></span>

### <span data-ttu-id="0e144-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="0e144-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="0e144-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e144-136">NOTES</span></span>

## <span data-ttu-id="0e144-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e144-137">RELATED LINKS</span></span>
