---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: f291eedade1a1a243f22dc618ffcc538a9158de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708828"
---
# <span data-ttu-id="7138a-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7138a-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="7138a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7138a-102">SYNOPSIS</span></span>
<span data-ttu-id="7138a-103">Pobierz źródła danych w obszarze roboczym Analiza dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="7138a-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="7138a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7138a-104">SYNTAX</span></span>

### <span data-ttu-id="7138a-105">ByWorkspaceNameByKind (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7138a-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7138a-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="7138a-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7138a-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="7138a-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7138a-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="7138a-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7138a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7138a-109">DESCRIPTION</span></span>
<span data-ttu-id="7138a-110">Polecenie cmdlet **Get-AzOperationalInsightsDataSource** pobiera źródła danych.</span><span class="sxs-lookup"><span data-stu-id="7138a-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="7138a-111">Możesz określić źródło danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7138a-111">You can specify a data source to get.</span></span>
<span data-ttu-id="7138a-112">Wyniki można filtrować na podstawie rodzaju źródła danych.</span><span class="sxs-lookup"><span data-stu-id="7138a-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="7138a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7138a-113">EXAMPLES</span></span>

## <span data-ttu-id="7138a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7138a-114">PARAMETERS</span></span>

### <span data-ttu-id="7138a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7138a-115">-DefaultProfile</span></span>
<span data-ttu-id="7138a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7138a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7138a-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="7138a-117">-Kind</span></span>
<span data-ttu-id="7138a-118">Określa rodzaj źródeł danych, które należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="7138a-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="7138a-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7138a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7138a-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="7138a-120">AzureActivityLog</span></span> 
- <span data-ttu-id="7138a-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="7138a-121">CustomLog</span></span> 
- <span data-ttu-id="7138a-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="7138a-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="7138a-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="7138a-123">LinuxSyslog</span></span> 
- <span data-ttu-id="7138a-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="7138a-124">WindowsEvent</span></span> 
- <span data-ttu-id="7138a-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="7138a-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="7138a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7138a-126">-Name</span></span>
<span data-ttu-id="7138a-127">Określa nazwę źródła danych, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="7138a-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="7138a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7138a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7138a-129">Określa nazwę grupy zasobów zawierającej źródła danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7138a-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="7138a-130">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="7138a-130">-Workspace</span></span>
<span data-ttu-id="7138a-131">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7138a-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7138a-132">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7138a-132">-WorkspaceName</span></span>
<span data-ttu-id="7138a-133">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7138a-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7138a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7138a-134">CommonParameters</span></span>
<span data-ttu-id="7138a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7138a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7138a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7138a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7138a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7138a-137">INPUTS</span></span>

### <span data-ttu-id="7138a-138">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7138a-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7138a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7138a-139">System.String</span></span>

## <span data-ttu-id="7138a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7138a-140">OUTPUTS</span></span>

### <span data-ttu-id="7138a-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7138a-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7138a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7138a-142">NOTES</span></span>
* <span data-ttu-id="7138a-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="7138a-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7138a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7138a-144">RELATED LINKS</span></span>

[<span data-ttu-id="7138a-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7138a-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="7138a-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7138a-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)

