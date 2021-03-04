---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: ad731dc612290e572ee74a967788e324f764a930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971233"
---
# <span data-ttu-id="befea-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="befea-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="befea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befea-102">SYNOPSIS</span></span>
<span data-ttu-id="befea-103">Tworzy potok w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="befea-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="befea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="befea-104">SYNTAX</span></span>

### <span data-ttu-id="befea-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="befea-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="befea-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="befea-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="befea-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="befea-107">DESCRIPTION</span></span>
<span data-ttu-id="befea-108">Polecenie **cmdlet New-AzDataFactoryPipeline** tworzy potok w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="befea-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="befea-109">Jeśli określisz nazwę dla potoku, który już istnieje, polecenie cmdlet wyświetli monit o potwierdzenie, zanim zastąpi potok.</span><span class="sxs-lookup"><span data-stu-id="befea-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="befea-110">Jeśli określisz parametr *Force,* polecenie cmdlet zastąpi istniejący potok bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="befea-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="befea-111">Wykonaj te operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="befea-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="befea-112">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="befea-112">Create a data factory.</span></span> 
- <span data-ttu-id="befea-113">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="befea-113">Create linked services.</span></span> 
- <span data-ttu-id="befea-114">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="befea-114">Create datasets.</span></span> 
- <span data-ttu-id="befea-115">Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="befea-115">Create a pipeline.</span></span>
<span data-ttu-id="befea-116">Jeśli w factory danych istnieje już potok o takiej samej nazwie, to polecenie cmdlet wyświetli monit o potwierdzenie, czy zastąpić istniejący potok nowym potokiem.</span><span class="sxs-lookup"><span data-stu-id="befea-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="befea-117">Jeśli potwierdzisz zastąpienie istniejącego potoku, definicja potoku również zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="befea-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="befea-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="befea-118">EXAMPLES</span></span>

### <span data-ttu-id="befea-119">Przykład 1. Tworzenie potoku</span><span class="sxs-lookup"><span data-stu-id="befea-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="befea-120">To polecenie tworzy potok o nazwie DPWikisample w fabrycznej układzie danych O nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="befea-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="befea-121">Polecenie bazuje na informacjach w pliku DPWikisample.jsplikach.</span><span class="sxs-lookup"><span data-stu-id="befea-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="befea-122">Ten plik zawiera informacje o działaniach, takich jak Działanie kopiowania i Aktywność hdInsight w potoku.</span><span class="sxs-lookup"><span data-stu-id="befea-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="befea-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="befea-123">PARAMETERS</span></span>

### <span data-ttu-id="befea-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="befea-124">-DataFactory</span></span>
<span data-ttu-id="befea-125">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="befea-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="befea-126">To polecenie cmdlet tworzy potok dla fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="befea-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="befea-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="befea-127">-DataFactoryName</span></span>
<span data-ttu-id="befea-128">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="befea-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="befea-129">To polecenie cmdlet tworzy potok dla fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="befea-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="befea-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befea-130">-DefaultProfile</span></span>
<span data-ttu-id="befea-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="befea-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="befea-132">— Plik</span><span class="sxs-lookup"><span data-stu-id="befea-132">-File</span></span>
<span data-ttu-id="befea-133">Określa pełną ścieżkę pliku JavaScript Object Notation (JSON) zawierającego opis potoku.</span><span class="sxs-lookup"><span data-stu-id="befea-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befea-134">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="befea-134">-Force</span></span>
<span data-ttu-id="befea-135">Wskazuje, że to polecenie cmdlet zastępuje istniejący potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="befea-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="befea-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="befea-136">-Name</span></span>
<span data-ttu-id="befea-137">Określa nazwę potoku do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="befea-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="befea-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befea-138">-ResourceGroupName</span></span>
<span data-ttu-id="befea-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="befea-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="befea-140">To polecenie cmdlet tworzy potok dla grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="befea-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="befea-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="befea-141">-Confirm</span></span>
<span data-ttu-id="befea-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="befea-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befea-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="befea-143">-WhatIf</span></span>
<span data-ttu-id="befea-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="befea-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="befea-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="befea-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befea-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befea-146">CommonParameters</span></span>
<span data-ttu-id="befea-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="befea-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befea-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="befea-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befea-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="befea-149">INPUTS</span></span>

### <span data-ttu-id="befea-150">System.String</span><span class="sxs-lookup"><span data-stu-id="befea-150">System.String</span></span>

### <span data-ttu-id="befea-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="befea-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="befea-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="befea-152">OUTPUTS</span></span>

### <span data-ttu-id="befea-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="befea-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="befea-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="befea-154">NOTES</span></span>
* <span data-ttu-id="befea-155">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="befea-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="befea-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="befea-156">RELATED LINKS</span></span>

[<span data-ttu-id="befea-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="befea-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="befea-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="befea-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="befea-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="befea-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="befea-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="befea-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="befea-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="befea-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


