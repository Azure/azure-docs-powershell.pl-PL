---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e7bfd0b72f5dffe4e5ff4d7e52394846d5f17afa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541775"
---
# <span data-ttu-id="30147-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="30147-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="30147-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30147-102">SYNOPSIS</span></span>
  <span data-ttu-id="30147-103">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="30147-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30147-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30147-104">SYNTAX</span></span>

### <span data-ttu-id="30147-105">ByFactoryNameByParameterFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="30147-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30147-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="30147-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30147-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="30147-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30147-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="30147-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30147-109">Opis</span><span class="sxs-lookup"><span data-stu-id="30147-109">DESCRIPTION</span></span>
<span data-ttu-id="30147-110">Polecenie **Invoke-AzureRmDataFactoryV2Pipeline** rozpoczyna działanie w określonym potoku i zwraca identyfikator.</span><span class="sxs-lookup"><span data-stu-id="30147-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="30147-111">Ten identyfikator GUID można przekazać do **AzureRmDataFactoryV2PipelineRun** lub **Get-AzureRmDataFactoryV2ActivityRun** , aby uzyskać więcej informacji na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="30147-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="30147-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30147-112">EXAMPLES</span></span>

### <span data-ttu-id="30147-113">Przykład 1: wywoływanie rurociągu w celu rozpoczęcia uruchamiania</span><span class="sxs-lookup"><span data-stu-id="30147-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="30147-114">To polecenie rozpoczyna uruchamianie rurociągu "DPWikisample" w fabryce "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="30147-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="30147-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30147-115">PARAMETERS</span></span>

### <span data-ttu-id="30147-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="30147-116">-DataFactoryName</span></span>
<span data-ttu-id="30147-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="30147-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30147-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30147-118">-DefaultProfile</span></span>
<span data-ttu-id="30147-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30147-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30147-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="30147-120">-InputObject</span></span>
<span data-ttu-id="30147-121">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="30147-121">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30147-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="30147-122">-Parameter</span></span>
<span data-ttu-id="30147-123">Parametry uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="30147-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30147-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="30147-124">-ParameterFile</span></span>
<span data-ttu-id="30147-125">Nazwa pliku z parametrami w celu uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="30147-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30147-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="30147-126">-PipelineName</span></span>
<span data-ttu-id="30147-127">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="30147-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30147-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30147-128">-ResourceGroupName</span></span>
<span data-ttu-id="30147-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="30147-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30147-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30147-130">-Confirm</span></span>
<span data-ttu-id="30147-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30147-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30147-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30147-132">-WhatIf</span></span>
<span data-ttu-id="30147-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30147-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="30147-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30147-134">CommonParameters</span></span>
<span data-ttu-id="30147-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30147-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30147-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30147-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30147-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30147-137">INPUTS</span></span>

### <span data-ttu-id="30147-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="30147-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="30147-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30147-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="30147-140">System. String</span><span class="sxs-lookup"><span data-stu-id="30147-140">System.String</span></span>

### <span data-ttu-id="30147-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="30147-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30147-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30147-142">OUTPUTS</span></span>

### <span data-ttu-id="30147-143">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="30147-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="30147-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30147-144">NOTES</span></span>

## <span data-ttu-id="30147-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30147-145">RELATED LINKS</span></span>

[<span data-ttu-id="30147-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="30147-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="30147-147">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="30147-147">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

