---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716721"
---
# <span data-ttu-id="97b16-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="97b16-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="97b16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97b16-102">SYNOPSIS</span></span>
<span data-ttu-id="97b16-103">Umożliwia wyświetlenie szczegółowych informacji o pojemności wbudowanej usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="97b16-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97b16-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="97b16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97b16-105">DESCRIPTION</span></span>
<span data-ttu-id="97b16-106">W poleceniu cmdlet Get-AzureRmPowerBIEmbeddedCapacity są pobierane szczegóły dotyczące pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="97b16-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="97b16-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97b16-107">EXAMPLES</span></span>

### <span data-ttu-id="97b16-108">Przykład 1: uzyskiwanie dyspozycyjności grup zasobów</span><span class="sxs-lookup"><span data-stu-id="97b16-108">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="97b16-109">To polecenie umożliwia pobieranie wszystkich możliwości osadzonych usługi Azure PowerBI w grupie zasobów o nazwie testRG</span><span class="sxs-lookup"><span data-stu-id="97b16-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="97b16-110">Przykład 2: Uzyskaj wydajność</span><span class="sxs-lookup"><span data-stu-id="97b16-110">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="97b16-111">To polecenie uzyskuje osadzoną pojemność usługi Azure PowerBI o nazwie testcapacity w grupie zasobów o nazwie testRG.</span><span class="sxs-lookup"><span data-stu-id="97b16-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="97b16-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97b16-112">PARAMETERS</span></span>

### <span data-ttu-id="97b16-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b16-113">-ResourceGroupName</span></span>
<span data-ttu-id="97b16-114">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="97b16-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="97b16-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97b16-115">-Name</span></span>
<span data-ttu-id="97b16-116">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="97b16-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="97b16-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97b16-117">-ResourceId</span></span>
<span data-ttu-id="97b16-118">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="97b16-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b16-119">CommonParameters</span></span>
<span data-ttu-id="97b16-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b16-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b16-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97b16-122">INPUTS</span></span>

### <span data-ttu-id="97b16-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="97b16-123">None</span></span>
<span data-ttu-id="97b16-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="97b16-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97b16-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97b16-125">OUTPUTS</span></span>

### <span data-ttu-id="97b16-126">Lista<> Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="97b16-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="97b16-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97b16-127">NOTES</span></span>

## <span data-ttu-id="97b16-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97b16-128">RELATED LINKS</span></span>

[<span data-ttu-id="97b16-129">Nowe — AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="97b16-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="97b16-130">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="97b16-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
