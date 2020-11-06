---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5d13fb4c432a0b40fdfd90a5eea55ea44a8b6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541631"
---
# <span data-ttu-id="6cae4-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6cae4-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="6cae4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cae4-102">SYNOPSIS</span></span>
<span data-ttu-id="6cae4-103">Pobierz źródła danych w obszarze roboczym Analiza dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="6cae4-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cae4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cae4-104">SYNTAX</span></span>

### <span data-ttu-id="6cae4-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6cae4-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cae4-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="6cae4-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cae4-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="6cae4-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cae4-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="6cae4-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cae4-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="6cae4-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cae4-110">Opis</span><span class="sxs-lookup"><span data-stu-id="6cae4-110">DESCRIPTION</span></span>
<span data-ttu-id="6cae4-111">Polecenie cmdlet **Get-AzureRmOperationalInsightsDataSource** pobiera źródła danych.</span><span class="sxs-lookup"><span data-stu-id="6cae4-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="6cae4-112">Możesz określić źródło danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6cae4-112">You can specify a data source to get.</span></span>
<span data-ttu-id="6cae4-113">Wyniki można filtrować na podstawie rodzaju źródła danych.</span><span class="sxs-lookup"><span data-stu-id="6cae4-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="6cae4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cae4-114">EXAMPLES</span></span>

## <span data-ttu-id="6cae4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cae4-115">PARAMETERS</span></span>

### <span data-ttu-id="6cae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cae4-116">-DefaultProfile</span></span>
<span data-ttu-id="6cae4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6cae4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cae4-118">-Kind</span><span class="sxs-lookup"><span data-stu-id="6cae4-118">-Kind</span></span>
<span data-ttu-id="6cae4-119">Określa rodzaj źródeł danych, które należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="6cae4-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="6cae4-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6cae4-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6cae4-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="6cae4-121">AzureActivityLog</span></span> 
- <span data-ttu-id="6cae4-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="6cae4-122">CustomLog</span></span> 
- <span data-ttu-id="6cae4-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="6cae4-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="6cae4-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="6cae4-124">LinuxSyslog</span></span> 
- <span data-ttu-id="6cae4-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="6cae4-125">WindowsEvent</span></span> 
- <span data-ttu-id="6cae4-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="6cae4-126">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cae4-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6cae4-127">-Name</span></span>
<span data-ttu-id="6cae4-128">Określa nazwę źródła danych, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="6cae4-128">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="6cae4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cae4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6cae4-130">Określa nazwę grupy zasobów zawierającej źródła danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6cae4-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cae4-131">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="6cae4-131">-Workspace</span></span>
<span data-ttu-id="6cae4-132">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cae4-132">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6cae4-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6cae4-133">-WorkspaceName</span></span>
<span data-ttu-id="6cae4-134">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cae4-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cae4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cae4-135">CommonParameters</span></span>
<span data-ttu-id="6cae4-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cae4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cae4-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cae4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cae4-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cae4-138">INPUTS</span></span>

### <span data-ttu-id="6cae4-139">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6cae4-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="6cae4-140">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6cae4-140">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="6cae4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6cae4-141">System.String</span></span>

## <span data-ttu-id="6cae4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cae4-142">OUTPUTS</span></span>

### <span data-ttu-id="6cae4-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6cae4-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6cae4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cae4-144">NOTES</span></span>
* <span data-ttu-id="6cae4-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="6cae4-145">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6cae4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cae4-146">RELATED LINKS</span></span>

[<span data-ttu-id="6cae4-147">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6cae4-147">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="6cae4-148">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6cae4-148">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


