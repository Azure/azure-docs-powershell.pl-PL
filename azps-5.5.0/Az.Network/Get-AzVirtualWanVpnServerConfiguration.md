---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191938"
---
# <span data-ttu-id="9c2f6-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c2f6-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="9c2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2f6-103">Pobiera listę wszystkich konfiguracji vpnServerConfiguration, które są skojarzone z tym środowiskiem VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="9c2f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c2f6-104">SYNTAX</span></span>

### <span data-ttu-id="9c2f6-105">ByVirtualWanName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9c2f6-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c2f6-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9c2f6-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c2f6-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9c2f6-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c2f6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c2f6-108">DESCRIPTION</span></span>
<span data-ttu-id="9c2f6-109">Polecenie **cmdlet Get-AzVirtualWanVpnServerConfiguration** zwróci listę wszystkich konfiguracji vpnServerConfiguration, które są skojarzone z tą skojarzoną z tym środowiskiem VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="9c2f6-110">Czyli wszystkie konfiguracje VpnServerConfiguration, które są dołączone do dowolnych P2SVpnGateway w obszarze VirutalHubs tej VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="9c2f6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c2f6-111">EXAMPLES</span></span>

### <span data-ttu-id="9c2f6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c2f6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="9c2f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c2f6-113">PARAMETERS</span></span>

### <span data-ttu-id="9c2f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2f6-114">-DefaultProfile</span></span>
<span data-ttu-id="9c2f6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c2f6-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9c2f6-116">-Name</span></span>
<span data-ttu-id="9c2f6-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-117">The resource name.</span></span>

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

### <span data-ttu-id="9c2f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c2f6-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-119">The resource group name.</span></span>

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

### <span data-ttu-id="9c2f6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c2f6-120">-ResourceId</span></span>
<span data-ttu-id="9c2f6-121">Identyfikator zasobu Azure dla wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="9c2f6-122">— VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9c2f6-122">-VirtualWanObject</span></span>
<span data-ttu-id="9c2f6-123">Obiekt wirtualny wan.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="9c2f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2f6-124">CommonParameters</span></span>
<span data-ttu-id="9c2f6-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2f6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c2f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2f6-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c2f6-127">INPUTS</span></span>

### <span data-ttu-id="9c2f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9c2f6-128">System.String</span></span>
<span data-ttu-id="9c2f6-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9c2f6-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="9c2f6-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c2f6-130">OUTPUTS</span></span>

### <span data-ttu-id="9c2f6-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="9c2f6-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="9c2f6-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c2f6-132">NOTES</span></span>

## <span data-ttu-id="9c2f6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c2f6-133">RELATED LINKS</span></span>
