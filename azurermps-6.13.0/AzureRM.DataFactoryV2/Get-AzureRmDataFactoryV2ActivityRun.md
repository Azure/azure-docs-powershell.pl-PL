---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 4bfebac1d37dbdc0cac2bc8262993a6c81b0c9ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545427"
---
# <span data-ttu-id="e51a4-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e51a4-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="e51a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e51a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e51a4-103">Pobiera informacje o działaniach dotyczących uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e51a4-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e51a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e51a4-104">SYNTAX</span></span>

### <span data-ttu-id="e51a4-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e51a4-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e51a4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e51a4-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e51a4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e51a4-107">DESCRIPTION</span></span>
<span data-ttu-id="e51a4-108">Polecenie cmdlet **Get-AzureRmDataFactoryV2ActivityRun** pobiera informacje dotyczące uruchamiania usługi Azure Data Factory dla określonego przebiegu procesu, który wystąpił w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="e51a4-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="e51a4-109">Ponadto możesz określić filtry dla nazwy działania, połączonej nazwy usługi, która wykonała uruchomienie, oraz stanu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e51a4-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="e51a4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e51a4-110">EXAMPLES</span></span>

### <span data-ttu-id="e51a4-111">Przykład 1: Pobierz wszystkie działania dla potoku</span><span class="sxs-lookup"><span data-stu-id="e51a4-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="e51a4-112">To polecenie pobiera szczegóły dotyczące wszystkich działań uruchomionych w potoku o IDENTYFIKATORze "f288712d-FB08-4cb8-96ef-82d3b9b30621", który wystąpił w zakresie od "2017-09-01" do "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="e51a4-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="e51a4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e51a4-113">PARAMETERS</span></span>

### <span data-ttu-id="e51a4-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="e51a4-114">-ActivityName</span></span>
<span data-ttu-id="e51a4-115">Nazwa działania.</span><span class="sxs-lookup"><span data-stu-id="e51a4-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51a4-116">-DataFactory</span></span>
<span data-ttu-id="e51a4-117">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e51a4-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e51a4-118">-DataFactoryName</span></span>
<span data-ttu-id="e51a4-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e51a4-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51a4-120">-DefaultProfile</span></span>
<span data-ttu-id="e51a4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e51a4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e51a4-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="e51a4-122">-LinkedServiceName</span></span>
<span data-ttu-id="e51a4-123">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="e51a4-123">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e51a4-124">-PipelineRunId</span></span>
<span data-ttu-id="e51a4-125">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e51a4-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="e51a4-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e51a4-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e51a4-128">-RunStartedAfter</span></span>
<span data-ttu-id="e51a4-129">Czas rozpoczęcia lub późniejszego uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e51a4-129">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e51a4-130">-RunStartedBefore</span></span>
<span data-ttu-id="e51a4-131">Czas, w którym rozpoczęto uruchamianie rurociągu lub przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="e51a4-131">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-132">-Status</span><span class="sxs-lookup"><span data-stu-id="e51a4-132">-Status</span></span>
<span data-ttu-id="e51a4-133">Stan uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e51a4-133">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51a4-134">CommonParameters</span></span>
<span data-ttu-id="e51a4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e51a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51a4-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e51a4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51a4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e51a4-137">INPUTS</span></span>

### <span data-ttu-id="e51a4-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e51a4-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="e51a4-139">Parametry: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e51a4-139">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="e51a4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e51a4-140">System.String</span></span>

## <span data-ttu-id="e51a4-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e51a4-141">OUTPUTS</span></span>

### <span data-ttu-id="e51a4-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="e51a4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="e51a4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e51a4-143">NOTES</span></span>

## <span data-ttu-id="e51a4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e51a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="e51a4-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e51a4-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e51a4-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e51a4-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

