---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 61846456cfbff2dcbdaffba8c73a9bada87f07dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550852"
---
# <span data-ttu-id="0ad32-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0ad32-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="0ad32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ad32-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad32-103">Pobierz źródła danych w obszarze roboczym Analiza dzienników Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad32-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ad32-104">SYNTAX</span></span>

### <span data-ttu-id="0ad32-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ad32-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad32-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="0ad32-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad32-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="0ad32-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad32-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="0ad32-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad32-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="0ad32-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad32-110">Opis</span><span class="sxs-lookup"><span data-stu-id="0ad32-110">DESCRIPTION</span></span>
<span data-ttu-id="0ad32-111">Polecenie cmdlet **Get-AzureRmOperationalInsightsDataSource** pobiera źródła danych.</span><span class="sxs-lookup"><span data-stu-id="0ad32-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="0ad32-112">Możesz określić źródło danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="0ad32-112">You can specify a data source to get.</span></span>
<span data-ttu-id="0ad32-113">Wyniki można filtrować na podstawie rodzaju źródła danych.</span><span class="sxs-lookup"><span data-stu-id="0ad32-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="0ad32-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ad32-114">EXAMPLES</span></span>

## <span data-ttu-id="0ad32-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ad32-115">PARAMETERS</span></span>

### <span data-ttu-id="0ad32-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="0ad32-116">-Kind</span></span>
<span data-ttu-id="0ad32-117">Określa rodzaj źródeł danych, które należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="0ad32-117">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="0ad32-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0ad32-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ad32-119">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="0ad32-119">AzureActivityLog</span></span> 
- <span data-ttu-id="0ad32-120">CustomLog</span><span class="sxs-lookup"><span data-stu-id="0ad32-120">CustomLog</span></span> 
- <span data-ttu-id="0ad32-121">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="0ad32-121">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="0ad32-122">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="0ad32-122">LinuxSyslog</span></span> 
- <span data-ttu-id="0ad32-123">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="0ad32-123">WindowsEvent</span></span> 
- <span data-ttu-id="0ad32-124">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="0ad32-124">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

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
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad32-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ad32-125">-Name</span></span>
<span data-ttu-id="0ad32-126">Określa nazwę źródła danych, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="0ad32-126">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="0ad32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad32-127">-ResourceGroupName</span></span>
<span data-ttu-id="0ad32-128">Określa nazwę grupy zasobów zawierającej źródła danych do pobrania.</span><span class="sxs-lookup"><span data-stu-id="0ad32-128">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="0ad32-129">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="0ad32-129">-Workspace</span></span>
<span data-ttu-id="0ad32-130">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad32-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0ad32-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="0ad32-131">-WorkspaceName</span></span>
<span data-ttu-id="0ad32-132">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad32-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0ad32-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad32-133">-DefaultProfile</span></span>
<span data-ttu-id="0ad32-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad32-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad32-135">CommonParameters</span></span>
<span data-ttu-id="0ad32-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad32-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad32-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad32-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ad32-138">INPUTS</span></span>

### <span data-ttu-id="0ad32-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ad32-139">PSWorkspace</span></span>
<span data-ttu-id="0ad32-140">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="0ad32-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="0ad32-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ad32-141">PSWorkspace</span></span>
<span data-ttu-id="0ad32-142">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="0ad32-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0ad32-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ad32-143">OUTPUTS</span></span>

### <span data-ttu-id="0ad32-144">System. Collections. Generic. list "1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="0ad32-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="0ad32-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0ad32-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0ad32-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ad32-146">NOTES</span></span>
* <span data-ttu-id="0ad32-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="0ad32-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0ad32-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ad32-148">RELATED LINKS</span></span>

[<span data-ttu-id="0ad32-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0ad32-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="0ad32-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0ad32-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


