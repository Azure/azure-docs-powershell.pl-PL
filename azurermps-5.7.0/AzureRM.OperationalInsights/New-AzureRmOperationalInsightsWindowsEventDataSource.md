---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: cebbcb0526c35fb803de783604db291612694baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542439"
---
# <span data-ttu-id="ff1bc-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ff1bc-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ff1bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1bc-103">Zbiera dzienniki zdarzeń na komputerach z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff1bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff1bc-104">SYNTAX</span></span>

### <span data-ttu-id="ff1bc-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff1bc-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff1bc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff1bc-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff1bc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff1bc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff1bc-108">Polecenie cmdlet **New-AzureRmOperationalInsightsWindowsEventDataSource** umożliwia dodanie źródła danych zbierającego dzienniki zdarzeń systemu Windows z połączonych komputerów, na których jest uruchomiony system operacyjny Windows w usłudze Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ff1bc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff1bc-109">EXAMPLES</span></span>

## <span data-ttu-id="ff1bc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff1bc-110">PARAMETERS</span></span>

### <span data-ttu-id="ff1bc-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ff1bc-111">-CollectErrors</span></span>
<span data-ttu-id="ff1bc-112">Wskazuje, że usługa Insights gromadzi komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-112">Indicates that Operational Insights collects error messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ff1bc-113">-CollectInformation</span></span>
<span data-ttu-id="ff1bc-114">Wskazuje, że komunikaty informacyjne są zbierane.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-114">Indicates that Operational Insights collects information messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ff1bc-115">-CollectWarnings</span></span>
<span data-ttu-id="ff1bc-116">Wskazuje, że usługa Insights gromadzi komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-116">Indicates that Operational Insights collects warning messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1bc-117">-DefaultProfile</span></span>
<span data-ttu-id="ff1bc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ff1bc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-119">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="ff1bc-119">-EventLogName</span></span>
<span data-ttu-id="ff1bc-120">Określa nazwę dziennika zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-120">Specifies the name of the event log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ff1bc-121">-Force</span></span>
<span data-ttu-id="ff1bc-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff1bc-123">-Name</span></span>
<span data-ttu-id="ff1bc-124">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-124">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff1bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff1bc-126">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-127">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="ff1bc-127">-Workspace</span></span>
<span data-ttu-id="ff1bc-128">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="ff1bc-129">-WorkspaceName</span></span>
<span data-ttu-id="ff1bc-130">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff1bc-131">-Confirm</span></span>
<span data-ttu-id="ff1bc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff1bc-133">-WhatIf</span></span>
<span data-ttu-id="ff1bc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff1bc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1bc-136">CommonParameters</span></span>
<span data-ttu-id="ff1bc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1bc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1bc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1bc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff1bc-139">INPUTS</span></span>

### <span data-ttu-id="ff1bc-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff1bc-140">PSWorkspace</span></span>
<span data-ttu-id="ff1bc-141">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="ff1bc-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="ff1bc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff1bc-142">OUTPUTS</span></span>

### <span data-ttu-id="ff1bc-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ff1bc-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ff1bc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff1bc-144">NOTES</span></span>

## <span data-ttu-id="ff1bc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff1bc-145">RELATED LINKS</span></span>

