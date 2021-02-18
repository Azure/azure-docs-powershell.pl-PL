---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184770"
---
# <span data-ttu-id="cdc87-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdc87-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="cdc87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc87-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc87-103">Pobiera konfigurację adresów IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cdc87-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="cdc87-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdc87-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc87-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdc87-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc87-106">Polecenie **cmdlet Get-AzApplicationGatewayIPConfiguration** pobiera konfigurację adresów IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cdc87-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="cdc87-107">Konfiguracja adresu IP zawiera podsieci, w której jest wdrożona brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cdc87-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="cdc87-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdc87-108">EXAMPLES</span></span>

### <span data-ttu-id="cdc87-109">Przykład 1. Uzyskiwanie konkretnej konfiguracji protokołu IP</span><span class="sxs-lookup"><span data-stu-id="cdc87-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="cdc87-110">Pierwsze polecenie pobiera bramę aplikacji i przechowuje je w $AppGw aplikacji. Drugie polecenie pobiera konfigurację adresów IP o nazwie GateSubnet01 z bramy przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cdc87-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="cdc87-111">Przykład 2. Uzyskiwanie listy konfiguracji adresów IP</span><span class="sxs-lookup"><span data-stu-id="cdc87-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="cdc87-112">Pierwsze polecenie otrzymuje bramę aplikacji i zapisuje je w $AppGw aplikacji. Drugie polecenie otrzymuje listę wszystkich konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="cdc87-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="cdc87-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdc87-113">PARAMETERS</span></span>

### <span data-ttu-id="cdc87-114">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdc87-114">-ApplicationGateway</span></span>
<span data-ttu-id="cdc87-115">Określa obiekt bramy aplikacji zawierający konfigurację protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="cdc87-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc87-116">-DefaultProfile</span></span>
<span data-ttu-id="cdc87-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc87-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc87-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cdc87-118">-Name</span></span>
<span data-ttu-id="cdc87-119">Określa nazwę konfiguracji protokołu IP, którą otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdc87-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc87-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc87-120">CommonParameters</span></span>
<span data-ttu-id="cdc87-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc87-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc87-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdc87-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc87-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdc87-123">INPUTS</span></span>

### <span data-ttu-id="cdc87-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdc87-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cdc87-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdc87-125">OUTPUTS</span></span>

### <span data-ttu-id="cdc87-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdc87-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="cdc87-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdc87-127">NOTES</span></span>

## <span data-ttu-id="cdc87-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdc87-128">RELATED LINKS</span></span>

[<span data-ttu-id="cdc87-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdc87-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cdc87-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdc87-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cdc87-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdc87-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cdc87-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdc87-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


