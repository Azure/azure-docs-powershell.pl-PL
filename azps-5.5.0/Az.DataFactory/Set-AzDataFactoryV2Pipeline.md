---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238270"
---
# <span data-ttu-id="c1f3e-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1f3e-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="c1f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f3e-103">Tworzy potok w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="c1f3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1f3e-104">SYNTAX</span></span>

### <span data-ttu-id="c1f3e-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="c1f3e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1f3e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f3e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1f3e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1f3e-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f3e-108">Polecenie Set-AzDataFactoryV2Pipeline cmdlet tworzy potok w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="c1f3e-109">Jeśli określisz nazwę dla potoku, który już istnieje, polecenie cmdlet wyświetli monit o potwierdzenie, zanim zastąpi potok.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="c1f3e-110">Jeśli określisz parametr Force, polecenie cmdlet zastąpi istniejący potok bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="c1f3e-111">Wykonaj następujące operacje w następującej kolejności: — Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="c1f3e-112">— Tworzenie usług połączonych.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-112">-- Create linked services.</span></span>
<span data-ttu-id="c1f3e-113">— Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-113">-- Create datasets.</span></span>
<span data-ttu-id="c1f3e-114">— Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-114">-- Create a pipeline.</span></span>
<span data-ttu-id="c1f3e-115">Jeśli w factory danych istnieje już potok o takiej samej nazwie, to polecenie cmdlet wyświetli monit o potwierdzenie, czy zastąpić istniejący potok nowym potokiem.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="c1f3e-116">Jeśli potwierdzisz zastąpienie istniejącego potoku, definicja potoku również zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="c1f3e-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1f3e-117">EXAMPLES</span></span>

### <span data-ttu-id="c1f3e-118">Przykład 1. Tworzenie potoku</span><span class="sxs-lookup"><span data-stu-id="c1f3e-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="c1f3e-119">To polecenie tworzy potok o nazwie DPWikisample w zakładzie danych O nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="c1f3e-120">Polecenie bazuje na informacjach z DPWikisample.jspliku.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="c1f3e-121">Ten plik zawiera informacje o działaniach, takich jak Działanie kopiowania i Aktywność hdInsight w potoku.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="c1f3e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1f3e-122">PARAMETERS</span></span>

### <span data-ttu-id="c1f3e-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c1f3e-123">-DataFactoryName</span></span>
<span data-ttu-id="c1f3e-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c1f3e-125">To polecenie cmdlet tworzy potok dla fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1f3e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f3e-126">-DefaultProfile</span></span>
<span data-ttu-id="c1f3e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1f3e-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c1f3e-128">-DefinitionFile</span></span>
<span data-ttu-id="c1f3e-129">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-129">The JSON file path.</span></span>

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

### <span data-ttu-id="c1f3e-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c1f3e-130">-Force</span></span>
<span data-ttu-id="c1f3e-131">Wskazuje, że to polecenie cmdlet zastępuje istniejący potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c1f3e-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c1f3e-132">-Name</span></span>
<span data-ttu-id="c1f3e-133">Określa nazwę potoku do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="c1f3e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f3e-134">-ResourceGroupName</span></span>
<span data-ttu-id="c1f3e-135">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c1f3e-136">To polecenie cmdlet tworzy potok dla grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1f3e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f3e-137">-ResourceId</span></span>
<span data-ttu-id="c1f3e-138">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c1f3e-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1f3e-139">-Confirm</span></span>
<span data-ttu-id="c1f3e-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1f3e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f3e-141">-WhatIf</span></span>
<span data-ttu-id="c1f3e-142">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c1f3e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f3e-143">CommonParameters</span></span>
<span data-ttu-id="c1f3e-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f3e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f3e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f3e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f3e-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1f3e-146">INPUTS</span></span>

### <span data-ttu-id="c1f3e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c1f3e-147">System.String</span></span>

## <span data-ttu-id="c1f3e-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1f3e-148">OUTPUTS</span></span>

### <span data-ttu-id="c1f3e-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c1f3e-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="c1f3e-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1f3e-150">NOTES</span></span>
<span data-ttu-id="c1f3e-151">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="c1f3e-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c1f3e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1f3e-152">RELATED LINKS</span></span>

[<span data-ttu-id="c1f3e-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1f3e-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c1f3e-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1f3e-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c1f3e-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1f3e-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
