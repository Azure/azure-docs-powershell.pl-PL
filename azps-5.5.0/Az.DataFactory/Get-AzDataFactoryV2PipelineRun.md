---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198866"
---
# <span data-ttu-id="78e9c-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="78e9c-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="78e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="78e9c-103">Pobiera informacje o uruchamianych potokach.</span><span class="sxs-lookup"><span data-stu-id="78e9c-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="78e9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78e9c-104">SYNTAX</span></span>

### <span data-ttu-id="78e9c-105">ByFactoryNameByRunId (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="78e9c-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78e9c-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="78e9c-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78e9c-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="78e9c-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78e9c-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="78e9c-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78e9c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="78e9c-109">DESCRIPTION</span></span>
<span data-ttu-id="78e9c-110">Polecenie **Get-AzDataFactoryV2PipelineRun zwraca** informacje o uruchomieniach dla określonego potoku.</span><span class="sxs-lookup"><span data-stu-id="78e9c-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="78e9c-111">Jeśli określono wartość PipelineRunId, są w nim podane szczegóły dotyczące uruchomienia z tym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="78e9c-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="78e9c-112">Jeśli wartość PipelineRunId nie jest określona, wyświetla informacje o wszystkich uruchomieniach dla potoków, które się wydarzyły między wartościami LastUpdatedAfter i LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="78e9c-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="78e9c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78e9c-113">EXAMPLES</span></span>

### <span data-ttu-id="78e9c-114">Przykład 1. Uzyskiwanie informacji dotyczących uruchomienia potoku</span><span class="sxs-lookup"><span data-stu-id="78e9c-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

<span data-ttu-id="78e9c-115">To polecenie pobiera szczegółowe informacje o uruchomieniu potoku o identyfikatorze "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="78e9c-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="78e9c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78e9c-116">PARAMETERS</span></span>

### <span data-ttu-id="78e9c-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="78e9c-117">-DataFactory</span></span>
<span data-ttu-id="78e9c-118">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="78e9c-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78e9c-119">-DataFactoryName</span></span>
<span data-ttu-id="78e9c-120">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="78e9c-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e9c-121">-DefaultProfile</span></span>
<span data-ttu-id="78e9c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78e9c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78e9c-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="78e9c-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="78e9c-124">Godzina lub godzina, po której potok został zaktualizowany w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="78e9c-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="78e9c-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="78e9c-126">Godzina lub wcześniejsza aktualizacja potoku w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="78e9c-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="78e9c-127">-PipelineName</span></span>
<span data-ttu-id="78e9c-128">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="78e9c-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="78e9c-129">-PipelineRunId</span></span>
<span data-ttu-id="78e9c-130">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="78e9c-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e9c-131">-ResourceGroupName</span></span>
<span data-ttu-id="78e9c-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78e9c-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e9c-133">CommonParameters</span></span>
<span data-ttu-id="78e9c-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e9c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78e9c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e9c-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78e9c-136">INPUTS</span></span>

### <span data-ttu-id="78e9c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78e9c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="78e9c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="78e9c-138">System.String</span></span>

## <span data-ttu-id="78e9c-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78e9c-139">OUTPUTS</span></span>

### <span data-ttu-id="78e9c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="78e9c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="78e9c-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78e9c-141">NOTES</span></span>

## <span data-ttu-id="78e9c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78e9c-142">RELATED LINKS</span></span>

[<span data-ttu-id="78e9c-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="78e9c-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="78e9c-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="78e9c-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

