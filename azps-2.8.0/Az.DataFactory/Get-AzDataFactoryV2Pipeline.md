---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: bbcc33eee2932eed984f4cf06cfc09a79a1357af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706020"
---
# <span data-ttu-id="5f034-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f034-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="5f034-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f034-102">SYNOPSIS</span></span>
<span data-ttu-id="5f034-103">Pobiera informacje o rurociągach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5f034-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="5f034-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f034-104">SYNTAX</span></span>

### <span data-ttu-id="5f034-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f034-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f034-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5f034-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f034-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f034-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f034-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5f034-108">DESCRIPTION</span></span>
<span data-ttu-id="5f034-109">Polecenie cmdlet Get-AzDataFactoryV2Pipeline pobiera informacje o rurociągach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5f034-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="5f034-110">Jeśli określisz nazwę potoku, to polecenie cmdlet będzie pobierać informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="5f034-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="5f034-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich rurociągach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5f034-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="5f034-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f034-112">EXAMPLES</span></span>

### <span data-ttu-id="5f034-113">Przykład 1: uzyskiwanie informacji o wszystkich rurociągach</span><span class="sxs-lookup"><span data-stu-id="5f034-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="5f034-114">To polecenie pobiera informacje o wszystkich rurociągach w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5f034-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="5f034-115">Możesz użyć jednego z poniższych poleceń przykładowych.</span><span class="sxs-lookup"><span data-stu-id="5f034-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="5f034-116">Druga z nich używa obiektu DataFactory jako parametru.</span><span class="sxs-lookup"><span data-stu-id="5f034-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="5f034-117">Przykład 2: uzyskiwanie informacji na temat konkretnego procesu</span><span class="sxs-lookup"><span data-stu-id="5f034-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="5f034-118">To polecenie pobiera informacje o potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5f034-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="5f034-119">Polecenie przekazuje te informacje do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5f034-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5f034-120">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="5f034-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="5f034-121">Aby uzyskać więcej informacji, wpisz Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="5f034-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="5f034-122">Przykład 3: uzyskiwanie właściwości dla konkretnego potoku</span><span class="sxs-lookup"><span data-stu-id="5f034-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

<span data-ttu-id="5f034-123">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości aktywności skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="5f034-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="5f034-124">Przykład 6: uzyskiwanie informacji o danych wejściowych dla pierwszej aktywności</span><span class="sxs-lookup"><span data-stu-id="5f034-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="5f034-125">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości aktywności skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="5f034-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="5f034-126">Polecenie wyświetla właściwość dane wejściowe pierwszego elementu tablicy aktywności przy użyciu polecenia cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="5f034-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="5f034-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f034-127">PARAMETERS</span></span>

### <span data-ttu-id="5f034-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5f034-128">-DataFactory</span></span>
<span data-ttu-id="5f034-129">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="5f034-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="5f034-130">To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5f034-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f034-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5f034-131">-DataFactoryName</span></span>
<span data-ttu-id="5f034-132">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5f034-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5f034-133">To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5f034-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f034-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f034-134">-DefaultProfile</span></span>
<span data-ttu-id="5f034-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f034-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f034-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f034-136">-Name</span></span>
<span data-ttu-id="5f034-137">Określa nazwę potoku, w którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="5f034-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f034-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f034-138">-ResourceGroupName</span></span>
<span data-ttu-id="5f034-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f034-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5f034-140">To polecenie cmdlet umożliwia pobieranie potoków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5f034-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f034-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f034-141">-ResourceId</span></span>
<span data-ttu-id="5f034-142">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f034-142">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f034-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f034-143">CommonParameters</span></span>
<span data-ttu-id="5f034-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f034-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f034-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f034-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f034-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f034-146">INPUTS</span></span>

### <span data-ttu-id="5f034-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5f034-147">System.String</span></span>

### <span data-ttu-id="5f034-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5f034-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5f034-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f034-149">OUTPUTS</span></span>

### <span data-ttu-id="5f034-150">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5f034-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="5f034-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f034-151">NOTES</span></span>
<span data-ttu-id="5f034-152">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="5f034-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5f034-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f034-153">RELATED LINKS</span></span>

[<span data-ttu-id="5f034-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f034-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5f034-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f034-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5f034-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f034-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()