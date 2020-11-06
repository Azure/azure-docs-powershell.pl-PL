---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 0898b65c0a124b278d0878ac1749e955011e1dab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525541"
---
# <span data-ttu-id="d6341-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d6341-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="d6341-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6341-102">SYNOPSIS</span></span>
<span data-ttu-id="d6341-103">Pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d6341-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6341-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6341-104">SYNTAX</span></span>

### <span data-ttu-id="d6341-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6341-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6341-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d6341-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6341-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6341-107">DESCRIPTION</span></span>
<span data-ttu-id="d6341-108">Polecenie cmdlet **Get-AzureRmDataFactoryDataset** pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d6341-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="d6341-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="d6341-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="d6341-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="d6341-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="d6341-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6341-111">EXAMPLES</span></span>

### <span data-ttu-id="d6341-112">Przykład 1: uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="d6341-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="d6341-113">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d6341-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="d6341-114">Przykład 2: uzyskiwanie informacji na temat konkretnego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="d6341-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="d6341-115">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d6341-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="d6341-116">Przykład 3: Uzyskiwanie lokalizacji dla określonego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="d6341-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="d6341-117">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego do wyświetlania **lokalizacji** skojarzonej z tym zestawem danych.</span><span class="sxs-lookup"><span data-stu-id="d6341-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="d6341-118">Możesz też przypisać dane wyjściowe polecenia cmdlet **Get-AzureRmDataFactoryDataset** do zmiennej, a następnie za pomocą notacji kropkowej wyświetlić Właściwość lokalizacji skojarzoną z obiektem zestawu danych przechowywanym w tej zmiennej.</span><span class="sxs-lookup"><span data-stu-id="d6341-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="d6341-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6341-119">PARAMETERS</span></span>

### <span data-ttu-id="d6341-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6341-120">-DataFactory</span></span>
<span data-ttu-id="d6341-121">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d6341-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d6341-122">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d6341-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6341-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d6341-123">-DataFactoryName</span></span>
<span data-ttu-id="d6341-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d6341-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d6341-125">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d6341-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6341-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6341-126">-Name</span></span>
<span data-ttu-id="d6341-127">Określa nazwę zestawu danych, w którym ten aplet polecenia pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="d6341-127">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6341-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6341-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6341-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6341-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d6341-130">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d6341-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6341-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6341-131">-DefaultProfile</span></span>
<span data-ttu-id="d6341-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6341-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6341-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6341-133">CommonParameters</span></span>
<span data-ttu-id="d6341-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6341-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6341-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6341-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6341-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6341-136">INPUTS</span></span>

## <span data-ttu-id="d6341-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6341-137">OUTPUTS</span></span>

### <span data-ttu-id="d6341-138">System. Collections. Generic. list "1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft. platformy windowsazure. Commands. Commands, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="d6341-138">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="d6341-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6341-139">NOTES</span></span>
* <span data-ttu-id="d6341-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="d6341-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d6341-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6341-141">RELATED LINKS</span></span>

[<span data-ttu-id="d6341-142">Nowe — AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d6341-142">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="d6341-143">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d6341-143">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


