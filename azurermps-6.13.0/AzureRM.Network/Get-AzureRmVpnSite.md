---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543708"
---
# <span data-ttu-id="aa99c-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="aa99c-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="aa99c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa99c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa99c-103">Pobiera zasób usługi Azure VpnSite, używając nazwy lub wyświetla wszystkie VpnSites w źródle danych lub identyfikatorze subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aa99c-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="aa99c-104">Jest to reprezentacja oddziałów klientów, które są przekazywane do platformy Azure dla połączeń S2S za pomocą wirtualnego centrum Cortex.</span><span class="sxs-lookup"><span data-stu-id="aa99c-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa99c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa99c-105">SYNTAX</span></span>

### <span data-ttu-id="aa99c-106">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa99c-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa99c-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa99c-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa99c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa99c-108">DESCRIPTION</span></span>
<span data-ttu-id="aa99c-109">Pobiera zasób usługi Azure VpnSite, używając nazwy lub wyświetla wszystkie VpnSites w źródle danych lub identyfikatorze subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aa99c-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="aa99c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa99c-110">EXAMPLES</span></span>

### <span data-ttu-id="aa99c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa99c-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="aa99c-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="aa99c-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="aa99c-113">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="aa99c-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="aa99c-114">Po utworzeniu witryny jest ona pobierana za pomocą polecenia Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="aa99c-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="aa99c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa99c-115">PARAMETERS</span></span>

### <span data-ttu-id="aa99c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa99c-116">-DefaultProfile</span></span>
<span data-ttu-id="aa99c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa99c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa99c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa99c-118">-Name</span></span>
<span data-ttu-id="aa99c-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa99c-119">The resource name.</span></span>

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

### <span data-ttu-id="aa99c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa99c-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa99c-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa99c-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa99c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa99c-122">CommonParameters</span></span>
<span data-ttu-id="aa99c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa99c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa99c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa99c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa99c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa99c-125">INPUTS</span></span>

### <span data-ttu-id="aa99c-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aa99c-126">None</span></span>

## <span data-ttu-id="aa99c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa99c-127">OUTPUTS</span></span>

### <span data-ttu-id="aa99c-128">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="aa99c-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="aa99c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa99c-129">NOTES</span></span>

## <span data-ttu-id="aa99c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa99c-130">RELATED LINKS</span></span>
