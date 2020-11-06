---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541588"
---
# <span data-ttu-id="8daab-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8daab-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8daab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8daab-102">SYNOPSIS</span></span>
<span data-ttu-id="8daab-103">Umożliwia wyświetlenie szczegółowych informacji o pojemności wbudowanej usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8daab-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8daab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8daab-104">SYNTAX</span></span>

### <span data-ttu-id="8daab-105">ByCapacityOrResourceGroupOrSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8daab-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8daab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8daab-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8daab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8daab-107">DESCRIPTION</span></span>
<span data-ttu-id="8daab-108">W poleceniu cmdlet Get-AzureRmPowerBIEmbeddedCapacity są pobierane szczegóły dotyczące pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8daab-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="8daab-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8daab-109">EXAMPLES</span></span>

### <span data-ttu-id="8daab-110">Przykład 1: uzyskiwanie dyspozycyjności grup zasobów</span><span class="sxs-lookup"><span data-stu-id="8daab-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="8daab-111">To polecenie umożliwia pobieranie wszystkich możliwości osadzonych usługi Azure PowerBI w grupie zasobów o nazwie testRG</span><span class="sxs-lookup"><span data-stu-id="8daab-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="8daab-112">Przykład 2: Uzyskaj wydajność</span><span class="sxs-lookup"><span data-stu-id="8daab-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="8daab-113">To polecenie uzyskuje osadzoną pojemność usługi Azure PowerBI o nazwie testcapacity w grupie zasobów o nazwie testRG.</span><span class="sxs-lookup"><span data-stu-id="8daab-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="8daab-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8daab-114">PARAMETERS</span></span>

### <span data-ttu-id="8daab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8daab-115">-DefaultProfile</span></span>
<span data-ttu-id="8daab-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8daab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8daab-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8daab-117">-Name</span></span>
<span data-ttu-id="8daab-118">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="8daab-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8daab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8daab-119">-ResourceGroupName</span></span>
<span data-ttu-id="8daab-120">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="8daab-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8daab-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8daab-121">-ResourceId</span></span>
<span data-ttu-id="8daab-122">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8daab-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8daab-123">CommonParameters</span></span>
<span data-ttu-id="8daab-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8daab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8daab-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8daab-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8daab-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8daab-126">INPUTS</span></span>

### <span data-ttu-id="8daab-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8daab-127">System.String</span></span>

## <span data-ttu-id="8daab-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8daab-128">OUTPUTS</span></span>

### <span data-ttu-id="8daab-129">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8daab-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8daab-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8daab-130">NOTES</span></span>

## <span data-ttu-id="8daab-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8daab-131">RELATED LINKS</span></span>

[<span data-ttu-id="8daab-132">Nowe — AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="8daab-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8daab-133">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="8daab-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
