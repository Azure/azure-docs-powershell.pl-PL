---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 5af781170418ea2ab9e0dda9dcd06107e9e784bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706004"
---
# <span data-ttu-id="096c8-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="096c8-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="096c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="096c8-102">SYNOPSIS</span></span>
  <span data-ttu-id="096c8-103">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="096c8-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="096c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="096c8-104">SYNTAX</span></span>

### <span data-ttu-id="096c8-105">ByFactoryNameByParameterFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="096c8-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="096c8-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="096c8-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="096c8-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="096c8-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="096c8-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="096c8-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="096c8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="096c8-109">DESCRIPTION</span></span>
<span data-ttu-id="096c8-110">Polecenie **Invoke-AzDataFactoryV2Pipeline** rozpoczyna działanie w określonym potoku i zwraca identyfikator.</span><span class="sxs-lookup"><span data-stu-id="096c8-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="096c8-111">Ten identyfikator GUID można przekazać do **AzDataFactoryV2PipelineRun** lub **Get-AzDataFactoryV2ActivityRun** , aby uzyskać więcej informacji na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="096c8-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="096c8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="096c8-112">EXAMPLES</span></span>

### <span data-ttu-id="096c8-113">Przykład 1: wywoływanie rurociągu w celu rozpoczęcia uruchamiania</span><span class="sxs-lookup"><span data-stu-id="096c8-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="096c8-114">To polecenie rozpoczyna uruchamianie rurociągu "DPWikisample" w fabryce "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="096c8-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="096c8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="096c8-115">PARAMETERS</span></span>

### <span data-ttu-id="096c8-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="096c8-116">-DataFactoryName</span></span>
<span data-ttu-id="096c8-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="096c8-117">The data factory name.</span></span>

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

### <span data-ttu-id="096c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096c8-118">-DefaultProfile</span></span>
<span data-ttu-id="096c8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="096c8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096c8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="096c8-120">-InputObject</span></span>
<span data-ttu-id="096c8-121">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="096c8-121">The data factory object.</span></span>

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

### <span data-ttu-id="096c8-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="096c8-122">-Parameter</span></span>
<span data-ttu-id="096c8-123">Parametry uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="096c8-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="096c8-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="096c8-124">-ParameterFile</span></span>
<span data-ttu-id="096c8-125">Nazwa pliku z parametrami w celu uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="096c8-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="096c8-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="096c8-126">-PipelineName</span></span>
<span data-ttu-id="096c8-127">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="096c8-127">The pipeline name.</span></span>

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

### <span data-ttu-id="096c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="096c8-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="096c8-129">The resource group name.</span></span>

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

### <span data-ttu-id="096c8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="096c8-130">-Confirm</span></span>
<span data-ttu-id="096c8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="096c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096c8-132">-WhatIf</span></span>
<span data-ttu-id="096c8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="096c8-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="096c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096c8-134">CommonParameters</span></span>
<span data-ttu-id="096c8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096c8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096c8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="096c8-137">INPUTS</span></span>

### <span data-ttu-id="096c8-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="096c8-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="096c8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="096c8-139">System.String</span></span>

### <span data-ttu-id="096c8-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="096c8-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="096c8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="096c8-141">OUTPUTS</span></span>

### <span data-ttu-id="096c8-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="096c8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="096c8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="096c8-143">NOTES</span></span>

## <span data-ttu-id="096c8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="096c8-144">RELATED LINKS</span></span>

[<span data-ttu-id="096c8-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="096c8-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="096c8-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="096c8-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

