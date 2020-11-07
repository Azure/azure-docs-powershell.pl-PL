---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2a936b9a75e9fc1053e2202950a6a6b4c49bd3a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719656"
---
# <span data-ttu-id="f8222-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8222-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f8222-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8222-102">SYNOPSIS</span></span>
<span data-ttu-id="f8222-103">Tworzy potok w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="f8222-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8222-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8222-104">SYNTAX</span></span>

### <span data-ttu-id="f8222-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8222-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f8222-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8222-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="f8222-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8222-107">DESCRIPTION</span></span>
<span data-ttu-id="f8222-108">Polecenie cmdlet Set-AzureRmDataFactoryV2Pipeline tworzy potok w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f8222-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="f8222-109">Jeśli określisz nazwę dla potoku, który już istnieje, polecenie cmdlet monituje o potwierdzenie przed zastąpieniem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f8222-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="f8222-110">Jeśli określisz parametr Force, polecenie cmdlet zastąpi istniejący potok bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="f8222-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="f8222-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="f8222-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="f8222-112">Jeśli rurociąg o tej samej nazwie już istnieje w fabryce danych, to polecenie cmdlet wyświetli monit o potwierdzenie zamiaru zastąpienia istniejącego rurociągu nowym rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="f8222-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="f8222-113">W przypadku potwierdzenia zastąpienia istniejącego rurociągu definicja potoku jest również zamieniana.</span><span class="sxs-lookup"><span data-stu-id="f8222-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="f8222-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8222-114">EXAMPLES</span></span>

### <span data-ttu-id="f8222-115">Przykład 1. Tworzenie rurociągu</span><span class="sxs-lookup"><span data-stu-id="f8222-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="f8222-116">To polecenie tworzy potok o nazwie DPWikisample w fabryce danych o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="f8222-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="f8222-117">Polecenie opiera się na potoku informacji w DPWikisample.jspliku.</span><span class="sxs-lookup"><span data-stu-id="f8222-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="f8222-118">Ten plik zawiera informacje o działaniach, takich jak aktywność kopiowania i Usługa HDInsight w potoku.</span><span class="sxs-lookup"><span data-stu-id="f8222-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="f8222-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8222-119">PARAMETERS</span></span>

### <span data-ttu-id="f8222-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8222-120">-Confirm</span></span>
<span data-ttu-id="f8222-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8222-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8222-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f8222-122">-DataFactoryName</span></span>
<span data-ttu-id="f8222-123">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f8222-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f8222-124">To polecenie cmdlet tworzy potok dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f8222-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8222-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f8222-125">-DefinitionFile</span></span>
<span data-ttu-id="f8222-126">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="f8222-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8222-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f8222-127">-Force</span></span>
<span data-ttu-id="f8222-128">Wskazuje, że to polecenie cmdlet zamieni istniejące potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8222-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f8222-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8222-129">-Name</span></span>
<span data-ttu-id="f8222-130">Określa nazwę potoku, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f8222-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8222-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8222-131">-ResourceGroupName</span></span>
<span data-ttu-id="f8222-132">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f8222-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f8222-133">To polecenie cmdlet tworzy potok dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f8222-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8222-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8222-134">-ResourceId</span></span>
<span data-ttu-id="f8222-135">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f8222-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8222-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8222-136">-WhatIf</span></span>
<span data-ttu-id="f8222-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8222-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f8222-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8222-138">INPUTS</span></span>

### <span data-ttu-id="f8222-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f8222-139">System.String</span></span>


## <span data-ttu-id="f8222-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8222-140">OUTPUTS</span></span>

### <span data-ttu-id="f8222-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f8222-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="f8222-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8222-142">NOTES</span></span>
<span data-ttu-id="f8222-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="f8222-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f8222-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8222-144">RELATED LINKS</span></span>
[<span data-ttu-id="f8222-145">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8222-145">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f8222-146">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8222-146">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f8222-147">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8222-147">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
