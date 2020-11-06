---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552955"
---
# <span data-ttu-id="71b14-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="71b14-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="71b14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71b14-102">SYNOPSIS</span></span>
<span data-ttu-id="71b14-103">Pobiera informacje o przebiegach potokowych.</span><span class="sxs-lookup"><span data-stu-id="71b14-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71b14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71b14-104">SYNTAX</span></span>

### <span data-ttu-id="71b14-105">ByFactoryNameByRunId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71b14-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71b14-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="71b14-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71b14-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="71b14-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71b14-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="71b14-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71b14-109">Opis</span><span class="sxs-lookup"><span data-stu-id="71b14-109">DESCRIPTION</span></span>
<span data-ttu-id="71b14-110">Polecenie **Get-AzureRmDataFactoryV2PipelineRun** zwraca informacje dotyczące uruchamiania określonego potoku.</span><span class="sxs-lookup"><span data-stu-id="71b14-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="71b14-111">Jeśli PipelineRunId jest określony, wyświetlane są szczegóły dotyczące uruchamiania z tym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="71b14-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="71b14-112">Jeśli nie podano PipelineRunId, wyświetlane są informacje dotyczące wszystkich uruchomień określonego rurociągu, które wystąpiły między wartościami LastUpdatedAfter i LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="71b14-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="71b14-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71b14-113">EXAMPLES</span></span>

### <span data-ttu-id="71b14-114">Przykład 1: uzyskiwanie informacji na temat uruchamiania pipline</span><span class="sxs-lookup"><span data-stu-id="71b14-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="71b14-115">To polecenie pobiera szczegóły dotyczące procesu o IDENTYFIKATORze "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="71b14-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="71b14-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71b14-116">PARAMETERS</span></span>

### <span data-ttu-id="71b14-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="71b14-117">-DataFactory</span></span>
<span data-ttu-id="71b14-118">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="71b14-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="71b14-119">-DataFactoryName</span></span>
<span data-ttu-id="71b14-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="71b14-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b14-121">-DefaultProfile</span></span>
<span data-ttu-id="71b14-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71b14-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b14-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="71b14-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="71b14-124">Czas, po którym uruchomiony potok został zaktualizowany w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="71b14-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="71b14-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="71b14-126">Czas, w którym lub przed upływem którego uruchomienie rurociągu został zaktualizowany w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="71b14-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="71b14-127">-PipelineName</span></span>
<span data-ttu-id="71b14-128">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="71b14-128">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="71b14-129">-PipelineRunId</span></span>
<span data-ttu-id="71b14-130">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="71b14-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b14-131">-ResourceGroupName</span></span>
<span data-ttu-id="71b14-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71b14-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b14-133">CommonParameters</span></span>
<span data-ttu-id="71b14-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b14-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b14-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b14-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b14-136">INPUTS</span></span>

### <span data-ttu-id="71b14-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="71b14-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="71b14-138">System. String</span><span class="sxs-lookup"><span data-stu-id="71b14-138">System.String</span></span>

## <span data-ttu-id="71b14-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71b14-139">OUTPUTS</span></span>

### <span data-ttu-id="71b14-140">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSPipelineRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="71b14-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="71b14-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="71b14-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="71b14-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71b14-142">NOTES</span></span>

## <span data-ttu-id="71b14-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71b14-143">RELATED LINKS</span></span>

[<span data-ttu-id="71b14-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="71b14-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="71b14-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="71b14-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

