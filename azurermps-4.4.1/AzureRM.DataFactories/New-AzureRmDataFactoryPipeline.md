---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ae640ffb0f595419bba57ff92d7789692af55d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527669"
---
# <span data-ttu-id="d1ac3-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1ac3-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="d1ac3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ac3-103">Tworzy potok w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ac3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1ac3-104">SYNTAX</span></span>

### <span data-ttu-id="d1ac3-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1ac3-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ac3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d1ac3-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ac3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1ac3-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ac3-108">Polecenie cmdlet **New-AzureRmDataFactoryPipeline** tworzy potok w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="d1ac3-109">Jeśli określisz nazwę dla potoku, który już istnieje, polecenie cmdlet monituje o potwierdzenie przed zastąpieniem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="d1ac3-110">Jeśli określisz parametr *Force* , polecenie cmdlet zastąpi istniejący potok bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="d1ac3-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="d1ac3-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="d1ac3-112">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-112">Create a data factory.</span></span> 
- <span data-ttu-id="d1ac3-113">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-113">Create linked services.</span></span> 
- <span data-ttu-id="d1ac3-114">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-114">Create datasets.</span></span> 
- <span data-ttu-id="d1ac3-115">Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-115">Create a pipeline.</span></span>

<span data-ttu-id="d1ac3-116">Jeśli rurociąg o tej samej nazwie już istnieje w fabryce danych, to polecenie cmdlet wyświetli monit o potwierdzenie zamiaru zastąpienia istniejącego rurociągu nowym rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="d1ac3-117">W przypadku potwierdzenia zastąpienia istniejącego rurociągu definicja potoku jest również zamieniana.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="d1ac3-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1ac3-118">EXAMPLES</span></span>

### <span data-ttu-id="d1ac3-119">Przykład 1. Tworzenie rurociągu</span><span class="sxs-lookup"><span data-stu-id="d1ac3-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="d1ac3-120">To polecenie tworzy potok o nazwie DPWikisample w fabryce danych o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="d1ac3-121">Polecenie opiera się na potoku informacji w DPWikisample.jspliku.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="d1ac3-122">Ten plik zawiera informacje o działaniach, takich jak aktywność kopiowania i Usługa HDInsight w potoku.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="d1ac3-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1ac3-123">PARAMETERS</span></span>

### <span data-ttu-id="d1ac3-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1ac3-124">-DataFactory</span></span>
<span data-ttu-id="d1ac3-125">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d1ac3-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d1ac3-126">To polecenie cmdlet tworzy potok dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1ac3-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d1ac3-127">-DataFactoryName</span></span>
<span data-ttu-id="d1ac3-128">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d1ac3-129">To polecenie cmdlet tworzy potok dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1ac3-130">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="d1ac3-130">-File</span></span>
<span data-ttu-id="d1ac3-131">Określa pełną ścieżkę pliku notacji JavaScript (kod JSON), który zawiera opis potoku.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="d1ac3-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d1ac3-132">-Force</span></span>
<span data-ttu-id="d1ac3-133">Wskazuje, że to polecenie cmdlet zamieni istniejące potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-133">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d1ac3-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1ac3-134">-Name</span></span>
<span data-ttu-id="d1ac3-135">Określa nazwę potoku, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-135">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="d1ac3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ac3-136">-ResourceGroupName</span></span>
<span data-ttu-id="d1ac3-137">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d1ac3-138">To polecenie cmdlet tworzy potok dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-138">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1ac3-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1ac3-139">-Confirm</span></span>
<span data-ttu-id="d1ac3-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ac3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ac3-141">-WhatIf</span></span>
<span data-ttu-id="d1ac3-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1ac3-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ac3-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ac3-144">-DefaultProfile</span></span>
<span data-ttu-id="d1ac3-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ac3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ac3-146">CommonParameters</span></span>
<span data-ttu-id="d1ac3-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ac3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ac3-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ac3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ac3-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1ac3-149">INPUTS</span></span>

## <span data-ttu-id="d1ac3-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1ac3-150">OUTPUTS</span></span>

### <span data-ttu-id="d1ac3-151">Microsoft. platformy windowsazure. Commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d1ac3-151">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="d1ac3-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1ac3-152">NOTES</span></span>
* <span data-ttu-id="d1ac3-153">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="d1ac3-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d1ac3-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1ac3-154">RELATED LINKS</span></span>

[<span data-ttu-id="d1ac3-155">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1ac3-155">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d1ac3-156">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1ac3-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d1ac3-157">Życiorys — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1ac3-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d1ac3-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d1ac3-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d1ac3-159">Suspend — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1ac3-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


