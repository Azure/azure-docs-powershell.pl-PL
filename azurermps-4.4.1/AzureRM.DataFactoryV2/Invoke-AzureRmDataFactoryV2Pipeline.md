---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718544"
---
# <span data-ttu-id="218be-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="218be-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="218be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="218be-102">SYNOPSIS</span></span>
  <span data-ttu-id="218be-103">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="218be-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="218be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="218be-104">SYNTAX</span></span>

### <span data-ttu-id="218be-105">ByFactoryNameByParameterFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="218be-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="218be-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="218be-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="218be-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="218be-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="218be-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="218be-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="218be-109">Opis</span><span class="sxs-lookup"><span data-stu-id="218be-109">DESCRIPTION</span></span>
<span data-ttu-id="218be-110">Polecenie **Invoke-AzureRmDataFactoryV2Pipeline** rozpoczyna działanie w określonym potoku i zwraca identyfikator.</span><span class="sxs-lookup"><span data-stu-id="218be-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="218be-111">Ten identyfikator GUID można przekazać do **AzureRmDataFactoryV2PipelineRun** lub **Get-AzureRmDataFactoryV2ActivityRun** , aby uzyskać więcej informacji na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="218be-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="218be-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="218be-112">EXAMPLES</span></span>

### <span data-ttu-id="218be-113">Przykład 1: wywoływanie rurociągu w celu rozpoczęcia uruchamiania</span><span class="sxs-lookup"><span data-stu-id="218be-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="218be-114">To polecenie rozpoczyna uruchamianie rurociągu "DPWikisample" w fabryce "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="218be-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="218be-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="218be-115">PARAMETERS</span></span>

### <span data-ttu-id="218be-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="218be-116">-Confirm</span></span>
<span data-ttu-id="218be-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="218be-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="218be-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="218be-118">-DataFactoryName</span></span>
<span data-ttu-id="218be-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="218be-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218be-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="218be-120">-ParameterFile</span></span>
<span data-ttu-id="218be-121">Nazwa pliku z parametrami w celu uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="218be-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218be-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="218be-122">-Parameter</span></span>
<span data-ttu-id="218be-123">Parametry uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="218be-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218be-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="218be-124">-InputObject</span></span>
<span data-ttu-id="218be-125">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="218be-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="218be-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="218be-126">-PipelineName</span></span>
<span data-ttu-id="218be-127">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="218be-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218be-128">-ResourceGroupName</span></span>
<span data-ttu-id="218be-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="218be-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218be-130">-WhatIf</span></span>
<span data-ttu-id="218be-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="218be-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="218be-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="218be-132">INPUTS</span></span>

### <span data-ttu-id="218be-133">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="218be-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="218be-134">System. String system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="218be-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="218be-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="218be-135">OUTPUTS</span></span>

### <span data-ttu-id="218be-136">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="218be-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="218be-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="218be-137">NOTES</span></span>

## <span data-ttu-id="218be-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="218be-138">RELATED LINKS</span></span>
[<span data-ttu-id="218be-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="218be-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="218be-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="218be-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

