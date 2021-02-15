---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197890"
---
# <span data-ttu-id="54c5b-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="54c5b-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="54c5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="54c5b-103">Pobiera analizę (reguła alertu).</span><span class="sxs-lookup"><span data-stu-id="54c5b-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="54c5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54c5b-104">SYNTAX</span></span>

### <span data-ttu-id="54c5b-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="54c5b-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c5b-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="54c5b-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c5b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c5b-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c5b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="54c5b-108">DESCRIPTION</span></span>
<span data-ttu-id="54c5b-109">Polecenie **cmdlet Get-AzSentinelAlertRule** pobiera polecenie analityczne (reguła alertu) z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="54c5b-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="54c5b-110">Jeśli określisz *parametr AlertRuleId,* zostanie zwrócony jeden obiekt **AlertRule.**</span><span class="sxs-lookup"><span data-stu-id="54c5b-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="54c5b-111">Jeśli parametr *AlertRuleId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie reguły alertów w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="54c5b-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="54c5b-112">Za pomocą obiektu **AlertRule** można zaktualizować alertRule, na przykład można wyłączyć **alertRule.**</span><span class="sxs-lookup"><span data-stu-id="54c5b-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="54c5b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54c5b-113">EXAMPLES</span></span>

### <span data-ttu-id="54c5b-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54c5b-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="54c5b-115">W tym przykładzie wszystkie **alerty są przechowywane** w określonym obszarze roboczym, a następnie przechowywane w $AlertRules alertów.</span><span class="sxs-lookup"><span data-stu-id="54c5b-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="54c5b-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="54c5b-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="54c5b-117">Ten przykład pobiera **wartość AlertRule** w określonym obszarze roboczym, a następnie zapisuje ją w $AlertRule zmienną.</span><span class="sxs-lookup"><span data-stu-id="54c5b-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="54c5b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54c5b-118">PARAMETERS</span></span>

### <span data-ttu-id="54c5b-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="54c5b-119">-AlertRuleId</span></span>
<span data-ttu-id="54c5b-120">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="54c5b-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c5b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c5b-121">-DefaultProfile</span></span>
<span data-ttu-id="54c5b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54c5b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c5b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c5b-123">-ResourceGroupName</span></span>
<span data-ttu-id="54c5b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54c5b-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c5b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c5b-125">-ResourceId</span></span>
<span data-ttu-id="54c5b-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="54c5b-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c5b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54c5b-127">-WorkspaceName</span></span>
<span data-ttu-id="54c5b-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="54c5b-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c5b-129">CommonParameters</span></span>
<span data-ttu-id="54c5b-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c5b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54c5b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c5b-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54c5b-132">INPUTS</span></span>

### <span data-ttu-id="54c5b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="54c5b-133">System.String</span></span>
## <span data-ttu-id="54c5b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54c5b-134">OUTPUTS</span></span>

### <span data-ttu-id="54c5b-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="54c5b-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="54c5b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54c5b-136">NOTES</span></span>

## <span data-ttu-id="54c5b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54c5b-137">RELATED LINKS</span></span>
