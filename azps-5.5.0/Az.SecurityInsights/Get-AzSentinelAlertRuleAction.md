---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191218"
---
# <span data-ttu-id="a2d66-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="a2d66-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="a2d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d66-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d66-103">Uzyskiwanie automatycznej odpowiedzi (akcji reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="a2d66-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="a2d66-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a2d66-104">SYNTAX</span></span>

### <span data-ttu-id="a2d66-105">AlertRuleId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a2d66-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d66-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="a2d66-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2d66-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a2d66-107">DESCRIPTION</span></span>
<span data-ttu-id="a2d66-108">Polecenie **cmdlet Get-AzSentinelAlertRuleAction** pobiera odpowiedź automatyczną (akcję reguły alertu) z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a2d66-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="a2d66-109">Jeśli określisz parametry *ActionId* i *AlertRuleId,* zostanie zwrócony jeden **obiekt AlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="a2d66-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="a2d66-110">Jeśli parametr *ActionId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie akcje dla określonej reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a2d66-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="a2d66-111">Obiekt Action **(Akcja)** umożliwia na przykład zmianę akcji **reguły** alertu.</span><span class="sxs-lookup"><span data-stu-id="a2d66-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="a2d66-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a2d66-112">EXAMPLES</span></span>

### <span data-ttu-id="a2d66-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2d66-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="a2d66-114">W tym przykładzie  wszystkie akcje dla określonej reguły alertu są przechowywane w określonym obszarze roboczym, a następnie są przechowywane w $AlertRuleActions obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a2d66-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="a2d66-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2d66-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="a2d66-116">W tym przykładzie **zostanie wpisanie akcji AlertRuleAction** dla określonej reguły alertu w określonym obszarze roboczym, a następnie zostanie on $AlertRuleAction zmienną.</span><span class="sxs-lookup"><span data-stu-id="a2d66-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="a2d66-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2d66-117">PARAMETERS</span></span>

### <span data-ttu-id="a2d66-118">- ActionId</span><span class="sxs-lookup"><span data-stu-id="a2d66-118">-ActionId</span></span>
<span data-ttu-id="a2d66-119">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="a2d66-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d66-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a2d66-120">-AlertRuleId</span></span>
<span data-ttu-id="a2d66-121">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="a2d66-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="a2d66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d66-122">-DefaultProfile</span></span>
<span data-ttu-id="a2d66-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d66-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2d66-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2d66-125">Resource group name.</span></span>

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

### <span data-ttu-id="a2d66-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2d66-126">-WorkspaceName</span></span>
<span data-ttu-id="a2d66-127">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a2d66-127">Workspace Name.</span></span>

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

### <span data-ttu-id="a2d66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d66-128">CommonParameters</span></span>
<span data-ttu-id="a2d66-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d66-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2d66-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d66-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2d66-131">INPUTS</span></span>

### <span data-ttu-id="a2d66-132">Brak</span><span class="sxs-lookup"><span data-stu-id="a2d66-132">None</span></span>
## <span data-ttu-id="a2d66-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2d66-133">OUTPUTS</span></span>

### <span data-ttu-id="a2d66-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="a2d66-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="a2d66-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a2d66-135">NOTES</span></span>

## <span data-ttu-id="a2d66-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2d66-136">RELATED LINKS</span></span>
