---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379752"
---
# <span data-ttu-id="c2fc4-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fc4-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="c2fc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fc4-103">Pobiera listę wszystkich VpnServerConfigurations skojarzonych z tym VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="c2fc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2fc4-104">SYNTAX</span></span>

### <span data-ttu-id="c2fc4-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2fc4-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2fc4-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c2fc4-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2fc4-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c2fc4-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2fc4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c2fc4-108">DESCRIPTION</span></span>
<span data-ttu-id="c2fc4-109">Polecenie cmdlet **Get-AzVirtualWanVpnServerConfiguration** zwróci listę wszystkich VpnServerConfigurations skojarzonych z tym VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="c2fc4-110">Wszystkie VpnServerConfigurations, które są dołączane do wszystkich P2SVpnGateways w obszarze VirutalHubs tego VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="c2fc4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2fc4-111">EXAMPLES</span></span>

### <span data-ttu-id="c2fc4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2fc4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="c2fc4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2fc4-113">PARAMETERS</span></span>

### <span data-ttu-id="c2fc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fc4-114">-DefaultProfile</span></span>
<span data-ttu-id="c2fc4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fc4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2fc4-116">-Name</span></span>
<span data-ttu-id="c2fc4-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fc4-118">-ResourceGroupName</span></span>
<span data-ttu-id="c2fc4-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2fc4-120">-ResourceId</span></span>
<span data-ttu-id="c2fc4-121">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc4-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c2fc4-122">-VirtualWanObject</span></span>
<span data-ttu-id="c2fc4-123">Wirtualny obiekt sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fc4-124">CommonParameters</span></span>
<span data-ttu-id="c2fc4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fc4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2fc4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fc4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2fc4-127">INPUTS</span></span>

### <span data-ttu-id="c2fc4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c2fc4-128">System.String</span></span>
<span data-ttu-id="c2fc4-129">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c2fc4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="c2fc4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2fc4-130">OUTPUTS</span></span>

### <span data-ttu-id="c2fc4-131">Microsoft. Azure. Commands. Network. models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="c2fc4-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="c2fc4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2fc4-132">NOTES</span></span>

## <span data-ttu-id="c2fc4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2fc4-133">RELATED LINKS</span></span>
