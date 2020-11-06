---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548287"
---
# <span data-ttu-id="0e3f2-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0e3f2-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="0e3f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3f2-103">Pobiera informacje o fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e3f2-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="0e3f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e3f2-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3f2-106">Polecenie cmdlet Get-AzureRmDataFactoryV2 pobiera informacje na temat fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="0e3f2-107">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet będzie pobierać informacje na temat fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="0e3f2-108">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="0e3f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e3f2-109">EXAMPLES</span></span>

### <span data-ttu-id="0e3f2-110">Przykład 1: pobieranie wszystkich fabryk danych</span><span class="sxs-lookup"><span data-stu-id="0e3f2-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="0e3f2-111">Wyświetla informacje dotyczące wszystkich fabryk danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="0e3f2-112">Przykład 2: uzyskiwanie określonej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="0e3f2-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="0e3f2-113">To polecenie wyświetla informacje o fabryce danych o nazwie WikiADF w subskrypcji grupy zasobów o nazwie ADF, a następnie zapisuje je w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="0e3f2-114">Określ parametr DataFactory w kolejnych poleceniach cmdlet, aby użyć fabryki danych przechowywanej w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="0e3f2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e3f2-115">PARAMETERS</span></span>

### <span data-ttu-id="0e3f2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e3f2-116">-Name</span></span>
<span data-ttu-id="0e3f2-117">Określa nazwę fabryki danych, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e3f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e3f2-119">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0e3f2-120">To polecenie cmdlet umożliwia pobieranie informacji na temat fabryk danych należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0e3f2-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="0e3f2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e3f2-121">INPUTS</span></span>

### <span data-ttu-id="0e3f2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0e3f2-122">System.String</span></span>


## <span data-ttu-id="0e3f2-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e3f2-123">OUTPUTS</span></span>

### <span data-ttu-id="0e3f2-124">System. Collections. Generic. list "1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0e3f2-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0e3f2-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0e3f2-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="0e3f2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e3f2-126">NOTES</span></span>
<span data-ttu-id="0e3f2-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0e3f2-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0e3f2-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e3f2-128">RELATED LINKS</span></span>
[<span data-ttu-id="0e3f2-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0e3f2-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="0e3f2-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0e3f2-130">Remove-AzureRmDataFactoryV2</span></span>]()

