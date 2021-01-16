---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355789"
---
# <span data-ttu-id="20177-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="20177-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="20177-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20177-102">SYNOPSIS</span></span>
<span data-ttu-id="20177-103">Umożliwia wyświetlenie szczegółowych informacji o pojemności wbudowanej usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="20177-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="20177-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20177-104">SYNTAX</span></span>

### <span data-ttu-id="20177-105">ByCapacityOrResourceGroupOrSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20177-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20177-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20177-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20177-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20177-107">DESCRIPTION</span></span>
<span data-ttu-id="20177-108">W poleceniu cmdlet Get-AzPowerBIEmbeddedCapacity są pobierane szczegóły dotyczące pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="20177-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="20177-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20177-109">EXAMPLES</span></span>

### <span data-ttu-id="20177-110">Przykład 1: uzyskiwanie dyspozycyjności grup zasobów</span><span class="sxs-lookup"><span data-stu-id="20177-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="20177-111">To polecenie umożliwia pobieranie wszystkich możliwości osadzonych usługi Azure PowerBI w grupie zasobów o nazwie testRG</span><span class="sxs-lookup"><span data-stu-id="20177-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="20177-112">Przykład 2: Uzyskaj wydajność</span><span class="sxs-lookup"><span data-stu-id="20177-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="20177-113">To polecenie uzyskuje osadzoną pojemność usługi Azure PowerBI o nazwie testcapacity w grupie zasobów o nazwie testRG.</span><span class="sxs-lookup"><span data-stu-id="20177-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="20177-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20177-114">PARAMETERS</span></span>

### <span data-ttu-id="20177-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20177-115">-DefaultProfile</span></span>
<span data-ttu-id="20177-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20177-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20177-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20177-117">-Name</span></span>
<span data-ttu-id="20177-118">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="20177-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="20177-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20177-119">-ResourceGroupName</span></span>
<span data-ttu-id="20177-120">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="20177-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="20177-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20177-121">-ResourceId</span></span>
<span data-ttu-id="20177-122">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="20177-122">Azure resource ID</span></span>

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

### <span data-ttu-id="20177-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20177-123">CommonParameters</span></span>
<span data-ttu-id="20177-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20177-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20177-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20177-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20177-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20177-126">INPUTS</span></span>

### <span data-ttu-id="20177-127">System. String</span><span class="sxs-lookup"><span data-stu-id="20177-127">System.String</span></span>

## <span data-ttu-id="20177-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20177-128">OUTPUTS</span></span>

### <span data-ttu-id="20177-129">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="20177-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="20177-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20177-130">NOTES</span></span>

## <span data-ttu-id="20177-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20177-131">RELATED LINKS</span></span>

[<span data-ttu-id="20177-132">Nowe — AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="20177-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="20177-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="20177-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
