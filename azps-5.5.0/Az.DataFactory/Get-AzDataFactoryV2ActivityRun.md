---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200595"
---
# <span data-ttu-id="b5cdc-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="b5cdc-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="b5cdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="b5cdc-103">Pobiera informacje o działaniach uruchamianych dla uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="b5cdc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5cdc-104">SYNTAX</span></span>

### <span data-ttu-id="b5cdc-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="b5cdc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5cdc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b5cdc-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5cdc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="b5cdc-108">Polecenie **cmdlet Get-AzDataFactoryV2ActivityRun** pobiera informacje o uruchamianiu w usłudze Azure Data Factory określonego uruchomienia potoku, które miało miejsce w określonym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="b5cdc-109">Ponadto można określić filtry dla nazwy działania, połączonej nazwy usługi, która wykonywała uruchamianie, oraz stanu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="b5cdc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5cdc-110">EXAMPLES</span></span>

### <span data-ttu-id="b5cdc-111">Przykład 1. Uruchamianie wszystkich działań w przypadku uruchomienia potoku</span><span class="sxs-lookup"><span data-stu-id="b5cdc-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="b5cdc-112">To polecenie pobiera szczegółowe informacje o wszystkich działaniach uruchamianych w potoku o identyfikatorze "f288712d-fb08-4cb8-96ef-82d3b9b30621", który wydarzył się między "2017-09-01" a "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="b5cdc-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="b5cdc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5cdc-113">PARAMETERS</span></span>

### <span data-ttu-id="b5cdc-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="b5cdc-114">-ActivityName</span></span>
<span data-ttu-id="b5cdc-115">Nazwa działania.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-115">The name of the activity.</span></span>

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

### <span data-ttu-id="b5cdc-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b5cdc-116">-DataFactory</span></span>
<span data-ttu-id="b5cdc-117">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-117">The data factory object.</span></span>

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

### <span data-ttu-id="b5cdc-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b5cdc-118">-DataFactoryName</span></span>
<span data-ttu-id="b5cdc-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-119">The data factory name.</span></span>

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

### <span data-ttu-id="b5cdc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5cdc-120">-DefaultProfile</span></span>
<span data-ttu-id="b5cdc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5cdc-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="b5cdc-122">-PipelineRunId</span></span>
<span data-ttu-id="b5cdc-123">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="b5cdc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5cdc-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5cdc-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-125">The resource group name.</span></span>

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

### <span data-ttu-id="b5cdc-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="b5cdc-126">-RunStartedAfter</span></span>
<span data-ttu-id="b5cdc-127">Godzina rozpoczęcia lub po uruchomieniu potoku.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="b5cdc-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="b5cdc-128">-RunStartedBefore</span></span>
<span data-ttu-id="b5cdc-129">Godzina rozpoczęcia lub czasu rozpoczęcia uruchamiania potoku.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="b5cdc-130">— Status</span><span class="sxs-lookup"><span data-stu-id="b5cdc-130">-Status</span></span>
<span data-ttu-id="b5cdc-131">Stan uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="b5cdc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5cdc-132">CommonParameters</span></span>
<span data-ttu-id="b5cdc-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5cdc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5cdc-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5cdc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5cdc-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5cdc-135">INPUTS</span></span>

### <span data-ttu-id="b5cdc-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5cdc-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="b5cdc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b5cdc-137">System.String</span></span>

## <span data-ttu-id="b5cdc-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5cdc-138">OUTPUTS</span></span>

### <span data-ttu-id="b5cdc-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="b5cdc-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="b5cdc-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5cdc-140">NOTES</span></span>

## <span data-ttu-id="b5cdc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5cdc-141">RELATED LINKS</span></span>

[<span data-ttu-id="b5cdc-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b5cdc-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b5cdc-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="b5cdc-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

