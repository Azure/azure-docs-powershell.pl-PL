---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502965"
---
# <span data-ttu-id="d9b4b-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="d9b4b-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="d9b4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b4b-103">Dodawanie komentarza dotyczącego incydentu do incydentu.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="d9b4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9b4b-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b4b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b4b-106">Polecenie cmdlet **New-AzSentinelIncidentComment** umożliwia utworzenie komentarza dotyczącego incydentu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="d9b4b-107">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d9b4b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9b4b-108">EXAMPLES</span></span>

### <span data-ttu-id="d9b4b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9b4b-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="d9b4b-110">W tym przykładzie przedstawiono tworzenie **IncidentComment** w określonym obszarze roboczym, a następnie przechowywanie go w zmiennej $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="d9b4b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9b4b-111">PARAMETERS</span></span>

### <span data-ttu-id="d9b4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b4b-112">-DefaultProfile</span></span>
<span data-ttu-id="d9b4b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b4b-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="d9b4b-114">-IncidentCommentId</span></span>
<span data-ttu-id="d9b4b-115">Identyfikator komentarza dotyczącego incydentu.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="d9b4b-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="d9b4b-116">-IncidentId</span></span>
<span data-ttu-id="d9b4b-117">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-117">Incident Id.</span></span>

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

### <span data-ttu-id="d9b4b-118">-Message</span><span class="sxs-lookup"><span data-stu-id="d9b4b-118">-Message</span></span>
<span data-ttu-id="d9b4b-119">Komunikat o zdarzeniu.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-119">Incident Message.</span></span>

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

### <span data-ttu-id="d9b4b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b4b-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9b4b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-121">Resource group name.</span></span>

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

### <span data-ttu-id="d9b4b-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d9b4b-122">-WorkspaceName</span></span>
<span data-ttu-id="d9b4b-123">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-123">Workspace Name.</span></span>

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

### <span data-ttu-id="d9b4b-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9b4b-124">-Confirm</span></span>
<span data-ttu-id="d9b4b-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b4b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b4b-126">-WhatIf</span></span>
<span data-ttu-id="d9b4b-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9b4b-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b4b-129">CommonParameters</span></span>
<span data-ttu-id="d9b4b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b4b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9b4b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b4b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9b4b-132">INPUTS</span></span>

### <span data-ttu-id="d9b4b-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9b4b-133">None</span></span>
## <span data-ttu-id="d9b4b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9b4b-134">OUTPUTS</span></span>

### <span data-ttu-id="d9b4b-135">Microsoft. Azure. Commands. SecurityInsights. models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="d9b4b-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="d9b4b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9b4b-136">NOTES</span></span>

## <span data-ttu-id="d9b4b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9b4b-137">RELATED LINKS</span></span>
