---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062823"
---
# <span data-ttu-id="1d9d8-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1d9d8-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="1d9d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9d8-103">Pobiera informacje o rurociągach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="1d9d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d9d8-104">SYNTAX</span></span>

### <span data-ttu-id="1d9d8-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d9d8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d9d8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1d9d8-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9d8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d9d8-107">DESCRIPTION</span></span>
<span data-ttu-id="1d9d8-108">Polecenie cmdlet **Get-AzDataFactoryPipeline** pobiera informacje o rurociągach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="1d9d8-109">Jeśli określisz nazwę potoku, to polecenie cmdlet będzie pobierać informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="1d9d8-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich rurociągach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="1d9d8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d9d8-111">EXAMPLES</span></span>

### <span data-ttu-id="1d9d8-112">Przykład 1: uzyskiwanie informacji o wszystkich rurociągach</span><span class="sxs-lookup"><span data-stu-id="1d9d8-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="1d9d8-113">To polecenie pobiera informacje o wszystkich rurociągach w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="1d9d8-114">Możesz wykonać jedną z następujących przykładowych poleceń.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="1d9d8-115">Druga z nich używa obiektu **DataFactory** jako parametru.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="1d9d8-116">Przykład 2: uzyskiwanie informacji na temat konkretnego procesu</span><span class="sxs-lookup"><span data-stu-id="1d9d8-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="1d9d8-117">To polecenie pobiera informacje o potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="1d9d8-118">Polecenie przekazuje te informacje do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d9d8-119">Ten aplet polecenia sformatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="1d9d8-120">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="1d9d8-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="1d9d8-121">Przykład 3: uzyskiwanie właściwości dla konkretnego potoku</span><span class="sxs-lookup"><span data-stu-id="1d9d8-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="1d9d8-122">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości **Właściwości** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="1d9d8-123">Przykład 4: uzyskiwanie działań dla konkretnego procesu</span><span class="sxs-lookup"><span data-stu-id="1d9d8-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="1d9d8-124">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości **aktywności** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="1d9d8-125">Przykład 5: uzyskiwanie informacji o czasie wykonywania dla konkretnego procesu</span><span class="sxs-lookup"><span data-stu-id="1d9d8-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="1d9d8-126">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości **RuntimeInfo** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="1d9d8-127">Przykład 6: uzyskiwanie informacji o danych wejściowych dla pierwszej aktywności</span><span class="sxs-lookup"><span data-stu-id="1d9d8-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="1d9d8-128">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości **aktywności** skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="1d9d8-129">Polecenie wyświetla Właściwość **dane wejściowe** pierwszego elementu tablicy **aktywności** , korzystając z **listy format**.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="1d9d8-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d9d8-130">PARAMETERS</span></span>

### <span data-ttu-id="1d9d8-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d9d8-131">-DataFactory</span></span>
<span data-ttu-id="1d9d8-132">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="1d9d8-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1d9d8-133">To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d9d8-134">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1d9d8-134">-DataFactoryName</span></span>
<span data-ttu-id="1d9d8-135">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1d9d8-136">To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d9d8-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9d8-137">-DefaultProfile</span></span>
<span data-ttu-id="1d9d8-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1d9d8-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d9d8-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d9d8-139">-Name</span></span>
<span data-ttu-id="1d9d8-140">Określa nazwę potoku, w którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="1d9d8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d9d8-141">-ResourceGroupName</span></span>
<span data-ttu-id="1d9d8-142">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1d9d8-143">To polecenie cmdlet umożliwia pobieranie potoków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d9d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9d8-144">CommonParameters</span></span>
<span data-ttu-id="1d9d8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9d8-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9d8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9d8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d9d8-147">INPUTS</span></span>

### <span data-ttu-id="1d9d8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9d8-148">System.String</span></span>

### <span data-ttu-id="1d9d8-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1d9d8-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1d9d8-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d9d8-150">OUTPUTS</span></span>

### <span data-ttu-id="1d9d8-151">Microsoft. Azure. Commands. datafactors. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1d9d8-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="1d9d8-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d9d8-152">NOTES</span></span>
* <span data-ttu-id="1d9d8-153">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1d9d8-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1d9d8-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d9d8-154">RELATED LINKS</span></span>

[<span data-ttu-id="1d9d8-155">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1d9d8-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="1d9d8-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1d9d8-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="1d9d8-157">Życiorys — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1d9d8-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="1d9d8-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1d9d8-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1d9d8-159">Suspend — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1d9d8-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


