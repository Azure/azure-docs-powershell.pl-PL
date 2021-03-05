---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 2919c007852961386fb1ab444e43d855ced2a8d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964241"
---
# <span data-ttu-id="449f3-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="449f3-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="449f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="449f3-102">SYNOPSIS</span></span>
<span data-ttu-id="449f3-103">Pobiera listę wszystkich konfiguracji vpnServerConfiguration, które są skojarzone z tym środowiskiem VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="449f3-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="449f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="449f3-104">SYNTAX</span></span>

### <span data-ttu-id="449f3-105">ByVirtualWanName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="449f3-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="449f3-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="449f3-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="449f3-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="449f3-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="449f3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="449f3-108">DESCRIPTION</span></span>
<span data-ttu-id="449f3-109">Polecenie **cmdlet Get-AzVirtualWanVpnServerConfiguration** zwróci listę wszystkich konfiguracji vpnServerConfiguration, które są skojarzone z tą skojarzoną z tym środowiskiem VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="449f3-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="449f3-110">Czyli wszystkie konfiguracje VpnServerConfiguration, które są dołączone do dowolnych P2SVpnGateway w obszarze VirutalHubs tej VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="449f3-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="449f3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="449f3-111">EXAMPLES</span></span>

### <span data-ttu-id="449f3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="449f3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="449f3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="449f3-113">PARAMETERS</span></span>

### <span data-ttu-id="449f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449f3-114">-DefaultProfile</span></span>
<span data-ttu-id="449f3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="449f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="449f3-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="449f3-116">-Name</span></span>
<span data-ttu-id="449f3-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="449f3-117">The resource name.</span></span>

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

### <span data-ttu-id="449f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="449f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="449f3-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="449f3-119">The resource group name.</span></span>

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

### <span data-ttu-id="449f3-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="449f3-120">-ResourceId</span></span>
<span data-ttu-id="449f3-121">Identyfikator zasobu Azure dla wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="449f3-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="449f3-122">— VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="449f3-122">-VirtualWanObject</span></span>
<span data-ttu-id="449f3-123">Obiekt wirtualny wan.</span><span class="sxs-lookup"><span data-stu-id="449f3-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="449f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449f3-124">CommonParameters</span></span>
<span data-ttu-id="449f3-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="449f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449f3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="449f3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449f3-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="449f3-127">INPUTS</span></span>

### <span data-ttu-id="449f3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="449f3-128">System.String</span></span>
<span data-ttu-id="449f3-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="449f3-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="449f3-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="449f3-130">OUTPUTS</span></span>

### <span data-ttu-id="449f3-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="449f3-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="449f3-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="449f3-132">NOTES</span></span>

## <span data-ttu-id="449f3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="449f3-133">RELATED LINKS</span></span>
