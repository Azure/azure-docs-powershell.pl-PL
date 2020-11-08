---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232708"
---
# <span data-ttu-id="16b72-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="16b72-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="16b72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16b72-102">SYNOPSIS</span></span>
<span data-ttu-id="16b72-103">Zbierz dzienniki z podanej Application-Insights aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16b72-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="16b72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16b72-104">SYNTAX</span></span>

### <span data-ttu-id="16b72-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16b72-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b72-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="16b72-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b72-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="16b72-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16b72-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="16b72-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b72-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="16b72-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16b72-110">Opis</span><span class="sxs-lookup"><span data-stu-id="16b72-110">DESCRIPTION</span></span>
<span data-ttu-id="16b72-111">Polecenie cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** umożliwia zbieranie dzienników z danej aplikacji Application-Insights.</span><span class="sxs-lookup"><span data-stu-id="16b72-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="16b72-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16b72-112">EXAMPLES</span></span>

### <span data-ttu-id="16b72-113">Przykład 1: tworzenie źródła danych w usłudze Application-Insights w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="16b72-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="16b72-114">To polecenie tworzy źródło danych usługi Application-Insights dla danej aplikacji w danym obszarze roboczym analizy dzienników.</span><span class="sxs-lookup"><span data-stu-id="16b72-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="16b72-115">Spowoduje to włączenie zbierania dzienników z danej aplikacji do obszaru roboczego Analiza dzienników.</span><span class="sxs-lookup"><span data-stu-id="16b72-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="16b72-116">Przykład 2: Pobieranie obiektu obszaru roboczego i tworzenie źródła danych w usłudze Application-Insights według identyfikatora zasobu aplikacji</span><span class="sxs-lookup"><span data-stu-id="16b72-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="16b72-117">To polecenie ilustruje obiekt obszar roboczy Analiza dzienników, a następnie przekazanie danych wyjściowych w celu utworzenia skojarzonego źródła danych usługi Application-Insights przez identyfikator zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16b72-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="16b72-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16b72-118">PARAMETERS</span></span>

### <span data-ttu-id="16b72-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="16b72-119">-ApplicationName</span></span>
<span data-ttu-id="16b72-120">Nazwa połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16b72-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="16b72-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b72-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="16b72-122">Nazwa grupy zasobów połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16b72-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="16b72-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="16b72-123">-ApplicationResourceId</span></span>
<span data-ttu-id="16b72-124">Identyfikator zasobu połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16b72-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="16b72-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16b72-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="16b72-126">Identyfikator subskrypcji połączonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16b72-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="16b72-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b72-127">-DefaultProfile</span></span>
<span data-ttu-id="16b72-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16b72-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b72-129">-Force</span><span class="sxs-lookup"><span data-stu-id="16b72-129">-Force</span></span>
<span data-ttu-id="16b72-130">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16b72-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="16b72-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b72-131">-ResourceGroupName</span></span>
<span data-ttu-id="16b72-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16b72-132">The resource group name.</span></span>

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

### <span data-ttu-id="16b72-133">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="16b72-133">-Workspace</span></span>
<span data-ttu-id="16b72-134">Obszar roboczy, który będzie zawierać źródło danych.</span><span class="sxs-lookup"><span data-stu-id="16b72-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="16b72-135">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="16b72-135">-WorkspaceName</span></span>
<span data-ttu-id="16b72-136">Nazwa obszaru roboczego, który będzie zawierać źródło danych.</span><span class="sxs-lookup"><span data-stu-id="16b72-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="16b72-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16b72-137">-Confirm</span></span>
<span data-ttu-id="16b72-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16b72-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b72-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b72-139">-WhatIf</span></span>
<span data-ttu-id="16b72-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16b72-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b72-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16b72-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b72-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b72-142">CommonParameters</span></span>
<span data-ttu-id="16b72-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b72-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b72-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16b72-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b72-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16b72-145">INPUTS</span></span>

### <span data-ttu-id="16b72-146">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="16b72-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="16b72-147">System. String</span><span class="sxs-lookup"><span data-stu-id="16b72-147">System.String</span></span>

## <span data-ttu-id="16b72-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16b72-148">OUTPUTS</span></span>

### <span data-ttu-id="16b72-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="16b72-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="16b72-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16b72-150">NOTES</span></span>

## <span data-ttu-id="16b72-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16b72-151">RELATED LINKS</span></span>
