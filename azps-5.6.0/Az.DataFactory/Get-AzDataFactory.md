---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: ff47851c998cb88bec7106e8aba6d47d16069321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977162"
---
# <span data-ttu-id="1fb99-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fb99-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="1fb99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb99-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb99-103">Pobiera informacje o fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1fb99-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="1fb99-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1fb99-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb99-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1fb99-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb99-106">Polecenie **cmdlet Get-AzDataFactory** pobiera informacje o fabryki danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb99-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="1fb99-107">Jeśli określisz nazwę fabryki danych, to polecenie cmdlet pobiera informacje o tej fabrycznej układzie danych.</span><span class="sxs-lookup"><span data-stu-id="1fb99-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="1fb99-108">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich fabryki danych w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb99-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="1fb99-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1fb99-109">EXAMPLES</span></span>

### <span data-ttu-id="1fb99-110">Przykład 1. Uzyskiwanie dostępu do wszystkich fabryki danych</span><span class="sxs-lookup"><span data-stu-id="1fb99-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="1fb99-111">To polecenie powoduje wyświetlenie informacji o wszystkich fabryki danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb99-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="1fb99-112">Przykład 2. Uzyskiwanie konkretnej fabryki danych</span><span class="sxs-lookup"><span data-stu-id="1fb99-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="1fb99-113">To polecenie wyświetla informacje o factory danych o nazwie WikiADF w subskrypcji grupy zasobów O nazwie ADF, a następnie zapisuje ją w zmiennej $DataFactory danych.</span><span class="sxs-lookup"><span data-stu-id="1fb99-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="1fb99-114">Określ parametr *DataFactory* w kolejnych poleceniach cmdlet, aby użyć fabrycznych danych przechowywanych w $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="1fb99-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="1fb99-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fb99-115">PARAMETERS</span></span>

### <span data-ttu-id="1fb99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb99-116">-DefaultProfile</span></span>
<span data-ttu-id="1fb99-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1fb99-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fb99-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1fb99-118">-Name</span></span>
<span data-ttu-id="1fb99-119">Określa nazwę fabryki danych, o której mają być zbierane informacje.</span><span class="sxs-lookup"><span data-stu-id="1fb99-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="1fb99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb99-120">-ResourceGroupName</span></span>
<span data-ttu-id="1fb99-121">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb99-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1fb99-122">To polecenie cmdlet pobiera informacje o fabryki danych należących do grupy, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1fb99-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fb99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb99-123">CommonParameters</span></span>
<span data-ttu-id="1fb99-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb99-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb99-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb99-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fb99-126">INPUTS</span></span>

### <span data-ttu-id="1fb99-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1fb99-127">System.String</span></span>

## <span data-ttu-id="1fb99-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fb99-128">OUTPUTS</span></span>

### <span data-ttu-id="1fb99-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fb99-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1fb99-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1fb99-130">NOTES</span></span>
* <span data-ttu-id="1fb99-131">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1fb99-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1fb99-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fb99-132">RELATED LINKS</span></span>

[<span data-ttu-id="1fb99-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fb99-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="1fb99-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fb99-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


