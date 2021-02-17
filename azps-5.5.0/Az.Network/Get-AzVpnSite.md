---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184562"
---
# <span data-ttu-id="be6a0-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="be6a0-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="be6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="be6a0-103">Pobiera zasób witryny VpnSite platformy Azure według nazwy LUB wyświetla listę wszystkich vpnsites w grupie zasobów lub usłudze SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="be6a0-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="be6a0-104">Jest to reprezentacja rm rozgałęzień klientów, które są przekazywane na platformę Azure dla S2S w ramach centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="be6a0-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="be6a0-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be6a0-105">SYNTAX</span></span>

### <span data-ttu-id="be6a0-106">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="be6a0-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be6a0-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be6a0-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be6a0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="be6a0-108">DESCRIPTION</span></span>
<span data-ttu-id="be6a0-109">Pobiera zasób witryny VpnSite platformy Azure według nazwy LUB wyświetla listę wszystkich vpnsites w grupie zasobów lub usłudze SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="be6a0-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="be6a0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be6a0-110">EXAMPLES</span></span>

### <span data-ttu-id="be6a0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be6a0-111">Example 1</span></span>

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

<span data-ttu-id="be6a0-112">Powyższe spowoduje utworzenie grupy zasobów — wirtualnej sieci WAN w zachód Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="be6a0-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="be6a0-113">Następnie tworzy witrynę VpnSite reprezentującą gałąź klienta i łączy ją z wirtualną siecią WAN.</span><span class="sxs-lookup"><span data-stu-id="be6a0-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="be6a0-114">Po utworzeniu witryna pobiera ją za pomocą Get-AzVpnSite witryny.</span><span class="sxs-lookup"><span data-stu-id="be6a0-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="be6a0-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="be6a0-115">Example 2</span></span>

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

<span data-ttu-id="be6a0-116">To polecenie cmdlet pobiera wszystkie witryny, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="be6a0-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="be6a0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be6a0-117">PARAMETERS</span></span>

### <span data-ttu-id="be6a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be6a0-118">-DefaultProfile</span></span>
<span data-ttu-id="be6a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be6a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be6a0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be6a0-120">-Name</span></span>
<span data-ttu-id="be6a0-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="be6a0-121">The resource name.</span></span>

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

### <span data-ttu-id="be6a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be6a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="be6a0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be6a0-123">The resource group name.</span></span>

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

### <span data-ttu-id="be6a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be6a0-124">CommonParameters</span></span>
<span data-ttu-id="be6a0-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be6a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be6a0-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be6a0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be6a0-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be6a0-127">INPUTS</span></span>

### <span data-ttu-id="be6a0-128">Brak</span><span class="sxs-lookup"><span data-stu-id="be6a0-128">None</span></span>

## <span data-ttu-id="be6a0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be6a0-129">OUTPUTS</span></span>

### <span data-ttu-id="be6a0-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="be6a0-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="be6a0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be6a0-131">NOTES</span></span>

## <span data-ttu-id="be6a0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be6a0-132">RELATED LINKS</span></span>

[<span data-ttu-id="be6a0-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="be6a0-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="be6a0-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="be6a0-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="be6a0-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="be6a0-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
