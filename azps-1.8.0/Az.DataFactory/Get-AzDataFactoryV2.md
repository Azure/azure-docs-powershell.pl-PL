---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: 94d3a23d3ce43c97594f53e092544d2bbdeb9a1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868771"
---
# <span data-ttu-id="ff968-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff968-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="ff968-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff968-102">SYNOPSIS</span></span>
<span data-ttu-id="ff968-103">Pobiera informacje o fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="ff968-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="ff968-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff968-104">SYNTAX</span></span>

### <span data-ttu-id="ff968-105">BySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff968-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff968-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="ff968-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff968-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff968-107">DESCRIPTION</span></span>
<span data-ttu-id="ff968-108">Polecenie cmdlet Get-AzDataFactoryV2 pobiera informacje na temat fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff968-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="ff968-109">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet będzie pobierać informacje na temat fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="ff968-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="ff968-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff968-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="ff968-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff968-111">EXAMPLES</span></span>

### <span data-ttu-id="ff968-112">Przykład 1: pobieranie wszystkich fabryk danych</span><span class="sxs-lookup"><span data-stu-id="ff968-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="ff968-113">Wyświetla informacje dotyczące wszystkich fabryk danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff968-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="ff968-114">Przykład 2: uzyskiwanie określonej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="ff968-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="ff968-115">To polecenie wyświetla informacje o fabryce danych o nazwie WikiADF w subskrypcji grupy zasobów o nazwie ADF, a następnie zapisuje je w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ff968-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="ff968-116">Określ parametr DataFactory w kolejnych poleceniach cmdlet, aby użyć fabryki danych przechowywanej w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ff968-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="ff968-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff968-117">PARAMETERS</span></span>

### <span data-ttu-id="ff968-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff968-118">-DefaultProfile</span></span>
<span data-ttu-id="ff968-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff968-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff968-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff968-120">-Name</span></span>
<span data-ttu-id="ff968-121">Określa nazwę fabryki danych, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="ff968-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff968-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff968-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff968-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff968-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff968-124">To polecenie cmdlet umożliwia pobieranie informacji na temat fabryk danych należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ff968-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="ff968-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff968-125">CommonParameters</span></span>
<span data-ttu-id="ff968-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff968-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff968-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff968-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff968-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff968-128">INPUTS</span></span>

### <span data-ttu-id="ff968-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ff968-129">System.String</span></span>

## <span data-ttu-id="ff968-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff968-130">OUTPUTS</span></span>

### <span data-ttu-id="ff968-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff968-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ff968-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff968-132">NOTES</span></span>
<span data-ttu-id="ff968-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="ff968-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff968-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff968-134">RELATED LINKS</span></span>

[<span data-ttu-id="ff968-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff968-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="ff968-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff968-136">Remove-AzDataFactoryV2</span></span>]()

