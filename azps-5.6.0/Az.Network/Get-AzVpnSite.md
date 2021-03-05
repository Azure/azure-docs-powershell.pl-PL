---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 444addf1b7f036ffc4fcaae4a1070b9238c29dc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965681"
---
# <span data-ttu-id="6c8aa-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6c8aa-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="6c8aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8aa-103">Pobiera zasób witryny vpnsite platformy Azure według nazwy LUB wyświetla listę wszystkich witryny vpn w grupie zasobów lub usłudze SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="6c8aa-104">Jest to reprezentacja RM gałęzi klienta, które są przekazywane na platformę Azure dla S2S za pomocą centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="6c8aa-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c8aa-105">SYNTAX</span></span>

### <span data-ttu-id="6c8aa-106">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6c8aa-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c8aa-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8aa-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c8aa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c8aa-108">DESCRIPTION</span></span>
<span data-ttu-id="6c8aa-109">Pobiera zasób witryny vpnsite platformy Azure według nazwy LUB wyświetla listę wszystkich witryny vpn w grupie zasobów lub usłudze SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="6c8aa-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c8aa-110">EXAMPLES</span></span>

### <span data-ttu-id="6c8aa-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c8aa-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="6c8aa-112">Powyższe spowoduje utworzenie grupy zasobów o wirtualnej sieci WAN w Zachód USA w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="6c8aa-113">Następnie tworzy witrynę VpnSite reprezentującą gałąź klienta i łączy ją z wirtualną siecią WAN.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="6c8aa-114">Po utworzeniu witryna pobiera ją za pomocą Get-AzVpnSite witryny.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="6c8aa-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6c8aa-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="6c8aa-116">To polecenie cmdlet pobiera wszystkie witryny, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="6c8aa-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="6c8aa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c8aa-117">PARAMETERS</span></span>

### <span data-ttu-id="6c8aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8aa-118">-DefaultProfile</span></span>
<span data-ttu-id="6c8aa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c8aa-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6c8aa-120">-Name</span></span>
<span data-ttu-id="6c8aa-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c8aa-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8aa-124">CommonParameters</span></span>
<span data-ttu-id="6c8aa-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8aa-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c8aa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8aa-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c8aa-127">INPUTS</span></span>

### <span data-ttu-id="6c8aa-128">Brak</span><span class="sxs-lookup"><span data-stu-id="6c8aa-128">None</span></span>

## <span data-ttu-id="6c8aa-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c8aa-129">OUTPUTS</span></span>

### <span data-ttu-id="6c8aa-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="6c8aa-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="6c8aa-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c8aa-131">NOTES</span></span>

## <span data-ttu-id="6c8aa-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c8aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c8aa-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6c8aa-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="6c8aa-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6c8aa-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="6c8aa-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="6c8aa-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
