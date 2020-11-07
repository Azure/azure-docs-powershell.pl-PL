---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bce1969ed951f196b1ff2c6d5bcc359ee68bc3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552956"
---
# <span data-ttu-id="5e44c-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e44c-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="5e44c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e44c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e44c-103">Pobiera informacje o rurociągach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5e44c-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e44c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e44c-104">SYNTAX</span></span>

### <span data-ttu-id="5e44c-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e44c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e44c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5e44c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e44c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e44c-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Pipeline -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e44c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e44c-108">DESCRIPTION</span></span>
<span data-ttu-id="5e44c-109">Polecenie cmdlet Get-AzureRmDataFactoryV2Pipeline pobiera informacje o rurociągach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5e44c-109">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="5e44c-110">Jeśli określisz nazwę potoku, to polecenie cmdlet będzie pobierać informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="5e44c-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="5e44c-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich rurociągach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5e44c-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="5e44c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e44c-112">EXAMPLES</span></span>

### <span data-ttu-id="5e44c-113">Przykład 1: uzyskiwanie informacji o wszystkich rurociągach</span><span class="sxs-lookup"><span data-stu-id="5e44c-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="5e44c-114">To polecenie pobiera informacje o wszystkich rurociągach w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5e44c-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="5e44c-115">Możesz użyć jednego z poniższych poleceń przykładowych.</span><span class="sxs-lookup"><span data-stu-id="5e44c-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="5e44c-116">Druga z nich używa obiektu DataFactory jako parametru.</span><span class="sxs-lookup"><span data-stu-id="5e44c-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="5e44c-117">Przykład 2: uzyskiwanie informacji na temat konkretnego procesu</span><span class="sxs-lookup"><span data-stu-id="5e44c-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="5e44c-118">To polecenie pobiera informacje o potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5e44c-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="5e44c-119">Polecenie przekazuje te informacje do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5e44c-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e44c-120">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="5e44c-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="5e44c-121">Aby uzyskać więcej informacji, wpisz Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="5e44c-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="5e44c-122">Przykład 3: uzyskiwanie właściwości dla konkretnego potoku</span><span class="sxs-lookup"><span data-stu-id="5e44c-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="5e44c-123">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości aktywności skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="5e44c-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="5e44c-124">Przykład 6: uzyskiwanie informacji o danych wejściowych dla pierwszej aktywności</span><span class="sxs-lookup"><span data-stu-id="5e44c-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="5e44c-125">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości aktywności skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="5e44c-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="5e44c-126">Polecenie wyświetla właściwość dane wejściowe pierwszego elementu tablicy aktywności przy użyciu polecenia cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="5e44c-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="5e44c-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e44c-127">PARAMETERS</span></span>

### <span data-ttu-id="5e44c-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5e44c-128">-DataFactory</span></span>
<span data-ttu-id="5e44c-129">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="5e44c-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="5e44c-130">To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5e44c-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e44c-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5e44c-131">-DataFactoryName</span></span>
<span data-ttu-id="5e44c-132">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5e44c-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5e44c-133">To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5e44c-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e44c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e44c-134">-DefaultProfile</span></span>
<span data-ttu-id="5e44c-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e44c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e44c-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e44c-136">-Name</span></span>
<span data-ttu-id="5e44c-137">Określa nazwę potoku, w którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="5e44c-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e44c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e44c-138">-ResourceGroupName</span></span>
<span data-ttu-id="5e44c-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e44c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5e44c-140">To polecenie cmdlet umożliwia pobieranie potoków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5e44c-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e44c-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e44c-141">-ResourceId</span></span>
<span data-ttu-id="5e44c-142">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e44c-142">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e44c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e44c-143">CommonParameters</span></span>
<span data-ttu-id="5e44c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e44c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e44c-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e44c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e44c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e44c-146">INPUTS</span></span>

### <span data-ttu-id="5e44c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5e44c-147">System.String</span></span>
<span data-ttu-id="5e44c-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5e44c-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5e44c-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e44c-149">OUTPUTS</span></span>

### <span data-ttu-id="5e44c-150">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5e44c-150">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5e44c-151">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5e44c-151">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="5e44c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e44c-152">NOTES</span></span>
<span data-ttu-id="5e44c-153">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="5e44c-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5e44c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e44c-154">RELATED LINKS</span></span>

[<span data-ttu-id="5e44c-155">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e44c-155">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5e44c-156">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e44c-156">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5e44c-157">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e44c-157">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()