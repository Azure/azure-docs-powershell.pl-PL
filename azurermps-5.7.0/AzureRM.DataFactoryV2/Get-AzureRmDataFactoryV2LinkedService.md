---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a9b718ab72435ac96c25847896a7c73718a16a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716624"
---
# <span data-ttu-id="cbcb9-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="cbcb9-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="cbcb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcb9-103">Pobiera informacje o usługach połączonych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbcb9-104">SYNTAX</span></span>

### <span data-ttu-id="cbcb9-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cbcb9-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcb9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cbcb9-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcb9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbcb9-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2LinkedService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbcb9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cbcb9-108">DESCRIPTION</span></span>
<span data-ttu-id="cbcb9-109">Polecenie cmdlet Get-AzureRmDataFactoryV2LinkedService pobiera informacje o usługach połączonych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-109">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="cbcb9-110">Jeśli określisz nazwę połączonej usługi, to polecenie cmdlet będzie pobierać informacje dotyczące tej połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="cbcb9-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich usług połączonych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="cbcb9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbcb9-112">EXAMPLES</span></span>

### <span data-ttu-id="cbcb9-113">Przykład 1: uzyskiwanie informacji o wszystkich usługach połączonych</span><span class="sxs-lookup"><span data-stu-id="cbcb9-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="cbcb9-114">To polecenie pobiera informacje dotyczące wszystkich usług połączonych w fabryce danych o nazwie WikiADF, a następnie przekazuje połączone usługi do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cbcb9-115">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="cbcb9-116">Aby uzyskać więcej informacji, wpisz Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-116">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="cbcb9-117">Możesz użyć jednego z następujących sposobów:</span><span class="sxs-lookup"><span data-stu-id="cbcb9-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="cbcb9-118">Przykład 2: uzyskiwanie informacji o konkretnej połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="cbcb9-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="cbcb9-119">To polecenie pobiera informacje o połączonej usłudze o nazwie LinkedServiceCuratedWikiData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="cbcb9-120">Przykład 3: uzyskiwanie informacji o konkretnej połączonej usłudze przez określenie parametru DataFactory</span><span class="sxs-lookup"><span data-stu-id="cbcb9-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="cbcb9-121">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmDataFactoryV2, aby uzyskać fabrykę danych o nazwie ContosoFactory, a następnie przechowywać ją w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-121">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="cbcb9-122">Drugie polecenie pobiera informacje o połączonej usłudze dla fabryki danych przechowywanej w $DataFactory, a następnie przekazuje te informacje do polecenia cmdlet Format-Table za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cbcb9-123">Polecenie cmdlet Format-Table formatuje dane wyjściowe jako zestaw danych o określonych właściwościach jako kolumny zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="cbcb9-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbcb9-124">PARAMETERS</span></span>

### <span data-ttu-id="cbcb9-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cbcb9-125">-DataFactory</span></span>
<span data-ttu-id="cbcb9-126">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="cbcb9-127">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbcb9-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cbcb9-128">-DataFactoryName</span></span>
<span data-ttu-id="cbcb9-129">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cbcb9-130">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbcb9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcb9-131">-DefaultProfile</span></span>
<span data-ttu-id="cbcb9-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcb9-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cbcb9-133">-Name</span></span>
<span data-ttu-id="cbcb9-134">Określa nazwę połączonej usługi, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcb9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcb9-135">-ResourceGroupName</span></span>
<span data-ttu-id="cbcb9-136">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cbcb9-137">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbcb9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbcb9-138">-ResourceId</span></span>
<span data-ttu-id="cbcb9-139">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cbcb9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcb9-140">CommonParameters</span></span>
<span data-ttu-id="cbcb9-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcb9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcb9-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcb9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcb9-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbcb9-143">INPUTS</span></span>

### <span data-ttu-id="cbcb9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cbcb9-144">System.String</span></span>
<span data-ttu-id="cbcb9-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cbcb9-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cbcb9-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbcb9-146">OUTPUTS</span></span>

### <span data-ttu-id="cbcb9-147">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cbcb9-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="cbcb9-148">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="cbcb9-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="cbcb9-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbcb9-149">NOTES</span></span>
<span data-ttu-id="cbcb9-150">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cbcb9-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cbcb9-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbcb9-151">RELATED LINKS</span></span>

[<span data-ttu-id="cbcb9-152">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="cbcb9-152">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="cbcb9-153">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="cbcb9-153">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
