---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8ee5ba855e1c9f9815e9dbcb844ebb23d7118d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527674"
---
# <span data-ttu-id="ac9d1-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ac9d1-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ac9d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9d1-103">Pobiera informacje o usługach połączonych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac9d1-104">SYNTAX</span></span>

### <span data-ttu-id="ac9d1-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ac9d1-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac9d1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ac9d1-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9d1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ac9d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ac9d1-108">Polecenie cmdlet Get-AzureRmDataFactoryV2LinkedService pobiera informacje o usługach połączonych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="ac9d1-109">Jeśli określisz nazwę połączonej usługi, to polecenie cmdlet będzie pobierać informacje dotyczące tej połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="ac9d1-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich usług połączonych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="ac9d1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac9d1-111">EXAMPLES</span></span>

### <span data-ttu-id="ac9d1-112">Przykład 1: uzyskiwanie informacji o wszystkich usługach połączonych</span><span class="sxs-lookup"><span data-stu-id="ac9d1-112">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="ac9d1-113">To polecenie pobiera informacje dotyczące wszystkich usług połączonych w fabryce danych o nazwie WikiADF, a następnie przekazuje połączone usługi do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac9d1-114">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ac9d1-115">Aby uzyskać więcej informacji, wpisz Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="ac9d1-116">Możesz użyć jednego z następujących sposobów:</span><span class="sxs-lookup"><span data-stu-id="ac9d1-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="ac9d1-117">Przykład 2: uzyskiwanie informacji o konkretnej połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="ac9d1-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="ac9d1-118">To polecenie pobiera informacje o połączonej usłudze o nazwie LinkedServiceCuratedWikiData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="ac9d1-119">Przykład 3: uzyskiwanie informacji o konkretnej połączonej usłudze przez określenie parametru DataFactory</span><span class="sxs-lookup"><span data-stu-id="ac9d1-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="ac9d1-120">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmDataFactoryV2, aby uzyskać fabrykę danych o nazwie ContosoFactory, a następnie przechowywać ją w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="ac9d1-121">Drugie polecenie pobiera informacje o połączonej usłudze dla fabryki danych przechowywanej w $DataFactory, a następnie przekazuje te informacje do polecenia cmdlet Format-Table za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac9d1-122">Polecenie cmdlet Format-Table formatuje dane wyjściowe jako zestaw danych o określonych właściwościach jako kolumny zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="ac9d1-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac9d1-123">PARAMETERS</span></span>

### <span data-ttu-id="ac9d1-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ac9d1-124">-DataFactory</span></span>
<span data-ttu-id="ac9d1-125">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="ac9d1-126">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac9d1-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ac9d1-127">-DataFactoryName</span></span>
<span data-ttu-id="ac9d1-128">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ac9d1-129">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac9d1-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac9d1-130">-Name</span></span>
<span data-ttu-id="ac9d1-131">Określa nazwę połączonej usługi, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9d1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9d1-132">-ResourceGroupName</span></span>
<span data-ttu-id="ac9d1-133">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac9d1-134">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac9d1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9d1-135">-DefaultProfile</span></span>
<span data-ttu-id="ac9d1-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9d1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9d1-137">CommonParameters</span></span>
<span data-ttu-id="ac9d1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9d1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9d1-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9d1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9d1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac9d1-140">INPUTS</span></span>

### <span data-ttu-id="ac9d1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ac9d1-141">System.String</span></span>
<span data-ttu-id="ac9d1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac9d1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ac9d1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac9d1-143">OUTPUTS</span></span>

### <span data-ttu-id="ac9d1-144">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ac9d1-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ac9d1-145">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ac9d1-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="ac9d1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac9d1-146">NOTES</span></span>
<span data-ttu-id="ac9d1-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="ac9d1-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac9d1-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac9d1-148">RELATED LINKS</span></span>

[<span data-ttu-id="ac9d1-149">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ac9d1-149">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ac9d1-150">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ac9d1-150">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
