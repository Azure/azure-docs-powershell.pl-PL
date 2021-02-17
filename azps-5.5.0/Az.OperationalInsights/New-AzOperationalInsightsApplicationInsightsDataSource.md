---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240419"
---
# <span data-ttu-id="0f206-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0f206-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="0f206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f206-102">SYNOPSIS</span></span>
<span data-ttu-id="0f206-103">Zbieraj dzienniki z danej Application-Insights aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="0f206-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f206-104">SYNTAX</span></span>

### <span data-ttu-id="0f206-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0f206-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f206-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="0f206-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f206-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="0f206-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f206-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="0f206-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f206-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="0f206-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f206-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f206-110">DESCRIPTION</span></span>
<span data-ttu-id="0f206-111">Polecenie cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** umożliwia zbieranie dzienników z danej Application-Insights aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="0f206-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f206-112">EXAMPLES</span></span>

### <span data-ttu-id="0f206-113">Przykład 1. Tworzenie źródła danych szczegółowych informacji dotyczących aplikacji w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="0f206-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="0f206-114">To polecenie tworzy źródło danych analizy aplikacji danej aplikacji w danym obszarze roboczym analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="0f206-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="0f206-115">Dzięki temu zbieranie dzienników z danej aplikacji do obszaru roboczego analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="0f206-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="0f206-116">Przykład 2. Uzyskiwanie obiektu obszaru roboczego i tworzenie źródła danych szczegółowych informacji aplikacji przy zastosowaniu identyfikatora zasobu aplikacji</span><span class="sxs-lookup"><span data-stu-id="0f206-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="0f206-117">To polecenie przedstawia uzyskiwanie obiektu obszaru roboczego analizy dziennika, a następnie przekazywanie danych wyjściowych w celu utworzenia skojarzonego źródła danych szczegółowych informacji aplikacji przy zastosowaniu identyfikatora zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="0f206-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f206-118">PARAMETERS</span></span>

### <span data-ttu-id="0f206-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0f206-119">-ApplicationName</span></span>
<span data-ttu-id="0f206-120">Nazwa połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f206-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="0f206-122">Nazwa grupy zasobów połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="0f206-123">-ApplicationResourceId</span></span>
<span data-ttu-id="0f206-124">Identyfikator połączonego zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f206-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="0f206-126">Identyfikator subskrypcji połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0f206-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f206-127">-DefaultProfile</span></span>
<span data-ttu-id="0f206-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f206-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f206-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0f206-129">-Force</span></span>
<span data-ttu-id="0f206-130">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f206-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0f206-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f206-131">-ResourceGroupName</span></span>
<span data-ttu-id="0f206-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f206-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-133">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="0f206-133">-Workspace</span></span>
<span data-ttu-id="0f206-134">Obszar roboczy, który będzie zawierał źródło danych.</span><span class="sxs-lookup"><span data-stu-id="0f206-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f206-135">-WorkspaceName</span></span>
<span data-ttu-id="0f206-136">Nazwa obszaru roboczego zawierającego źródło danych.</span><span class="sxs-lookup"><span data-stu-id="0f206-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f206-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f206-137">-Confirm</span></span>
<span data-ttu-id="0f206-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f206-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f206-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f206-139">-WhatIf</span></span>
<span data-ttu-id="0f206-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f206-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f206-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f206-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f206-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f206-142">CommonParameters</span></span>
<span data-ttu-id="0f206-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f206-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f206-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f206-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f206-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f206-145">INPUTS</span></span>

### <span data-ttu-id="0f206-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f206-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0f206-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0f206-147">System.String</span></span>

## <span data-ttu-id="0f206-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f206-148">OUTPUTS</span></span>

### <span data-ttu-id="0f206-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0f206-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0f206-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f206-150">NOTES</span></span>

## <span data-ttu-id="0f206-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f206-151">RELATED LINKS</span></span>
