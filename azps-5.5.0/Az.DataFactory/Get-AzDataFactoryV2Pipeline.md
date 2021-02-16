---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188626"
---
# <span data-ttu-id="5f8e7-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f8e7-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="5f8e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8e7-103">Pobiera informacje o potokach w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="5f8e7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f8e7-104">SYNTAX</span></span>

### <span data-ttu-id="5f8e7-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5f8e7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f8e7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5f8e7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f8e7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f8e7-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f8e7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f8e7-108">DESCRIPTION</span></span>
<span data-ttu-id="5f8e7-109">Polecenie Get-AzDataFactoryV2Pipeline pobiera informacje o potokach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="5f8e7-110">Jeśli określisz nazwę potoku, to polecenie cmdlet pobiera informacje o tym potoku.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="5f8e7-111">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich potokach w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="5f8e7-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f8e7-112">EXAMPLES</span></span>

### <span data-ttu-id="5f8e7-113">Przykład 1. Uzyskiwanie informacji o wszystkich potokach</span><span class="sxs-lookup"><span data-stu-id="5f8e7-113">Example 1: Get information about all pipelines</span></span>
```powershell
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

<span data-ttu-id="5f8e7-114">To polecenie pobiera informacje o wszystkich potokach w fabrycznej układzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="5f8e7-115">Możesz użyć jednego z poniższych poleceń przykładowych.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="5f8e7-116">Drugi parametr używa jako parametru obiektu DataFactory.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="5f8e7-117">Przykład 2. Uzyskiwanie informacji o określonym potoku</span><span class="sxs-lookup"><span data-stu-id="5f8e7-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="5f8e7-118">To polecenie pobiera informacje o potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="5f8e7-119">Polecenie przekazuje te informacje do Format-List cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5f8e7-120">Polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="5f8e7-121">Aby uzyskać więcej informacji, wpisz Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="5f8e7-122">Przykład 3. Uzyskiwanie właściwości określonego potoku</span><span class="sxs-lookup"><span data-stu-id="5f8e7-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
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

<span data-ttu-id="5f8e7-123">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="5f8e7-124">Przykład 4. Uzyskiwanie informacji o danych wejściowych pierwszego działania</span><span class="sxs-lookup"><span data-stu-id="5f8e7-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="5f8e7-125">To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="5f8e7-126">To polecenie wyświetla właściwość Inputs pierwszego elementu tablicy Activities (Działania) za pomocą Format-List cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="5f8e7-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f8e7-127">PARAMETERS</span></span>

### <span data-ttu-id="5f8e7-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5f8e7-128">-DataFactory</span></span>
<span data-ttu-id="5f8e7-129">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="5f8e7-130">To polecenie cmdlet pobiera potoki, które należą do fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f8e7-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f8e7-131">-DataFactoryName</span></span>
<span data-ttu-id="5f8e7-132">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5f8e7-133">To polecenie cmdlet pobiera potoki, które należą do fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f8e7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8e7-134">-DefaultProfile</span></span>
<span data-ttu-id="5f8e7-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f8e7-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5f8e7-136">-Name</span></span>
<span data-ttu-id="5f8e7-137">Określa nazwę potoku, o którym mają być informacje.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="5f8e7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8e7-138">-ResourceGroupName</span></span>
<span data-ttu-id="5f8e7-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5f8e7-140">To polecenie cmdlet pobiera potoki, które należą do grupy, której parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f8e7-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f8e7-141">-ResourceId</span></span>
<span data-ttu-id="5f8e7-142">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5f8e7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8e7-143">CommonParameters</span></span>
<span data-ttu-id="5f8e7-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8e7-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8e7-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8e7-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f8e7-146">INPUTS</span></span>

### <span data-ttu-id="5f8e7-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5f8e7-147">System.String</span></span>

### <span data-ttu-id="5f8e7-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5f8e7-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5f8e7-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f8e7-149">OUTPUTS</span></span>

### <span data-ttu-id="5f8e7-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="5f8e7-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="5f8e7-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f8e7-151">NOTES</span></span>
<span data-ttu-id="5f8e7-152">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="5f8e7-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5f8e7-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f8e7-153">RELATED LINKS</span></span>

[<span data-ttu-id="5f8e7-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f8e7-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5f8e7-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f8e7-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="5f8e7-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="5f8e7-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
