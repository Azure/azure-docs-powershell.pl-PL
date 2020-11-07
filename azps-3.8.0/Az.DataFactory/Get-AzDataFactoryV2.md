---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: d52ddd20253e2d6969a19b92f7bd973584a7f630
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896470"
---
# <span data-ttu-id="860cf-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="860cf-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="860cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="860cf-102">SYNOPSIS</span></span>
<span data-ttu-id="860cf-103">Pobiera informacje o fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="860cf-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="860cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="860cf-104">SYNTAX</span></span>

### <span data-ttu-id="860cf-105">BySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="860cf-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="860cf-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="860cf-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="860cf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="860cf-107">DESCRIPTION</span></span>
<span data-ttu-id="860cf-108">Polecenie cmdlet Get-AzDataFactoryV2 pobiera informacje na temat fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="860cf-109">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet będzie pobierać informacje na temat fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="860cf-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="860cf-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="860cf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="860cf-111">EXAMPLES</span></span>

### <span data-ttu-id="860cf-112">Przykład 1: pobieranie wszystkich fabryk danych</span><span class="sxs-lookup"><span data-stu-id="860cf-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="860cf-113">Wyświetla informacje dotyczące wszystkich fabryk danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="860cf-114">Przykład 2: uzyskiwanie określonej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="860cf-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="860cf-115">To polecenie wyświetla informacje o fabryce danych o nazwie WikiADF w subskrypcji grupy zasobów o nazwie ADF, a następnie zapisuje je w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="860cf-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="860cf-116">Określ parametr DataFactory w kolejnych poleceniach cmdlet, aby użyć fabryki danych przechowywanej w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="860cf-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="860cf-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="860cf-117">PARAMETERS</span></span>

### <span data-ttu-id="860cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860cf-118">-DefaultProfile</span></span>
<span data-ttu-id="860cf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860cf-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="860cf-120">-Name</span></span>
<span data-ttu-id="860cf-121">Określa nazwę fabryki danych, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="860cf-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="860cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="860cf-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="860cf-124">To polecenie cmdlet umożliwia pobieranie informacji na temat fabryk danych należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="860cf-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="860cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860cf-125">CommonParameters</span></span>
<span data-ttu-id="860cf-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860cf-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860cf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860cf-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="860cf-128">INPUTS</span></span>

### <span data-ttu-id="860cf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="860cf-129">System.String</span></span>

## <span data-ttu-id="860cf-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="860cf-130">OUTPUTS</span></span>

### <span data-ttu-id="860cf-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="860cf-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="860cf-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="860cf-132">NOTES</span></span>
<span data-ttu-id="860cf-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="860cf-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="860cf-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="860cf-134">RELATED LINKS</span></span>

[<span data-ttu-id="860cf-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="860cf-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="860cf-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="860cf-136">Remove-AzDataFactoryV2</span></span>]()

