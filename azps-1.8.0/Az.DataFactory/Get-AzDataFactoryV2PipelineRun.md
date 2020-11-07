---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: eba11e68d23c852426a7d4541359874bd813fc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710116"
---
# <span data-ttu-id="63c6f-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="63c6f-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="63c6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="63c6f-103">Pobiera informacje o przebiegach potokowych.</span><span class="sxs-lookup"><span data-stu-id="63c6f-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="63c6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63c6f-104">SYNTAX</span></span>

### <span data-ttu-id="63c6f-105">ByFactoryNameByRunId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63c6f-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63c6f-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="63c6f-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63c6f-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="63c6f-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63c6f-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="63c6f-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63c6f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="63c6f-109">DESCRIPTION</span></span>
<span data-ttu-id="63c6f-110">Polecenie **Get-AzDataFactoryV2PipelineRun** zwraca informacje dotyczące uruchamiania określonego potoku.</span><span class="sxs-lookup"><span data-stu-id="63c6f-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="63c6f-111">Jeśli PipelineRunId jest określony, wyświetlane są szczegóły dotyczące uruchamiania z tym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="63c6f-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="63c6f-112">Jeśli nie podano PipelineRunId, wyświetlane są informacje dotyczące wszystkich uruchomień określonego rurociągu, które wystąpiły między wartościami LastUpdatedAfter i LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="63c6f-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="63c6f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63c6f-113">EXAMPLES</span></span>

### <span data-ttu-id="63c6f-114">Przykład 1: uzyskiwanie informacji na temat uruchamiania pipline</span><span class="sxs-lookup"><span data-stu-id="63c6f-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="63c6f-115">To polecenie pobiera szczegóły dotyczące procesu o IDENTYFIKATORze "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="63c6f-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="63c6f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63c6f-116">PARAMETERS</span></span>

### <span data-ttu-id="63c6f-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="63c6f-117">-DataFactory</span></span>
<span data-ttu-id="63c6f-118">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="63c6f-118">The data factory object.</span></span>

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

### <span data-ttu-id="63c6f-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="63c6f-119">-DataFactoryName</span></span>
<span data-ttu-id="63c6f-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="63c6f-120">The data factory name.</span></span>

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

### <span data-ttu-id="63c6f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c6f-121">-DefaultProfile</span></span>
<span data-ttu-id="63c6f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63c6f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63c6f-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="63c6f-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="63c6f-124">Czas, po którym uruchomiony potok został zaktualizowany w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="63c6f-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="63c6f-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="63c6f-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="63c6f-126">Czas, w którym lub przed upływem którego uruchomienie rurociągu został zaktualizowany w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="63c6f-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="63c6f-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="63c6f-127">-PipelineName</span></span>
<span data-ttu-id="63c6f-128">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="63c6f-128">The pipeline name.</span></span>

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

### <span data-ttu-id="63c6f-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="63c6f-129">-PipelineRunId</span></span>
<span data-ttu-id="63c6f-130">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="63c6f-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="63c6f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c6f-131">-ResourceGroupName</span></span>
<span data-ttu-id="63c6f-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="63c6f-132">The resource group name.</span></span>

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

### <span data-ttu-id="63c6f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c6f-133">CommonParameters</span></span>
<span data-ttu-id="63c6f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c6f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c6f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63c6f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c6f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63c6f-136">INPUTS</span></span>

### <span data-ttu-id="63c6f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="63c6f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="63c6f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="63c6f-138">System.String</span></span>

## <span data-ttu-id="63c6f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63c6f-139">OUTPUTS</span></span>

### <span data-ttu-id="63c6f-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="63c6f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="63c6f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63c6f-141">NOTES</span></span>

## <span data-ttu-id="63c6f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63c6f-142">RELATED LINKS</span></span>

[<span data-ttu-id="63c6f-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63c6f-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="63c6f-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="63c6f-144">Get-AzDataFactoryV2ActivityRun</span></span>]()
