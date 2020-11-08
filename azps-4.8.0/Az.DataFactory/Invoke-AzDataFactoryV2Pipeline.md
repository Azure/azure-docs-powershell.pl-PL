---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224005"
---
# <span data-ttu-id="77326-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="77326-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="77326-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77326-102">SYNOPSIS</span></span>
  <span data-ttu-id="77326-103">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="77326-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="77326-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77326-104">SYNTAX</span></span>

### <span data-ttu-id="77326-105">ByFactoryNameByParameterFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77326-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77326-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="77326-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77326-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="77326-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77326-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="77326-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77326-109">Opis</span><span class="sxs-lookup"><span data-stu-id="77326-109">DESCRIPTION</span></span>
<span data-ttu-id="77326-110">Polecenie **Invoke-AzDataFactoryV2Pipeline** rozpoczyna działanie w określonym potoku i zwraca identyfikator.</span><span class="sxs-lookup"><span data-stu-id="77326-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="77326-111">Ten identyfikator GUID można przekazać do **AzDataFactoryV2PipelineRun** lub **Get-AzDataFactoryV2ActivityRun** , aby uzyskać więcej informacji na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="77326-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="77326-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77326-112">EXAMPLES</span></span>

### <span data-ttu-id="77326-113">Przykład 1: wywoływanie rurociągu w celu rozpoczęcia uruchamiania</span><span class="sxs-lookup"><span data-stu-id="77326-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="77326-114">To polecenie rozpoczyna uruchamianie rurociągu "DPWikisample" w fabryce "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="77326-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="77326-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77326-115">Example 2</span></span>

<span data-ttu-id="77326-116">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="77326-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="77326-117">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="77326-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="77326-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77326-118">PARAMETERS</span></span>

### <span data-ttu-id="77326-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="77326-119">-DataFactoryName</span></span>
<span data-ttu-id="77326-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="77326-120">The data factory name.</span></span>

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

### <span data-ttu-id="77326-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77326-121">-DefaultProfile</span></span>
<span data-ttu-id="77326-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77326-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77326-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77326-123">-InputObject</span></span>
<span data-ttu-id="77326-124">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="77326-124">The data factory object.</span></span>

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

### <span data-ttu-id="77326-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="77326-125">-IsRecovery</span></span>
<span data-ttu-id="77326-126">Flaga trybu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="77326-126">Recovery mode flag.</span></span> <span data-ttu-id="77326-127">Jeśli tryb odzyskiwania jest ustawiony na wartość true, określony potok zostanie uruchomiony, a nowy proces zostanie zgrupowany w tym samym identyfikatorze groupId.</span><span class="sxs-lookup"><span data-stu-id="77326-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77326-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="77326-128">-Parameter</span></span>
<span data-ttu-id="77326-129">Parametry uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="77326-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="77326-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="77326-130">-ParameterFile</span></span>
<span data-ttu-id="77326-131">Nazwa pliku z parametrami w celu uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="77326-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="77326-132">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="77326-132">-PipelineName</span></span>
<span data-ttu-id="77326-133">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="77326-133">The pipeline name.</span></span>

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

### <span data-ttu-id="77326-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="77326-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="77326-135">Identyfikator uruchomienia potoku w celu ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="77326-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="77326-136">Jeśli jest określony identyfikator uruchomienia, w celu utworzenia nowego uruchomienia zostanie użyte parametry określonego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="77326-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77326-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77326-137">-ResourceGroupName</span></span>
<span data-ttu-id="77326-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77326-138">The resource group name.</span></span>

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

### <span data-ttu-id="77326-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="77326-139">-StartActivityName</span></span>
<span data-ttu-id="77326-140">W trybie odzyskiwania rozpocznie się ponowne uruchomienie od tego działania.</span><span class="sxs-lookup"><span data-stu-id="77326-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="77326-141">Jeśli nie określono, zostaną uruchomione wszystkie działania.</span><span class="sxs-lookup"><span data-stu-id="77326-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77326-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="77326-142">-StartFromFailure</span></span>
<span data-ttu-id="77326-143">Uruchom ponownie działanie od flagi działań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="77326-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="77326-144">Jeśli jest określony tryb odzyskiwania, ponowne uruchomienie rozpoczyna się od działań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="77326-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77326-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77326-145">-Confirm</span></span>
<span data-ttu-id="77326-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77326-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77326-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77326-147">-WhatIf</span></span>
<span data-ttu-id="77326-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77326-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="77326-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77326-149">CommonParameters</span></span>
<span data-ttu-id="77326-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77326-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77326-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77326-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77326-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77326-152">INPUTS</span></span>

### <span data-ttu-id="77326-153">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="77326-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="77326-154">System. String</span><span class="sxs-lookup"><span data-stu-id="77326-154">System.String</span></span>

### <span data-ttu-id="77326-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="77326-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="77326-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77326-156">OUTPUTS</span></span>

### <span data-ttu-id="77326-157">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="77326-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="77326-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77326-158">NOTES</span></span>

## <span data-ttu-id="77326-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77326-159">RELATED LINKS</span></span>

[<span data-ttu-id="77326-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="77326-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="77326-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="77326-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

