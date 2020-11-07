---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898358"
---
# <span data-ttu-id="f06c7-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f06c7-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f06c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f06c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f06c7-103">Pobiera bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f06c7-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f06c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f06c7-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f06c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f06c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f06c7-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f06c7-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="f06c7-107">Polecenie cmdlet **Get-AzureRmVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f06c7-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f06c7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f06c7-108">EXAMPLES</span></span>

### <span data-ttu-id="f06c7-109">1: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f06c7-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f06c7-110">Zwraca obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="f06c7-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f06c7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f06c7-111">PARAMETERS</span></span>

### <span data-ttu-id="f06c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06c7-112">-DefaultProfile</span></span>
<span data-ttu-id="f06c7-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f06c7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f06c7-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f06c7-114">-Name</span></span>
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

### <span data-ttu-id="f06c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f06c7-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f06c7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06c7-116">CommonParameters</span></span>
<span data-ttu-id="f06c7-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f06c7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06c7-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f06c7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06c7-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f06c7-119">INPUTS</span></span>

## <span data-ttu-id="f06c7-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f06c7-120">OUTPUTS</span></span>

### <span data-ttu-id="f06c7-121">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f06c7-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f06c7-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f06c7-122">NOTES</span></span>

## <span data-ttu-id="f06c7-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f06c7-123">RELATED LINKS</span></span>

