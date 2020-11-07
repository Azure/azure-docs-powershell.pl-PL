---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 5a7faf2e3eebcb00650bce367747e1945f7524da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527718"
---
# <span data-ttu-id="b5f53-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5f53-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="b5f53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5f53-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f53-103">Pobiera informacje na temat fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="b5f53-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5f53-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5f53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5f53-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f53-106">Polecenie cmdlet **Get-AzureRmDataFactory** pobiera informacje dotyczące fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f53-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="b5f53-107">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet będzie pobierać informacje na temat fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b5f53-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="b5f53-108">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich fabryk danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f53-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="b5f53-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5f53-109">EXAMPLES</span></span>

### <span data-ttu-id="b5f53-110">Przykład 1: pobieranie wszystkich fabryk danych</span><span class="sxs-lookup"><span data-stu-id="b5f53-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="b5f53-111">To polecenie wyświetla informacje dotyczące wszystkich fabryk danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f53-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="b5f53-112">Przykład 2: uzyskiwanie określonej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="b5f53-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="b5f53-113">To polecenie wyświetla informacje o fabryce danych o nazwie WikiADF w subskrypcji grupy zasobów o nazwie ADF, a następnie zapisuje je w zmiennej $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b5f53-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="b5f53-114">Określ parametr *DataFactory* w kolejnych poleceniach cmdlet, aby użyć fabryki danych przechowywanej w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b5f53-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="b5f53-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5f53-115">PARAMETERS</span></span>

### <span data-ttu-id="b5f53-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5f53-116">-Name</span></span>
<span data-ttu-id="b5f53-117">Określa nazwę fabryki danych, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="b5f53-117">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="b5f53-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f53-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5f53-119">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f53-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b5f53-120">To polecenie cmdlet umożliwia pobieranie informacji o fabrykach danych należących do grupy, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b5f53-120">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5f53-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f53-121">-DefaultProfile</span></span>
<span data-ttu-id="b5f53-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f53-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5f53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f53-123">CommonParameters</span></span>
<span data-ttu-id="b5f53-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f53-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f53-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f53-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5f53-126">INPUTS</span></span>

## <span data-ttu-id="b5f53-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5f53-127">OUTPUTS</span></span>

### <span data-ttu-id="b5f53-128">System. Collections. Generic. list "1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. platformy windowsazure. Commands. Commands, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5f53-128">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="b5f53-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5f53-129">NOTES</span></span>
* <span data-ttu-id="b5f53-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="b5f53-130">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b5f53-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5f53-131">RELATED LINKS</span></span>

[<span data-ttu-id="b5f53-132">Nowe — AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5f53-132">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="b5f53-133">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5f53-133">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)

