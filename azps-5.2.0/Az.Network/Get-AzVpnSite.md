---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365967"
---
# <span data-ttu-id="7fe29-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7fe29-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="7fe29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fe29-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe29-103">Pobiera zasób usługi Azure VpnSite, używając nazwy lub wyświetla wszystkie VpnSites w źródle danych lub identyfikatorze subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7fe29-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="7fe29-104">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="7fe29-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="7fe29-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fe29-105">SYNTAX</span></span>

### <span data-ttu-id="7fe29-106">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7fe29-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fe29-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe29-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fe29-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7fe29-108">DESCRIPTION</span></span>
<span data-ttu-id="7fe29-109">Pobiera zasób usługi Azure VpnSite, używając nazwy lub wyświetla wszystkie VpnSites w źródle danych lub identyfikatorze subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7fe29-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="7fe29-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fe29-110">EXAMPLES</span></span>

### <span data-ttu-id="7fe29-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fe29-111">Example 1</span></span>

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

<span data-ttu-id="7fe29-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe29-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="7fe29-113">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="7fe29-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="7fe29-114">Po utworzeniu witryny jest ona pobierana za pomocą polecenia Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="7fe29-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="7fe29-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7fe29-115">Example 2</span></span>

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

<span data-ttu-id="7fe29-116">To polecenie cmdlet umożliwia pobieranie wszystkich witryn, które zaczynają się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="7fe29-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="7fe29-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fe29-117">PARAMETERS</span></span>

### <span data-ttu-id="7fe29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe29-118">-DefaultProfile</span></span>
<span data-ttu-id="7fe29-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fe29-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7fe29-120">-Name</span></span>
<span data-ttu-id="7fe29-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7fe29-121">The resource name.</span></span>

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

### <span data-ttu-id="7fe29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe29-122">-ResourceGroupName</span></span>
<span data-ttu-id="7fe29-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7fe29-123">The resource group name.</span></span>

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

### <span data-ttu-id="7fe29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe29-124">CommonParameters</span></span>
<span data-ttu-id="7fe29-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fe29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe29-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fe29-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe29-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fe29-127">INPUTS</span></span>

### <span data-ttu-id="7fe29-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7fe29-128">None</span></span>

## <span data-ttu-id="7fe29-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fe29-129">OUTPUTS</span></span>

### <span data-ttu-id="7fe29-130">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="7fe29-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="7fe29-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fe29-131">NOTES</span></span>

## <span data-ttu-id="7fe29-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fe29-132">RELATED LINKS</span></span>

[<span data-ttu-id="7fe29-133">Nowe — AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7fe29-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="7fe29-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7fe29-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="7fe29-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7fe29-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
