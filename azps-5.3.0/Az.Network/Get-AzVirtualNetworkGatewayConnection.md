---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503580"
---
# <span data-ttu-id="eb7b6-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb7b6-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="eb7b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7b6-103">Pobiera połączenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eb7b6-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="eb7b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb7b6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb7b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7b6-106">Połączenie bramy sieci wirtualnej to obiekt reprezentujący tunel IPsec (lokacja-lokacja lub Sieć wirtualna-wirtualna) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7b6-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="eb7b6-107">Polecenie cmdlet **Get-AzVirtualNetworkGatewayConnection** zwraca obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb7b6-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="eb7b6-108">Jeśli polecenie cmdlet **Get-AzVirtualNetworkGatewayConnection** jest wystawiane bez określenia parametru-name, dane wyjściowe nie będą wyświetlane ConnectionStatus i SharedKey szczegółów.</span><span class="sxs-lookup"><span data-stu-id="eb7b6-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="eb7b6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb7b6-109">EXAMPLES</span></span>

### <span data-ttu-id="eb7b6-110">1: uzyskiwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eb7b6-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="eb7b6-111">Zwraca obiekt połączenia bramy sieci wirtualnej o nazwie "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="eb7b6-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="eb7b6-112">2: uzyskiwanie wszystkich połączeń bramy sieci wirtualnej przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="eb7b6-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="eb7b6-113">Zwraca wszystkie połączenia bramy sieci wirtualnej, które zaczynają się od ciągu "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="eb7b6-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="eb7b6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb7b6-114">PARAMETERS</span></span>

### <span data-ttu-id="eb7b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7b6-115">-DefaultProfile</span></span>
<span data-ttu-id="eb7b6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb7b6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb7b6-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="eb7b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7b6-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="eb7b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7b6-119">CommonParameters</span></span>
<span data-ttu-id="eb7b6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7b6-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb7b6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7b6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb7b6-122">INPUTS</span></span>

### <span data-ttu-id="eb7b6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7b6-123">System.String</span></span>

## <span data-ttu-id="eb7b6-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb7b6-124">OUTPUTS</span></span>

### <span data-ttu-id="eb7b6-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb7b6-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="eb7b6-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb7b6-126">NOTES</span></span>

## <span data-ttu-id="eb7b6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb7b6-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb7b6-128">Nowe — AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb7b6-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="eb7b6-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb7b6-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="eb7b6-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eb7b6-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
