---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: c3ca23ae1cbe29c7c2867ec9ac48bea612dd4fc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976506"
---
# <span data-ttu-id="a19c5-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a19c5-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a19c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a19c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a19c5-103">Uzyskiwanie źródeł danych w obszarze roboczym usługi Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="a19c5-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="a19c5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a19c5-104">SYNTAX</span></span>

### <span data-ttu-id="a19c5-105">ByWorkspaceNameByKind (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a19c5-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a19c5-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="a19c5-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a19c5-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="a19c5-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a19c5-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="a19c5-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a19c5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a19c5-109">DESCRIPTION</span></span>
<span data-ttu-id="a19c5-110">Polecenie **cmdlet Get-AzOperationalInsightsDataSource** pobiera źródła danych.</span><span class="sxs-lookup"><span data-stu-id="a19c5-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="a19c5-111">Możesz określić źródło danych do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a19c5-111">You can specify a data source to get.</span></span>
<span data-ttu-id="a19c5-112">Wyniki można filtrować według rodzaju źródła danych.</span><span class="sxs-lookup"><span data-stu-id="a19c5-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="a19c5-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a19c5-113">EXAMPLES</span></span>

## <span data-ttu-id="a19c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a19c5-114">PARAMETERS</span></span>

### <span data-ttu-id="a19c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19c5-115">-DefaultProfile</span></span>
<span data-ttu-id="a19c5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a19c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a19c5-117">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="a19c5-117">-Kind</span></span>
<span data-ttu-id="a19c5-118">Określa rodzaj źródeł danych do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a19c5-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="a19c5-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a19c5-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a19c5-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="a19c5-120">AzureActivityLog</span></span> 
- <span data-ttu-id="a19c5-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="a19c5-121">CustomLog</span></span> 
- <span data-ttu-id="a19c5-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="a19c5-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="a19c5-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="a19c5-123">LinuxSyslog</span></span> 
- <span data-ttu-id="a19c5-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="a19c5-124">WindowsEvent</span></span> 
- <span data-ttu-id="a19c5-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="a19c5-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19c5-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a19c5-126">-Name</span></span>
<span data-ttu-id="a19c5-127">Określa nazwę źródła danych do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a19c5-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="a19c5-129">Określa nazwę grupy zasobów zawierającej źródła danych do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a19c5-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19c5-130">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="a19c5-130">-Workspace</span></span>
<span data-ttu-id="a19c5-131">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19c5-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a19c5-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a19c5-132">-WorkspaceName</span></span>
<span data-ttu-id="a19c5-133">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19c5-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19c5-134">CommonParameters</span></span>
<span data-ttu-id="a19c5-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19c5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19c5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19c5-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a19c5-137">INPUTS</span></span>

### <span data-ttu-id="a19c5-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a19c5-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a19c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a19c5-139">System.String</span></span>

## <span data-ttu-id="a19c5-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a19c5-140">OUTPUTS</span></span>

### <span data-ttu-id="a19c5-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a19c5-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a19c5-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a19c5-142">NOTES</span></span>
* <span data-ttu-id="a19c5-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="a19c5-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a19c5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a19c5-144">RELATED LINKS</span></span>

[<span data-ttu-id="a19c5-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a19c5-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="a19c5-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a19c5-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


