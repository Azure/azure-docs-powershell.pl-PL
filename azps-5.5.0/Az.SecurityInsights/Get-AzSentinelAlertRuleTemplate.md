---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183546"
---
# <span data-ttu-id="d297a-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="d297a-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="d297a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d297a-102">SYNOPSIS</span></span>
<span data-ttu-id="d297a-103">Pobierz szablon reguły analitycznej.</span><span class="sxs-lookup"><span data-stu-id="d297a-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="d297a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d297a-104">SYNTAX</span></span>

### <span data-ttu-id="d297a-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d297a-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d297a-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="d297a-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d297a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d297a-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d297a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d297a-108">DESCRIPTION</span></span>
<span data-ttu-id="d297a-109">Polecenie **cmdlet Get-AzSentinelAlertRuleTemplate** pobiera szablon reguły alertu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d297a-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="d297a-110">W przypadku określenia *parametru AlertRuleTemplateId* jest zwracany jeden **obiekt AlertRuleTemplate.**</span><span class="sxs-lookup"><span data-stu-id="d297a-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="d297a-111">Jeśli parametr *AlertRuleTemplateId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie szablony reguł alertów w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="d297a-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="d297a-112">Za pomocą obiektu **AlertRuleTemplate** można utworzyć nową regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="d297a-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="d297a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d297a-113">EXAMPLES</span></span>

### <span data-ttu-id="d297a-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d297a-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="d297a-115">W tym przykładzie wszystkie **alertyRuleTemplates** są przechowywane w określonym obszarze roboczym, a następnie są przechowywane $AlertRuleTemplates zmienną.</span><span class="sxs-lookup"><span data-stu-id="d297a-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="d297a-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d297a-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="d297a-117">W tym przykładzie **element AlertRuleTemplate** jest przechowywany w określonym obszarze roboczym, a następnie jest on $AlertRuleTemplate zmienną.</span><span class="sxs-lookup"><span data-stu-id="d297a-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="d297a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d297a-118">PARAMETERS</span></span>

### <span data-ttu-id="d297a-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="d297a-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="d297a-120">Identyfikator reguły alertu szablonu.</span><span class="sxs-lookup"><span data-stu-id="d297a-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d297a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d297a-121">-DefaultProfile</span></span>
<span data-ttu-id="d297a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d297a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d297a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d297a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d297a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d297a-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d297a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d297a-125">-ResourceId</span></span>
<span data-ttu-id="d297a-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d297a-126">Resource Id.</span></span>

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

### <span data-ttu-id="d297a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d297a-127">-WorkspaceName</span></span>
<span data-ttu-id="d297a-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d297a-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d297a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d297a-129">CommonParameters</span></span>
<span data-ttu-id="d297a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d297a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d297a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d297a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d297a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d297a-132">INPUTS</span></span>

### <span data-ttu-id="d297a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d297a-133">System.String</span></span>
## <span data-ttu-id="d297a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d297a-134">OUTPUTS</span></span>

### <span data-ttu-id="d297a-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="d297a-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="d297a-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d297a-136">NOTES</span></span>

## <span data-ttu-id="d297a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d297a-137">RELATED LINKS</span></span>
