---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 17d7547daaffdfafc117a250d20c0af1f069b70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953473"
---
# <span data-ttu-id="f1aee-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f1aee-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f1aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1aee-102">SYNOPSIS</span></span>
<span data-ttu-id="f1aee-103">Pobiera szczegółowe informacje o osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="f1aee-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f1aee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1aee-104">SYNTAX</span></span>

### <span data-ttu-id="f1aee-105">ByCapacityOrResourceGroupOrSubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="f1aee-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1aee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1aee-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1aee-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1aee-107">DESCRIPTION</span></span>
<span data-ttu-id="f1aee-108">Polecenie Get-AzPowerBIEmbeddedCapacity cmdlet pobiera szczegółowe informacje dotyczące osadzonej pojemności usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="f1aee-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f1aee-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1aee-109">EXAMPLES</span></span>

### <span data-ttu-id="f1aee-110">Przykład 1. Wykorzystanie zasobów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="f1aee-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="f1aee-111">To polecenie pobiera całą osadzoną wydajność usługi Azure PowerBI w grupie zasobów o nazwie testRG</span><span class="sxs-lookup"><span data-stu-id="f1aee-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="f1aee-112">Przykład 2. Uzyskiwanie pojemności</span><span class="sxs-lookup"><span data-stu-id="f1aee-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="f1aee-113">To polecenie pobiera osadzoną wydajność usługi Azure PowerBI o nazwie testcapacity w grupie zasobów o nazwie testRG.</span><span class="sxs-lookup"><span data-stu-id="f1aee-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="f1aee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1aee-114">PARAMETERS</span></span>

### <span data-ttu-id="f1aee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1aee-115">-DefaultProfile</span></span>
<span data-ttu-id="f1aee-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1aee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1aee-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1aee-117">-Name</span></span>
<span data-ttu-id="f1aee-118">Nazwa osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="f1aee-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="f1aee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1aee-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1aee-120">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="f1aee-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="f1aee-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1aee-121">-ResourceId</span></span>
<span data-ttu-id="f1aee-122">Identyfikator zasobu Azure</span><span class="sxs-lookup"><span data-stu-id="f1aee-122">Azure resource ID</span></span>

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

### <span data-ttu-id="f1aee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1aee-123">CommonParameters</span></span>
<span data-ttu-id="f1aee-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1aee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1aee-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1aee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1aee-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1aee-126">INPUTS</span></span>

### <span data-ttu-id="f1aee-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f1aee-127">System.String</span></span>

## <span data-ttu-id="f1aee-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1aee-128">OUTPUTS</span></span>

### <span data-ttu-id="f1aee-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f1aee-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f1aee-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1aee-130">NOTES</span></span>

## <span data-ttu-id="f1aee-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1aee-131">RELATED LINKS</span></span>

[<span data-ttu-id="f1aee-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="f1aee-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f1aee-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="f1aee-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
