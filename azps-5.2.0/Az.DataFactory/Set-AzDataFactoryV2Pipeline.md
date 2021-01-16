---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355294"
---
# <span data-ttu-id="36b2a-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="36b2a-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="36b2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="36b2a-103">Tworzy potok w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="36b2a-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="36b2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36b2a-104">SYNTAX</span></span>

### <span data-ttu-id="36b2a-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36b2a-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36b2a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36b2a-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b2a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36b2a-107">DESCRIPTION</span></span>
<span data-ttu-id="36b2a-108">Polecenie cmdlet Set-AzDataFactoryV2Pipeline tworzy potok w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="36b2a-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="36b2a-109">Jeśli określisz nazwę dla potoku, który już istnieje, polecenie cmdlet monituje o potwierdzenie przed zastąpieniem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="36b2a-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="36b2a-110">Jeśli określisz parametr Force, polecenie cmdlet zastąpi istniejący potok bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="36b2a-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="36b2a-111">Wykonuj następujące operacje w następującej kolejności:--Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="36b2a-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="36b2a-112">--Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="36b2a-112">-- Create linked services.</span></span>
<span data-ttu-id="36b2a-113">--Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="36b2a-113">-- Create datasets.</span></span>
<span data-ttu-id="36b2a-114">— Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="36b2a-114">-- Create a pipeline.</span></span>
<span data-ttu-id="36b2a-115">Jeśli rurociąg o tej samej nazwie już istnieje w fabryce danych, to polecenie cmdlet wyświetli monit o potwierdzenie zamiaru zastąpienia istniejącego rurociągu nowym rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="36b2a-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="36b2a-116">W przypadku potwierdzenia zastąpienia istniejącego rurociągu definicja potoku jest również zamieniana.</span><span class="sxs-lookup"><span data-stu-id="36b2a-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="36b2a-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36b2a-117">EXAMPLES</span></span>

### <span data-ttu-id="36b2a-118">Przykład 1. Tworzenie rurociągu</span><span class="sxs-lookup"><span data-stu-id="36b2a-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="36b2a-119">To polecenie tworzy potok o nazwie DPWikisample w fabryce danych o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="36b2a-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="36b2a-120">Polecenie opiera się na potoku informacji w DPWikisample.jspliku.</span><span class="sxs-lookup"><span data-stu-id="36b2a-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="36b2a-121">Ten plik zawiera informacje o działaniach, takich jak aktywność kopiowania i Usługa HDInsight w potoku.</span><span class="sxs-lookup"><span data-stu-id="36b2a-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="36b2a-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36b2a-122">PARAMETERS</span></span>

### <span data-ttu-id="36b2a-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="36b2a-123">-DataFactoryName</span></span>
<span data-ttu-id="36b2a-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="36b2a-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="36b2a-125">To polecenie cmdlet tworzy potok dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="36b2a-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="36b2a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b2a-126">-DefaultProfile</span></span>
<span data-ttu-id="36b2a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36b2a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b2a-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="36b2a-128">-DefinitionFile</span></span>
<span data-ttu-id="36b2a-129">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="36b2a-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b2a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="36b2a-130">-Force</span></span>
<span data-ttu-id="36b2a-131">Wskazuje, że to polecenie cmdlet zamieni istniejące potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36b2a-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="36b2a-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36b2a-132">-Name</span></span>
<span data-ttu-id="36b2a-133">Określa nazwę potoku, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="36b2a-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b2a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b2a-134">-ResourceGroupName</span></span>
<span data-ttu-id="36b2a-135">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36b2a-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="36b2a-136">To polecenie cmdlet tworzy potok dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="36b2a-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="36b2a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b2a-137">-ResourceId</span></span>
<span data-ttu-id="36b2a-138">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36b2a-138">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b2a-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36b2a-139">-Confirm</span></span>
<span data-ttu-id="36b2a-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36b2a-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b2a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b2a-141">-WhatIf</span></span>
<span data-ttu-id="36b2a-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36b2a-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b2a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b2a-143">CommonParameters</span></span>
<span data-ttu-id="36b2a-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b2a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b2a-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b2a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b2a-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36b2a-146">INPUTS</span></span>

### <span data-ttu-id="36b2a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="36b2a-147">System.String</span></span>

## <span data-ttu-id="36b2a-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36b2a-148">OUTPUTS</span></span>

### <span data-ttu-id="36b2a-149">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="36b2a-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="36b2a-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36b2a-150">NOTES</span></span>
<span data-ttu-id="36b2a-151">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="36b2a-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="36b2a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36b2a-152">RELATED LINKS</span></span>

[<span data-ttu-id="36b2a-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="36b2a-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="36b2a-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="36b2a-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="36b2a-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="36b2a-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
