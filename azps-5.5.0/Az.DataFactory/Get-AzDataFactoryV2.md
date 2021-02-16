---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238320"
---
# <span data-ttu-id="88949-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="88949-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="88949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88949-102">SYNOPSIS</span></span>
<span data-ttu-id="88949-103">Pobiera informacje o układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="88949-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="88949-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88949-104">SYNTAX</span></span>

### <span data-ttu-id="88949-105">BySubscriptionId (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="88949-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88949-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="88949-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88949-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="88949-107">DESCRIPTION</span></span>
<span data-ttu-id="88949-108">Polecenie Get-AzDataFactoryV2 pobiera informacje o fabryki danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88949-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="88949-109">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet pobiera informacje o tej fabrycznej układzie danych.</span><span class="sxs-lookup"><span data-stu-id="88949-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="88949-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich fabryki danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88949-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="88949-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88949-111">EXAMPLES</span></span>

### <span data-ttu-id="88949-112">Przykład 1. Uzyskiwanie dostępu do wszystkich fabryki danych</span><span class="sxs-lookup"><span data-stu-id="88949-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="88949-113">Wyświetla informacje o wszystkich fabryki danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88949-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="88949-114">Przykład 2. Uzyskiwanie konkretnej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="88949-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="88949-115">To polecenie wyświetla informacje dotyczące fabryki danych o nazwie WikiADF w subskrypcji grupy zasobów O nazwie ADF, a następnie zapisuje ją w zmiennej $DataFactory danych.</span><span class="sxs-lookup"><span data-stu-id="88949-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="88949-116">Określ parametr DataFactory w kolejnych poleceniach cmdlet, aby użyć fabrycznych danych przechowywanych w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="88949-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="88949-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88949-117">PARAMETERS</span></span>

### <span data-ttu-id="88949-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88949-118">-DefaultProfile</span></span>
<span data-ttu-id="88949-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88949-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88949-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88949-120">-Name</span></span>
<span data-ttu-id="88949-121">Określa nazwę fabryki danych, o której mają być zbierane informacje.</span><span class="sxs-lookup"><span data-stu-id="88949-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="88949-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88949-122">-ResourceGroupName</span></span>
<span data-ttu-id="88949-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88949-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="88949-124">To polecenie cmdlet pobiera informacje o fabryki danych należących do grupy, które określają ten parametr.</span><span class="sxs-lookup"><span data-stu-id="88949-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="88949-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88949-125">CommonParameters</span></span>
<span data-ttu-id="88949-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88949-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88949-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88949-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88949-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88949-128">INPUTS</span></span>

### <span data-ttu-id="88949-129">System.String</span><span class="sxs-lookup"><span data-stu-id="88949-129">System.String</span></span>

## <span data-ttu-id="88949-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88949-130">OUTPUTS</span></span>

### <span data-ttu-id="88949-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="88949-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="88949-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88949-132">NOTES</span></span>
<span data-ttu-id="88949-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="88949-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="88949-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88949-134">RELATED LINKS</span></span>

[<span data-ttu-id="88949-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="88949-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="88949-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="88949-136">Remove-AzDataFactoryV2</span></span>]()

