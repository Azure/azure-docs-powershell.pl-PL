---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179859"
---
# <span data-ttu-id="34f41-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34f41-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="34f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f41-102">SYNOPSIS</span></span>
<span data-ttu-id="34f41-103">Pobiera sieć wirtualną do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34f41-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="34f41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34f41-104">SYNTAX</span></span>

### <span data-ttu-id="34f41-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="34f41-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34f41-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="34f41-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f41-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="34f41-107">DESCRIPTION</span></span>
<span data-ttu-id="34f41-108">Polecenie **cmdlet Get-AzVirtualNetwork** pobiera jedną lub więcej sieci wirtualnych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="34f41-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="34f41-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34f41-109">EXAMPLES</span></span>

### <span data-ttu-id="34f41-110">1. Pobieranie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="34f41-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="34f41-111">To polecenie pobiera sieć wirtualną o nazwie MyVirtualNetwork w grupie zasobów TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34f41-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="34f41-112">2. Lista sieci wirtualnych przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="34f41-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="34f41-113">To polecenie pobiera wszystkie sieci wirtualne, które zaczynają się od "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="34f41-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="34f41-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f41-114">PARAMETERS</span></span>

### <span data-ttu-id="34f41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f41-115">-DefaultProfile</span></span>
<span data-ttu-id="34f41-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34f41-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f41-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="34f41-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f41-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34f41-118">-Name</span></span>
<span data-ttu-id="34f41-119">Określa nazwę sieci wirtualnej, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f41-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="34f41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f41-120">-ResourceGroupName</span></span>
<span data-ttu-id="34f41-121">Określa nazwę grupy zasobów, do której należy sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="34f41-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="34f41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f41-122">CommonParameters</span></span>
<span data-ttu-id="34f41-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f41-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34f41-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f41-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34f41-125">INPUTS</span></span>

### <span data-ttu-id="34f41-126">System.String</span><span class="sxs-lookup"><span data-stu-id="34f41-126">System.String</span></span>

## <span data-ttu-id="34f41-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34f41-127">OUTPUTS</span></span>

### <span data-ttu-id="34f41-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34f41-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="34f41-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34f41-129">NOTES</span></span>

## <span data-ttu-id="34f41-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34f41-130">RELATED LINKS</span></span>

[<span data-ttu-id="34f41-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34f41-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="34f41-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34f41-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="34f41-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34f41-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


