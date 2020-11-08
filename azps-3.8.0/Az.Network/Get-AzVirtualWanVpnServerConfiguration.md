---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: de25e096be96e54d2a8aa18f24bf9915a2f16538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052512"
---
# <span data-ttu-id="fceac-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fceac-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="fceac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fceac-102">SYNOPSIS</span></span>
<span data-ttu-id="fceac-103">Pobiera listę wszystkich VpnServerConfigurations skojarzonych z tym VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="fceac-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="fceac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fceac-104">SYNTAX</span></span>

### <span data-ttu-id="fceac-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fceac-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fceac-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="fceac-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fceac-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="fceac-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fceac-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fceac-108">DESCRIPTION</span></span>
<span data-ttu-id="fceac-109">Polecenie cmdlet **Get-AzVirtualWanVpnServerConfiguration** zwróci listę wszystkich VpnServerConfigurations skojarzonych z tym VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="fceac-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="fceac-110">Wszystkie VpnServerConfigurations, które są dołączane do wszystkich P2SVpnGateways w obszarze VirutalHubs tego VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="fceac-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="fceac-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fceac-111">EXAMPLES</span></span>

### <span data-ttu-id="fceac-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fceac-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="fceac-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fceac-113">PARAMETERS</span></span>

### <span data-ttu-id="fceac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fceac-114">-DefaultProfile</span></span>
<span data-ttu-id="fceac-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fceac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceac-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fceac-116">-Name</span></span>
<span data-ttu-id="fceac-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fceac-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fceac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fceac-118">-ResourceGroupName</span></span>
<span data-ttu-id="fceac-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fceac-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fceac-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fceac-120">-ResourceId</span></span>
<span data-ttu-id="fceac-121">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="fceac-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fceac-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="fceac-122">-VirtualWanObject</span></span>
<span data-ttu-id="fceac-123">Wirtualny obiekt sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="fceac-123">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fceac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fceac-124">CommonParameters</span></span>
<span data-ttu-id="fceac-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fceac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fceac-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fceac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fceac-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fceac-127">INPUTS</span></span>

### <span data-ttu-id="fceac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fceac-128">System.String</span></span>
<span data-ttu-id="fceac-129">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="fceac-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="fceac-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fceac-130">OUTPUTS</span></span>

### <span data-ttu-id="fceac-131">Microsoft. Azure. Commands. Network. models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="fceac-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="fceac-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fceac-132">NOTES</span></span>

## <span data-ttu-id="fceac-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fceac-133">RELATED LINKS</span></span>
