---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188650"
---
# <span data-ttu-id="cfd1a-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cfd1a-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="cfd1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd1a-103">Pobiera informacje o potokach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="cfd1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cfd1a-104">SYNTAX</span></span>

### <span data-ttu-id="cfd1a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="cfd1a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfd1a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cfd1a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfd1a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cfd1a-107">DESCRIPTION</span></span>
<span data-ttu-id="cfd1a-108">Polecenie **cmdlet Get-AzDataFactoryPipeline** pobiera informacje o potokach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="cfd1a-109">Jeśli określisz nazwę potoku, to polecenie cmdlet pobiera informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="cfd1a-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich potokach w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="cfd1a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cfd1a-111">EXAMPLES</span></span>

### <span data-ttu-id="cfd1a-112">Przykład 1. Uzyskiwanie informacji o wszystkich potokach</span><span class="sxs-lookup"><span data-stu-id="cfd1a-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="cfd1a-113">To polecenie pobiera informacje o wszystkich potokach w fabrycznej układzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="cfd1a-114">Możesz użyć jednego z poniższych poleceń przykładowych.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="cfd1a-115">Drugi obiekt korzysta z **obiektu DataFactory** jako parametru.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="cfd1a-116">Przykład 2. Uzyskiwanie informacji o określonym potoku</span><span class="sxs-lookup"><span data-stu-id="cfd1a-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="cfd1a-117">To polecenie pobiera informacje o potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="cfd1a-118">Polecenie przekazuje te informacje do Format-List cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cfd1a-119">To polecenie cmdlet s formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="cfd1a-120">Aby uzyskać więcej informacji, wpisz `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="cfd1a-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="cfd1a-121">Przykład 3. Uzyskiwanie właściwości określonego potoku</span><span class="sxs-lookup"><span data-stu-id="cfd1a-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="cfd1a-122">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości **Properties** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="cfd1a-123">Przykład 4. Uzyskiwanie działań dla określonego potoku</span><span class="sxs-lookup"><span data-stu-id="cfd1a-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="cfd1a-124">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w zakładzie danych o  nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="cfd1a-125">Przykład 5. Uzyskiwanie informacji dotyczących środowiska uruchomieniowego dla określonego potoku</span><span class="sxs-lookup"><span data-stu-id="cfd1a-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="cfd1a-126">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości **RuntimeInfo** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="cfd1a-127">Przykład 6. Uzyskiwanie informacji o danych wejściowych dla pierwszego działania</span><span class="sxs-lookup"><span data-stu-id="cfd1a-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="cfd1a-128">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie  WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="cfd1a-129">Polecenie wyświetla właściwość **Dane wejściowe** pierwszego elementu tablicy Działania **przy** użyciu opcji **Format-Lista.**</span><span class="sxs-lookup"><span data-stu-id="cfd1a-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="cfd1a-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfd1a-130">PARAMETERS</span></span>

### <span data-ttu-id="cfd1a-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfd1a-131">-DataFactory</span></span>
<span data-ttu-id="cfd1a-132">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="cfd1a-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cfd1a-133">To polecenie cmdlet pobiera potoki, które należą do fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfd1a-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cfd1a-134">-DataFactoryName</span></span>
<span data-ttu-id="cfd1a-135">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cfd1a-136">To polecenie cmdlet pobiera potoki należące do fabrycznych danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfd1a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd1a-137">-DefaultProfile</span></span>
<span data-ttu-id="cfd1a-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cfd1a-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfd1a-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cfd1a-139">-Name</span></span>
<span data-ttu-id="cfd1a-140">Określa nazwę potoku, o którym mają być informacje.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="cfd1a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd1a-141">-ResourceGroupName</span></span>
<span data-ttu-id="cfd1a-142">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cfd1a-143">To polecenie cmdlet pobiera potoki, które należą do grupy, której parametr określa.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfd1a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd1a-144">CommonParameters</span></span>
<span data-ttu-id="cfd1a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd1a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd1a-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd1a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd1a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfd1a-147">INPUTS</span></span>

### <span data-ttu-id="cfd1a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="cfd1a-148">System.String</span></span>

### <span data-ttu-id="cfd1a-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cfd1a-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="cfd1a-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cfd1a-150">OUTPUTS</span></span>

### <span data-ttu-id="cfd1a-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cfd1a-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="cfd1a-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cfd1a-152">NOTES</span></span>
* <span data-ttu-id="cfd1a-153">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cfd1a-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cfd1a-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfd1a-154">RELATED LINKS</span></span>

[<span data-ttu-id="cfd1a-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cfd1a-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="cfd1a-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cfd1a-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="cfd1a-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cfd1a-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="cfd1a-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="cfd1a-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="cfd1a-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cfd1a-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


