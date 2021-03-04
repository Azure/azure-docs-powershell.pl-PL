---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975409"
---
# <span data-ttu-id="80428-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="80428-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="80428-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80428-102">SYNOPSIS</span></span>
<span data-ttu-id="80428-103">Pobiera informacje o potokach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="80428-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="80428-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80428-104">SYNTAX</span></span>

### <span data-ttu-id="80428-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="80428-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80428-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="80428-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80428-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="80428-107">DESCRIPTION</span></span>
<span data-ttu-id="80428-108">Polecenie **cmdlet Get-AzDataFactoryPipeline** pobiera informacje o potokach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="80428-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="80428-109">Jeśli określisz nazwę potoku, to polecenie cmdlet pobiera informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="80428-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="80428-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich potokach w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="80428-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="80428-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80428-111">EXAMPLES</span></span>

### <span data-ttu-id="80428-112">Przykład 1. Uzyskiwanie informacji o wszystkich potokach</span><span class="sxs-lookup"><span data-stu-id="80428-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="80428-113">To polecenie pobiera informacje o wszystkich potokach w fabrycznej układzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="80428-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="80428-114">Możesz użyć jednego z poniższych poleceń przykładowych.</span><span class="sxs-lookup"><span data-stu-id="80428-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="80428-115">Drugi obiekt korzysta z **obiektu DataFactory** jako parametru.</span><span class="sxs-lookup"><span data-stu-id="80428-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="80428-116">Przykład 2. Uzyskiwanie informacji o określonym potoku</span><span class="sxs-lookup"><span data-stu-id="80428-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="80428-117">To polecenie pobiera informacje o potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="80428-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="80428-118">Polecenie przekazuje te informacje do Format-List cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="80428-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80428-119">To polecenie cmdlet s formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="80428-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="80428-120">Aby uzyskać więcej informacji, wpisz `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="80428-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="80428-121">Przykład 3. Uzyskiwanie właściwości określonego potoku</span><span class="sxs-lookup"><span data-stu-id="80428-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="80428-122">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości **Properties** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="80428-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="80428-123">Przykład 4. Uzyskiwanie działań dla określonego potoku</span><span class="sxs-lookup"><span data-stu-id="80428-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="80428-124">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie  WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="80428-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="80428-125">Przykład 5. Uzyskiwanie informacji dotyczących środowiska uruchomieniowego dla określonego potoku</span><span class="sxs-lookup"><span data-stu-id="80428-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="80428-126">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości **RuntimeInfo** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="80428-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="80428-127">Przykład 6. Uzyskiwanie informacji o danych wejściowych dla pierwszego działania</span><span class="sxs-lookup"><span data-stu-id="80428-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="80428-128">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie  WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="80428-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="80428-129">Polecenie wyświetla właściwość **Dane wejściowe** pierwszego elementu tablicy Działania **przy** użyciu opcji **Format-Lista.**</span><span class="sxs-lookup"><span data-stu-id="80428-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="80428-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80428-130">PARAMETERS</span></span>

### <span data-ttu-id="80428-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="80428-131">-DataFactory</span></span>
<span data-ttu-id="80428-132">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="80428-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="80428-133">To polecenie cmdlet pobiera potoki należące do fabrycznych danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="80428-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="80428-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="80428-134">-DataFactoryName</span></span>
<span data-ttu-id="80428-135">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="80428-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="80428-136">To polecenie cmdlet pobiera potoki należące do fabrycznych danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="80428-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="80428-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80428-137">-DefaultProfile</span></span>
<span data-ttu-id="80428-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="80428-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80428-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80428-139">-Name</span></span>
<span data-ttu-id="80428-140">Określa nazwę potoku, o którym mają być informacje.</span><span class="sxs-lookup"><span data-stu-id="80428-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="80428-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80428-141">-ResourceGroupName</span></span>
<span data-ttu-id="80428-142">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80428-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="80428-143">To polecenie cmdlet pobiera potoki, które należą do grupy, której parametr określa.</span><span class="sxs-lookup"><span data-stu-id="80428-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="80428-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80428-144">CommonParameters</span></span>
<span data-ttu-id="80428-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80428-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80428-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80428-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80428-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80428-147">INPUTS</span></span>

### <span data-ttu-id="80428-148">System.String</span><span class="sxs-lookup"><span data-stu-id="80428-148">System.String</span></span>

### <span data-ttu-id="80428-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="80428-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="80428-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80428-150">OUTPUTS</span></span>

### <span data-ttu-id="80428-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="80428-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="80428-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80428-152">NOTES</span></span>
* <span data-ttu-id="80428-153">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="80428-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="80428-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80428-154">RELATED LINKS</span></span>

[<span data-ttu-id="80428-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="80428-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="80428-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="80428-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="80428-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="80428-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="80428-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="80428-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="80428-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="80428-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


