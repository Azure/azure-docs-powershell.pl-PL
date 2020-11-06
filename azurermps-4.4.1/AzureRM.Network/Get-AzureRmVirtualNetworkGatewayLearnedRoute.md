---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: b6a4899fb54ffc4305f6b512046e00bda994b02e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546924"
---
# <span data-ttu-id="33e99-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="33e99-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="33e99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33e99-102">SYNOPSIS</span></span>
<span data-ttu-id="33e99-103">Wyświetla trasy rozpoznane przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="33e99-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33e99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33e99-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33e99-105">DESCRIPTION</span></span>
<span data-ttu-id="33e99-106">Wylicza trasy rozpoznane przez bramę sieci wirtualnej platformy Azure z różnych źródeł.</span><span class="sxs-lookup"><span data-stu-id="33e99-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="33e99-107">Obejmuje to trasy rozpoznane za pośrednictwem protokołu BGP, a także trasy statyczne.</span><span class="sxs-lookup"><span data-stu-id="33e99-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="33e99-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33e99-108">EXAMPLES</span></span>

### <span data-ttu-id="33e99-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33e99-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="33e99-110">W przypadku bramy usługi Azure Virtual Network o nazwie gatewayname w grupie Resource Group (zasób wirtualny platformy Azure) są pobierane trasy z tej bramy.</span><span class="sxs-lookup"><span data-stu-id="33e99-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="33e99-111">Brama sieci wirtualnej platformy Azure w tym przypadku ma dwie trasy statyczne (10.1.0.0/16 oraz 10.0.0.254/32), a także o jednej trasie uzyskanej za pośrednictwem protokołu BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="33e99-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="33e99-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33e99-112">PARAMETERS</span></span>

### <span data-ttu-id="33e99-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e99-113">-ResourceGroupName</span></span>
<span data-ttu-id="33e99-114">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="33e99-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="33e99-115">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="33e99-115">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="33e99-116">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="33e99-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e99-117">-DefaultProfile</span></span>
<span data-ttu-id="33e99-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33e99-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e99-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e99-119">CommonParameters</span></span>
<span data-ttu-id="33e99-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e99-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e99-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e99-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e99-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33e99-122">INPUTS</span></span>

### <span data-ttu-id="33e99-123">System. String</span><span class="sxs-lookup"><span data-stu-id="33e99-123">System.String</span></span>

## <span data-ttu-id="33e99-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33e99-124">OUTPUTS</span></span>

### <span data-ttu-id="33e99-125">Microsoft. Azure. Commands. Network. models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="33e99-125">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="33e99-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33e99-126">NOTES</span></span>

## <span data-ttu-id="33e99-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33e99-127">RELATED LINKS</span></span>

