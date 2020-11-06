---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: a7486c3fc50e5c6517022190e05d099329fc6001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546263"
---
# <span data-ttu-id="1cc5d-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1cc5d-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1cc5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1cc5d-102">SYNOPSIS</span></span>
  <span data-ttu-id="1cc5d-103">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cc5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1cc5d-104">SYNTAX</span></span>

### <span data-ttu-id="1cc5d-105">ByFactoryNameByParameterFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1cc5d-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc5d-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="1cc5d-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc5d-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1cc5d-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc5d-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1cc5d-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc5d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1cc5d-109">DESCRIPTION</span></span>
<span data-ttu-id="1cc5d-110">Polecenie **Invoke-AzureRmDataFactoryV2Pipeline** rozpoczyna działanie w określonym potoku i zwraca identyfikator.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="1cc5d-111">Ten identyfikator GUID można przekazać do **AzureRmDataFactoryV2PipelineRun** lub **Get-AzureRmDataFactoryV2ActivityRun** , aby uzyskać więcej informacji na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="1cc5d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1cc5d-112">EXAMPLES</span></span>

### <span data-ttu-id="1cc5d-113">Przykład 1: wywoływanie rurociągu w celu rozpoczęcia uruchamiania</span><span class="sxs-lookup"><span data-stu-id="1cc5d-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="1cc5d-114">To polecenie rozpoczyna uruchamianie rurociągu "DPWikisample" w fabryce "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1cc5d-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="1cc5d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1cc5d-115">PARAMETERS</span></span>

### <span data-ttu-id="1cc5d-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1cc5d-116">-Confirm</span></span>
<span data-ttu-id="1cc5d-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc5d-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1cc5d-118">-DataFactoryName</span></span>
<span data-ttu-id="1cc5d-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-119">The data factory name.</span></span>

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

### <span data-ttu-id="1cc5d-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="1cc5d-120">-ParameterFile</span></span>
<span data-ttu-id="1cc5d-121">Nazwa pliku z parametrami w celu uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-121">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1cc5d-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1cc5d-122">-Parameter</span></span>
<span data-ttu-id="1cc5d-123">Parametry uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1cc5d-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1cc5d-124">-InputObject</span></span>
<span data-ttu-id="1cc5d-125">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-125">The data factory object.</span></span>

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

### <span data-ttu-id="1cc5d-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="1cc5d-126">-PipelineName</span></span>
<span data-ttu-id="1cc5d-127">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-127">The pipeline name.</span></span>

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

### <span data-ttu-id="1cc5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="1cc5d-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-129">The resource group name.</span></span>

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

### <span data-ttu-id="1cc5d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc5d-130">-WhatIf</span></span>
<span data-ttu-id="1cc5d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1cc5d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc5d-132">-DefaultProfile</span></span>
<span data-ttu-id="1cc5d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cc5d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc5d-134">CommonParameters</span></span>
<span data-ttu-id="1cc5d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc5d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc5d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc5d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cc5d-137">INPUTS</span></span>

### <span data-ttu-id="1cc5d-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1cc5d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="1cc5d-139">System. String system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1cc5d-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="1cc5d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1cc5d-140">OUTPUTS</span></span>

### <span data-ttu-id="1cc5d-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1cc5d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1cc5d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1cc5d-142">NOTES</span></span>

## <span data-ttu-id="1cc5d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cc5d-143">RELATED LINKS</span></span>

[<span data-ttu-id="1cc5d-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="1cc5d-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="1cc5d-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="1cc5d-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

