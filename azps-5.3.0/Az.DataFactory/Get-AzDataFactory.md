---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503704"
---
# <span data-ttu-id="95e18-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="95e18-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="95e18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95e18-102">SYNOPSIS</span></span>
<span data-ttu-id="95e18-103">Pobiera informacje na temat fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="95e18-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="95e18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95e18-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95e18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95e18-105">DESCRIPTION</span></span>
<span data-ttu-id="95e18-106">Polecenie cmdlet **Get-AzDataFactory** pobiera informacje dotyczące fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95e18-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="95e18-107">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet będzie pobierać informacje na temat fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="95e18-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="95e18-108">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95e18-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="95e18-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95e18-109">EXAMPLES</span></span>

### <span data-ttu-id="95e18-110">Przykład 1: pobieranie wszystkich fabryk danych</span><span class="sxs-lookup"><span data-stu-id="95e18-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="95e18-111">To polecenie wyświetla informacje dotyczące wszystkich fabryk danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95e18-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="95e18-112">Przykład 2: uzyskiwanie określonej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="95e18-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="95e18-113">To polecenie wyświetla informacje o fabryce danych o nazwie WikiADF w subskrypcji grupy zasobów o nazwie ADF, a następnie zapisuje je w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="95e18-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="95e18-114">Określ parametr *DataFactory* w kolejnych poleceniach cmdlet, aby użyć fabryki danych przechowywanej w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="95e18-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="95e18-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95e18-115">PARAMETERS</span></span>

### <span data-ttu-id="95e18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e18-116">-DefaultProfile</span></span>
<span data-ttu-id="95e18-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="95e18-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95e18-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95e18-118">-Name</span></span>
<span data-ttu-id="95e18-119">Określa nazwę fabryki danych, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="95e18-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e18-120">-ResourceGroupName</span></span>
<span data-ttu-id="95e18-121">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95e18-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="95e18-122">To polecenie cmdlet umożliwia pobieranie informacji o fabrykach danych należących do grupy, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="95e18-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e18-123">CommonParameters</span></span>
<span data-ttu-id="95e18-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e18-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95e18-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e18-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95e18-126">INPUTS</span></span>

### <span data-ttu-id="95e18-127">System. String</span><span class="sxs-lookup"><span data-stu-id="95e18-127">System.String</span></span>

## <span data-ttu-id="95e18-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95e18-128">OUTPUTS</span></span>

### <span data-ttu-id="95e18-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="95e18-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="95e18-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95e18-130">NOTES</span></span>
* <span data-ttu-id="95e18-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="95e18-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="95e18-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95e18-132">RELATED LINKS</span></span>

[<span data-ttu-id="95e18-133">Nowe — AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="95e18-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="95e18-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="95e18-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


