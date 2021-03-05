---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 37cc56714712d71ab34adee14a8b758cd9dd1113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986462"
---
# <span data-ttu-id="fd55a-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="fd55a-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="fd55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd55a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd55a-103">Uzyskiwanie automatycznej odpowiedzi (akcji reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="fd55a-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="fd55a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd55a-104">SYNTAX</span></span>

### <span data-ttu-id="fd55a-105">AlertRuleId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fd55a-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd55a-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="fd55a-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd55a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd55a-107">DESCRIPTION</span></span>
<span data-ttu-id="fd55a-108">Polecenie **cmdlet Get-AzSentinelAlertRuleAction** pobiera odpowiedź automatyczną (akcję reguły alertu) z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fd55a-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="fd55a-109">Jeśli określisz parametry *ActionId* i *AlertRuleId,* zostanie zwrócony jeden **obiekt AlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="fd55a-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="fd55a-110">Jeśli parametr *ActionId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie akcje dla określonej reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="fd55a-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="fd55a-111">Obiekt Action **(Akcja)** umożliwia na przykład zmianę akcji **reguły** alertu.</span><span class="sxs-lookup"><span data-stu-id="fd55a-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="fd55a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd55a-112">EXAMPLES</span></span>

### <span data-ttu-id="fd55a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd55a-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="fd55a-114">W tym przykładzie  wszystkie akcje dla określonej reguły alertu są przechowywane w określonym obszarze roboczym, a następnie są przechowywane w $AlertRuleActions obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="fd55a-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="fd55a-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd55a-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="fd55a-116">W tym przykładzie **zostanie wpisanie akcji AlertRuleAction** dla określonej reguły alertu w określonym obszarze roboczym, a następnie zostanie on $AlertRuleAction zmienną.</span><span class="sxs-lookup"><span data-stu-id="fd55a-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="fd55a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd55a-117">PARAMETERS</span></span>

### <span data-ttu-id="fd55a-118">- ActionId</span><span class="sxs-lookup"><span data-stu-id="fd55a-118">-ActionId</span></span>
<span data-ttu-id="fd55a-119">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="fd55a-119">Action Id.</span></span>

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

### <span data-ttu-id="fd55a-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fd55a-120">-AlertRuleId</span></span>
<span data-ttu-id="fd55a-121">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="fd55a-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="fd55a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd55a-122">-DefaultProfile</span></span>
<span data-ttu-id="fd55a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd55a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd55a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd55a-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd55a-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd55a-125">Resource group name.</span></span>

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

### <span data-ttu-id="fd55a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd55a-126">-WorkspaceName</span></span>
<span data-ttu-id="fd55a-127">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fd55a-127">Workspace Name.</span></span>

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

### <span data-ttu-id="fd55a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd55a-128">CommonParameters</span></span>
<span data-ttu-id="fd55a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd55a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd55a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd55a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd55a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd55a-131">INPUTS</span></span>

### <span data-ttu-id="fd55a-132">Brak</span><span class="sxs-lookup"><span data-stu-id="fd55a-132">None</span></span>
## <span data-ttu-id="fd55a-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd55a-133">OUTPUTS</span></span>

### <span data-ttu-id="fd55a-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="fd55a-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="fd55a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd55a-135">NOTES</span></span>

## <span data-ttu-id="fd55a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd55a-136">RELATED LINKS</span></span>
