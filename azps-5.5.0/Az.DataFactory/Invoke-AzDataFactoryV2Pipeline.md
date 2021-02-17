---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198827"
---
# <span data-ttu-id="e759c-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e759c-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e759c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e759c-102">SYNOPSIS</span></span>
  <span data-ttu-id="e759c-103">Wywołuje potok, aby rozpocząć jego uruchamianie.</span><span class="sxs-lookup"><span data-stu-id="e759c-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="e759c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e759c-104">SYNTAX</span></span>

### <span data-ttu-id="e759c-105">ByFactoryNameByParameterFile (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e759c-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e759c-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="e759c-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e759c-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e759c-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e759c-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e759c-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e759c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e759c-109">DESCRIPTION</span></span>
<span data-ttu-id="e759c-110">Polecenie **Invoke-AzDataFactoryV2Pipeline** uruchamia uruchomienie w określonym potoku i zwraca identyfikator tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e759c-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="e759c-111">Ten identyfikator GUID można przekazywane do **get-AzDataFactoryV2PipelineRun** lub **Get-AzDataFactoryV2ActivityRun,** aby uzyskać szczegółowe informacje na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e759c-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="e759c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e759c-112">EXAMPLES</span></span>

### <span data-ttu-id="e759c-113">Przykład 1. Wywoływanie potoku w celu uruchomienia</span><span class="sxs-lookup"><span data-stu-id="e759c-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="e759c-114">To polecenie uruchamia uruchomienie potoku "DPWikisample" w zakładzie typu WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e759c-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="e759c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e759c-115">Example 2</span></span>

<span data-ttu-id="e759c-116">Wywołuje potok, aby rozpocząć jego uruchamianie.</span><span class="sxs-lookup"><span data-stu-id="e759c-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="e759c-117">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="e759c-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="e759c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e759c-118">PARAMETERS</span></span>

### <span data-ttu-id="e759c-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e759c-119">-DataFactoryName</span></span>
<span data-ttu-id="e759c-120">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="e759c-120">The data factory name.</span></span>

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

### <span data-ttu-id="e759c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e759c-121">-DefaultProfile</span></span>
<span data-ttu-id="e759c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e759c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e759c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e759c-123">-InputObject</span></span>
<span data-ttu-id="e759c-124">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="e759c-124">The data factory object.</span></span>

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

### <span data-ttu-id="e759c-125">— IsRecovery</span><span class="sxs-lookup"><span data-stu-id="e759c-125">-IsRecovery</span></span>
<span data-ttu-id="e759c-126">Flaga trybu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e759c-126">Recovery mode flag.</span></span> <span data-ttu-id="e759c-127">Jeśli tryb odzyskiwania ma wartość True (Prawda), potok, do których prowadzi odwołanie, zostanie pogrupowany według tego samego groupId.</span><span class="sxs-lookup"><span data-stu-id="e759c-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="e759c-128">- Parametr</span><span class="sxs-lookup"><span data-stu-id="e759c-128">-Parameter</span></span>
<span data-ttu-id="e759c-129">Parametry uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="e759c-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="e759c-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="e759c-130">-ParameterFile</span></span>
<span data-ttu-id="e759c-131">Nazwa pliku z parametrami do uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="e759c-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="e759c-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="e759c-132">-PipelineName</span></span>
<span data-ttu-id="e759c-133">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="e759c-133">The pipeline name.</span></span>

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

### <span data-ttu-id="e759c-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e759c-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="e759c-135">Identyfikator uruchomienia potoku dla ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e759c-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="e759c-136">Jeśli zostanie określony identyfikator uruchomienia, parametry określonego uruchomienia zostaną użyte do utworzenia nowego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e759c-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="e759c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e759c-137">-ResourceGroupName</span></span>
<span data-ttu-id="e759c-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e759c-138">The resource group name.</span></span>

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

### <span data-ttu-id="e759c-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="e759c-139">-StartActivityName</span></span>
<span data-ttu-id="e759c-140">W trybie odzyskiwania ponowne uruchomienie rozpocznie się od tego działania.</span><span class="sxs-lookup"><span data-stu-id="e759c-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="e759c-141">Jeśli nie zostanie określona, zostaną uruchomione wszystkie działania.</span><span class="sxs-lookup"><span data-stu-id="e759c-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="e759c-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="e759c-142">-StartFromFailure</span></span>
<span data-ttu-id="e759c-143">Uruchom ponownie flagę działań, których nie udało się uruchomić.</span><span class="sxs-lookup"><span data-stu-id="e759c-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="e759c-144">W trybie odzyskiwania, jeśli zostanie określony, ponowne uruchomienie rozpocznie się od działań, których niepowodzenie nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e759c-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="e759c-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e759c-145">-Confirm</span></span>
<span data-ttu-id="e759c-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e759c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e759c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e759c-147">-WhatIf</span></span>
<span data-ttu-id="e759c-148">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e759c-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e759c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e759c-149">CommonParameters</span></span>
<span data-ttu-id="e759c-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e759c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e759c-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e759c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e759c-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e759c-152">INPUTS</span></span>

### <span data-ttu-id="e759c-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e759c-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="e759c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="e759c-154">System.String</span></span>

### <span data-ttu-id="e759c-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e759c-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e759c-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e759c-156">OUTPUTS</span></span>

### <span data-ttu-id="e759c-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e759c-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e759c-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e759c-158">NOTES</span></span>

## <span data-ttu-id="e759c-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e759c-159">RELATED LINKS</span></span>

[<span data-ttu-id="e759c-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e759c-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="e759c-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e759c-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

