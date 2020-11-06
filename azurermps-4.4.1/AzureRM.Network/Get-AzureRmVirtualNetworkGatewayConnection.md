---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3d58e2f9fbd62826084df329cd7047a293ef0291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546947"
---
# <span data-ttu-id="0ce5d-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ce5d-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0ce5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ce5d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce5d-103">Pobiera połączenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0ce5d-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ce5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ce5d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ce5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ce5d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce5d-106">Połączenie bramy sieci wirtualnej to obiekt reprezentujący tunel IPsec (lokacja-lokacja lub Sieć wirtualna-wirtualna) połączony z wirtualną bramą sieciową na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce5d-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="0ce5d-107">Polecenie cmdlet **Get-AzureRmVirtualNetworkGatewayConnection** zwraca obiekt połączenia na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ce5d-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="0ce5d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ce5d-108">EXAMPLES</span></span>

### <span data-ttu-id="0ce5d-109">1: uzyskiwanie połączenia bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0ce5d-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="0ce5d-110">Zwraca obiekt połączenia bramy sieci wirtualnej o nazwie "mój tunel" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="0ce5d-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="0ce5d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ce5d-111">PARAMETERS</span></span>

### <span data-ttu-id="0ce5d-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ce5d-112">-Name</span></span>
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

### <span data-ttu-id="0ce5d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce5d-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0ce5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce5d-114">-DefaultProfile</span></span>
<span data-ttu-id="0ce5d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce5d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce5d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce5d-116">CommonParameters</span></span>
<span data-ttu-id="0ce5d-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce5d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce5d-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce5d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce5d-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ce5d-119">INPUTS</span></span>

## <span data-ttu-id="0ce5d-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ce5d-120">OUTPUTS</span></span>

### <span data-ttu-id="0ce5d-121">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0ce5d-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0ce5d-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ce5d-122">NOTES</span></span>

## <span data-ttu-id="0ce5d-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ce5d-123">RELATED LINKS</span></span>

