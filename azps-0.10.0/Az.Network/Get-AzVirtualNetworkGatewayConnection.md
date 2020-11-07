---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890646"
---
# <span data-ttu-id="d5f30-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5f30-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d5f30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5f30-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f30-103">Pobiera połączenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d5f30-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="d5f30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5f30-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5f30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5f30-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f30-106">Połączenie bramy sieci wirtualnej to obiekt reprezentujący tunel IPsec (lokacja-lokacja lub Sieć wirtualna-wirtualna) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f30-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="d5f30-107">Polecenie cmdlet **Get-AzVirtualNetworkGatewayConnection** zwraca obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5f30-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d5f30-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5f30-108">EXAMPLES</span></span>

### <span data-ttu-id="d5f30-109">1: uzyskiwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d5f30-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="d5f30-110">Zwraca obiekt połączenia bramy sieci wirtualnej o nazwie "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="d5f30-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="d5f30-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5f30-111">PARAMETERS</span></span>

### <span data-ttu-id="d5f30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f30-112">-DefaultProfile</span></span>
<span data-ttu-id="d5f30-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f30-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5f30-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f30-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f30-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f30-116">CommonParameters</span></span>
<span data-ttu-id="d5f30-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f30-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f30-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f30-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f30-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5f30-119">INPUTS</span></span>

## <span data-ttu-id="d5f30-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5f30-120">OUTPUTS</span></span>

### <span data-ttu-id="d5f30-121">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d5f30-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d5f30-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5f30-122">NOTES</span></span>

## <span data-ttu-id="d5f30-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5f30-123">RELATED LINKS</span></span>

