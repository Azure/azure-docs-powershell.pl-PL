---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5f3200459cbcca9806a1a7185798889b3457760d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547388"
---
# <span data-ttu-id="249ff-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="249ff-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="249ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="249ff-102">SYNOPSIS</span></span>
<span data-ttu-id="249ff-103">Zbiera dzienniki zdarzeń na komputerach z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="249ff-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="249ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="249ff-104">SYNTAX</span></span>

### <span data-ttu-id="249ff-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="249ff-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="249ff-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="249ff-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="249ff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="249ff-107">DESCRIPTION</span></span>
<span data-ttu-id="249ff-108">Polecenie cmdlet **New-AzureRmOperationalInsightsWindowsEventDataSource** umożliwia dodanie źródła danych zbierającego dzienniki zdarzeń systemu Windows z połączonych komputerów, na których jest uruchomiony system operacyjny Windows w usłudze Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="249ff-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="249ff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="249ff-109">EXAMPLES</span></span>

## <span data-ttu-id="249ff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="249ff-110">PARAMETERS</span></span>

### <span data-ttu-id="249ff-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="249ff-111">-CollectErrors</span></span>
<span data-ttu-id="249ff-112">Wskazuje, że usługa Insights gromadzi komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="249ff-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="249ff-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="249ff-113">-CollectInformation</span></span>
<span data-ttu-id="249ff-114">Wskazuje, że komunikaty informacyjne są zbierane.</span><span class="sxs-lookup"><span data-stu-id="249ff-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="249ff-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="249ff-115">-CollectWarnings</span></span>
<span data-ttu-id="249ff-116">Wskazuje, że usługa Insights gromadzi komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="249ff-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="249ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249ff-117">-DefaultProfile</span></span>
<span data-ttu-id="249ff-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="249ff-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="249ff-119">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="249ff-119">-EventLogName</span></span>
<span data-ttu-id="249ff-120">Określa nazwę dziennika zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="249ff-120">Specifies the name of the event log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="249ff-121">-Force</span></span>
<span data-ttu-id="249ff-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="249ff-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="249ff-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="249ff-123">-Name</span></span>
<span data-ttu-id="249ff-124">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="249ff-124">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="249ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="249ff-126">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="249ff-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-127">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="249ff-127">-Workspace</span></span>
<span data-ttu-id="249ff-128">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249ff-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="249ff-129">-WorkspaceName</span></span>
<span data-ttu-id="249ff-130">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249ff-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="249ff-131">-Confirm</span></span>
<span data-ttu-id="249ff-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="249ff-133">-WhatIf</span></span>
<span data-ttu-id="249ff-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249ff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="249ff-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="249ff-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="249ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249ff-136">CommonParameters</span></span>
<span data-ttu-id="249ff-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="249ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249ff-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="249ff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249ff-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="249ff-139">INPUTS</span></span>

### <span data-ttu-id="249ff-140">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="249ff-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="249ff-141">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="249ff-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="249ff-142">System. String</span><span class="sxs-lookup"><span data-stu-id="249ff-142">System.String</span></span>

## <span data-ttu-id="249ff-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="249ff-143">OUTPUTS</span></span>

### <span data-ttu-id="249ff-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="249ff-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="249ff-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="249ff-145">NOTES</span></span>

## <span data-ttu-id="249ff-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="249ff-146">RELATED LINKS</span></span>
