---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 0bc3d62ad690ab8bed961045ce46448af8700bd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982609"
---
# <span data-ttu-id="e852a-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e852a-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="e852a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e852a-102">SYNOPSIS</span></span>
<span data-ttu-id="e852a-103">Dodaje konfigurację prywatnego linku do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e852a-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="e852a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e852a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e852a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e852a-105">DESCRIPTION</span></span>
<span data-ttu-id="e852a-106">Polecenie **cmdlet Add-AzApplicationGatewayPrivateLinkConfiguration** dodaje konfigurację prywatnego linku do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e852a-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="e852a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e852a-107">EXAMPLES</span></span>

### <span data-ttu-id="e852a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e852a-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="e852a-109">Pierwsze polecenie tworzy nazwę privateLinkIpConfiguration i zapisuje ją w $PrivateLinkIpConfiguration zmienną.</span><span class="sxs-lookup"><span data-stu-id="e852a-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="e852a-110">Drugie polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="e852a-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e852a-111">Trzecie polecenie dodaje konfigurację łącza prywatnego o nazwie privateLinkConfig01 dla bramy w u $AppGw</span><span class="sxs-lookup"><span data-stu-id="e852a-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="e852a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e852a-112">PARAMETERS</span></span>

### <span data-ttu-id="e852a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e852a-113">-ApplicationGateway</span></span>
<span data-ttu-id="e852a-114">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e852a-114">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e852a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e852a-115">-DefaultProfile</span></span>
<span data-ttu-id="e852a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e852a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e852a-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e852a-117">-IpConfiguration</span></span>
<span data-ttu-id="e852a-118">Lista konfiguracji ip</span><span class="sxs-lookup"><span data-stu-id="e852a-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e852a-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e852a-119">-Name</span></span>
<span data-ttu-id="e852a-120">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="e852a-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e852a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e852a-121">CommonParameters</span></span>
<span data-ttu-id="e852a-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e852a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e852a-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e852a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e852a-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e852a-124">INPUTS</span></span>

### <span data-ttu-id="e852a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e852a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="e852a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="e852a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="e852a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e852a-127">OUTPUTS</span></span>

### <span data-ttu-id="e852a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e852a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e852a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e852a-129">NOTES</span></span>

## <span data-ttu-id="e852a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e852a-130">RELATED LINKS</span></span>

[<span data-ttu-id="e852a-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e852a-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e852a-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e852a-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e852a-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e852a-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e852a-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e852a-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)