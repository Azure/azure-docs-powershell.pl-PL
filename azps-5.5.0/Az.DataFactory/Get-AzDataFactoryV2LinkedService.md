---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188643"
---
# <span data-ttu-id="379ec-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="379ec-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="379ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379ec-102">SYNOPSIS</span></span>
<span data-ttu-id="379ec-103">Pobiera informacje o połączonych usługach w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="379ec-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="379ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="379ec-104">SYNTAX</span></span>

### <span data-ttu-id="379ec-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="379ec-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="379ec-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="379ec-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="379ec-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="379ec-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="379ec-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="379ec-108">DESCRIPTION</span></span>
<span data-ttu-id="379ec-109">Polecenie Get-AzDataFactoryV2LinkedService pobiera informacje o usługach połączonych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="379ec-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="379ec-110">Jeśli określisz nazwę usługi połączonej, to polecenie cmdlet pobiera informacje o tej połączonej usłudze.</span><span class="sxs-lookup"><span data-stu-id="379ec-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="379ec-111">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich połączonych usługach w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="379ec-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="379ec-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="379ec-112">EXAMPLES</span></span>

### <span data-ttu-id="379ec-113">Przykład 1. Uzyskiwanie informacji o wszystkich połączonych usługach</span><span class="sxs-lookup"><span data-stu-id="379ec-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="379ec-114">To polecenie pobiera informacje o wszystkich połączonych usługach w zakładzie danych o nazwie WikiADF, Format-List następnie przekazuje połączone usługi do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="379ec-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="379ec-115">Polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="379ec-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="379ec-116">Aby uzyskać więcej informacji, wpisz Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="379ec-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="379ec-117">Możesz skorzystać z jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="379ec-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="379ec-118">Przykład 2. Uzyskiwanie informacji o konkretnej połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="379ec-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="379ec-119">To polecenie pobiera informacje o połączonej usłudze o nazwie LinkedServiceCuratedWikiData w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="379ec-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="379ec-120">Przykład 3. Uzyskiwanie informacji o określonej połączonej usłudze przez określenie parametru DataFactory</span><span class="sxs-lookup"><span data-stu-id="379ec-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="379ec-121">Pierwsze polecenie używa Get-AzDataFactoryV2 cmdlet w celu uzyskania bazy danych o nazwie ContosoFactory, a następnie zapisuje ją w $DataFactory danych.</span><span class="sxs-lookup"><span data-stu-id="379ec-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="379ec-122">Drugie polecenie pobiera informacje o połączonej usłudze dla fabrycznych danych przechowywanych w usłudze $DataFactory, Format-Table następnie przekazuje te informacje do polecenia cmdlet Format-Table przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="379ec-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="379ec-123">Polecenie Format-Table formatuje dane wyjściowe jako zestaw danych o określonych właściwościach jako kolumny zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="379ec-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="379ec-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="379ec-124">PARAMETERS</span></span>

### <span data-ttu-id="379ec-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="379ec-125">-DataFactory</span></span>
<span data-ttu-id="379ec-126">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="379ec-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="379ec-127">To polecenie cmdlet pobiera usługi połączone, które należą do fabrycznej usługi danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="379ec-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="379ec-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="379ec-128">-DataFactoryName</span></span>
<span data-ttu-id="379ec-129">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="379ec-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="379ec-130">To polecenie cmdlet pobiera usługi połączone, które należą do fabrycznej usługi danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="379ec-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="379ec-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379ec-131">-DefaultProfile</span></span>
<span data-ttu-id="379ec-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="379ec-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="379ec-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="379ec-133">-Name</span></span>
<span data-ttu-id="379ec-134">Określa nazwę połączonej usługi, o której mają być uzyskiwanie informacji.</span><span class="sxs-lookup"><span data-stu-id="379ec-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379ec-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379ec-135">-ResourceGroupName</span></span>
<span data-ttu-id="379ec-136">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="379ec-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="379ec-137">To polecenie cmdlet pobiera usługi połączone, które należą do grupy, której parametr określa.</span><span class="sxs-lookup"><span data-stu-id="379ec-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="379ec-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="379ec-138">-ResourceId</span></span>
<span data-ttu-id="379ec-139">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="379ec-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="379ec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379ec-140">CommonParameters</span></span>
<span data-ttu-id="379ec-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379ec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379ec-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="379ec-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379ec-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="379ec-143">INPUTS</span></span>

### <span data-ttu-id="379ec-144">System.String</span><span class="sxs-lookup"><span data-stu-id="379ec-144">System.String</span></span>

### <span data-ttu-id="379ec-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="379ec-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="379ec-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="379ec-146">OUTPUTS</span></span>

### <span data-ttu-id="379ec-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="379ec-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="379ec-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="379ec-148">NOTES</span></span>
<span data-ttu-id="379ec-149">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="379ec-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="379ec-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="379ec-150">RELATED LINKS</span></span>

[<span data-ttu-id="379ec-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="379ec-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="379ec-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="379ec-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
