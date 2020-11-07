---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: 5f6c56fac892e2c3e9c1546dac226c5d81ddb99e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710125"
---
# <span data-ttu-id="da582-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="da582-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="da582-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da582-102">SYNOPSIS</span></span>
<span data-ttu-id="da582-103">Pobiera informacje o działaniach dotyczących uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="da582-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="da582-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da582-104">SYNTAX</span></span>

### <span data-ttu-id="da582-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da582-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da582-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="da582-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da582-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da582-107">DESCRIPTION</span></span>
<span data-ttu-id="da582-108">Polecenie cmdlet **Get-AzDataFactoryV2ActivityRun** pobiera informacje dotyczące uruchamiania usługi Azure Data Factory dla określonego przebiegu procesu, który wystąpił w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="da582-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="da582-109">Ponadto możesz określić filtry dla nazwy działania, połączonej nazwy usługi, która wykonała uruchomienie, oraz stanu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="da582-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="da582-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da582-110">EXAMPLES</span></span>

### <span data-ttu-id="da582-111">Przykład 1: Pobierz wszystkie działania dla potoku</span><span class="sxs-lookup"><span data-stu-id="da582-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="da582-112">To polecenie pobiera szczegóły dotyczące wszystkich działań uruchomionych w potoku o IDENTYFIKATORze "f288712d-FB08-4cb8-96ef-82d3b9b30621", który wystąpił w zakresie od "2017-09-01" do "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="da582-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="da582-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da582-113">PARAMETERS</span></span>

### <span data-ttu-id="da582-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="da582-114">-ActivityName</span></span>
<span data-ttu-id="da582-115">Nazwa działania.</span><span class="sxs-lookup"><span data-stu-id="da582-115">The name of the activity.</span></span>

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

### <span data-ttu-id="da582-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="da582-116">-DataFactory</span></span>
<span data-ttu-id="da582-117">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="da582-117">The data factory object.</span></span>

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

### <span data-ttu-id="da582-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="da582-118">-DataFactoryName</span></span>
<span data-ttu-id="da582-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="da582-119">The data factory name.</span></span>

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

### <span data-ttu-id="da582-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da582-120">-DefaultProfile</span></span>
<span data-ttu-id="da582-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da582-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da582-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="da582-122">-PipelineRunId</span></span>
<span data-ttu-id="da582-123">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="da582-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="da582-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da582-124">-ResourceGroupName</span></span>
<span data-ttu-id="da582-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da582-125">The resource group name.</span></span>

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

### <span data-ttu-id="da582-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="da582-126">-RunStartedAfter</span></span>
<span data-ttu-id="da582-127">Czas rozpoczęcia lub późniejszego uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="da582-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="da582-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="da582-128">-RunStartedBefore</span></span>
<span data-ttu-id="da582-129">Czas, w którym rozpoczęto uruchamianie rurociągu lub przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="da582-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="da582-130">-Status</span><span class="sxs-lookup"><span data-stu-id="da582-130">-Status</span></span>
<span data-ttu-id="da582-131">Stan uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="da582-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="da582-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da582-132">CommonParameters</span></span>
<span data-ttu-id="da582-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da582-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da582-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da582-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da582-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da582-135">INPUTS</span></span>

### <span data-ttu-id="da582-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="da582-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="da582-137">System. String</span><span class="sxs-lookup"><span data-stu-id="da582-137">System.String</span></span>

## <span data-ttu-id="da582-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da582-138">OUTPUTS</span></span>

### <span data-ttu-id="da582-139">Microsoft. Azure. Commands. DataFactoryV2. models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="da582-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="da582-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da582-140">NOTES</span></span>

## <span data-ttu-id="da582-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da582-141">RELATED LINKS</span></span>

[<span data-ttu-id="da582-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="da582-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="da582-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="da582-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

