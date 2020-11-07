---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: a54cdb0a30d0249ccb8fd177646e218e0fe604c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868776"
---
# <span data-ttu-id="77f76-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="77f76-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="77f76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77f76-102">SYNOPSIS</span></span>
<span data-ttu-id="77f76-103">Pobiera informacje o usługach połączonych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="77f76-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="77f76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77f76-104">SYNTAX</span></span>

### <span data-ttu-id="77f76-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77f76-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77f76-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="77f76-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77f76-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77f76-107">DESCRIPTION</span></span>
<span data-ttu-id="77f76-108">Polecenie cmdlet **Get-AzDataFactoryLinkedService** pobiera informacje o usługach połączonych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="77f76-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="77f76-109">Jeśli określisz nazwę połączonej usługi, to polecenie cmdlet będzie pobierać informacje dotyczące tej połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="77f76-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="77f76-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich usług połączonych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="77f76-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="77f76-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77f76-111">EXAMPLES</span></span>

### <span data-ttu-id="77f76-112">Przykład 1: uzyskiwanie informacji o wszystkich usługach połączonych</span><span class="sxs-lookup"><span data-stu-id="77f76-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="77f76-113">To polecenie pobiera informacje dotyczące wszystkich usług połączonych w fabryce danych o nazwie WikiADF, a następnie przekazuje połączone usługi do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="77f76-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="77f76-114">Ten aplet polecenia sformatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="77f76-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="77f76-115">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="77f76-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="77f76-116">Przykład 2: uzyskiwanie informacji o konkretnej połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="77f76-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="77f76-117">To polecenie pobiera informacje o połączonej usłudze o nazwie HDILinkedService w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="77f76-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="77f76-118">Przykład 3: uzyskiwanie informacji o konkretnej połączonej usłudze przez określenie parametru DataFactory</span><span class="sxs-lookup"><span data-stu-id="77f76-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="77f76-119">Pierwsze polecenie używa polecenia cmdlet Get-AzDataFactory, aby uzyskać fabrykę danych o nazwie ContosoFactory, a następnie przechowywać ją w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="77f76-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="77f76-120">Drugie polecenie pobiera informacje o połączonej usłudze dla fabryki danych przechowywanej w $DataFactory, a następnie przekazuje te informacje do polecenia cmdlet Format-Table za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="77f76-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="77f76-121">**Format — tabela formatowanie** danych wyjściowych jako zestawu danych o określonych właściwościach jako kolumn zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="77f76-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="77f76-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77f76-122">PARAMETERS</span></span>

### <span data-ttu-id="77f76-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="77f76-123">-DataFactory</span></span>
<span data-ttu-id="77f76-124">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="77f76-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="77f76-125">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="77f76-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="77f76-126">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="77f76-126">-DataFactoryName</span></span>
<span data-ttu-id="77f76-127">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="77f76-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="77f76-128">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="77f76-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="77f76-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f76-129">-DefaultProfile</span></span>
<span data-ttu-id="77f76-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="77f76-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77f76-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77f76-131">-Name</span></span>
<span data-ttu-id="77f76-132">Określa nazwę połączonej usługi, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="77f76-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="77f76-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f76-133">-ResourceGroupName</span></span>
<span data-ttu-id="77f76-134">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77f76-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="77f76-135">To polecenie cmdlet umożliwia pobieranie połączonych usług należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="77f76-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="77f76-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f76-136">CommonParameters</span></span>
<span data-ttu-id="77f76-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f76-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f76-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f76-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f76-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77f76-139">INPUTS</span></span>

### <span data-ttu-id="77f76-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="77f76-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="77f76-141">System. String</span><span class="sxs-lookup"><span data-stu-id="77f76-141">System.String</span></span>

## <span data-ttu-id="77f76-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77f76-142">OUTPUTS</span></span>

### <span data-ttu-id="77f76-143">Microsoft. Azure. Commands. datafactors. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="77f76-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="77f76-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77f76-144">NOTES</span></span>
* <span data-ttu-id="77f76-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="77f76-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="77f76-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77f76-146">RELATED LINKS</span></span>

[<span data-ttu-id="77f76-147">Nowe — AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="77f76-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="77f76-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="77f76-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


