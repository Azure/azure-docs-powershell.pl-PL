---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 80bb8e05b110f1b3e9689895ae9bea2aad1207b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870592"
---
# <span data-ttu-id="d930d-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="d930d-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="d930d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d930d-102">SYNOPSIS</span></span>
<span data-ttu-id="d930d-103">Wyświetla trasy rozpoznane przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d930d-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="d930d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d930d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d930d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d930d-105">DESCRIPTION</span></span>
<span data-ttu-id="d930d-106">Wylicza trasy rozpoznane przez bramę sieci wirtualnej platformy Azure z różnych źródeł.</span><span class="sxs-lookup"><span data-stu-id="d930d-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="d930d-107">Obejmuje to trasy rozpoznane za pośrednictwem protokołu BGP, a także trasy statyczne.</span><span class="sxs-lookup"><span data-stu-id="d930d-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="d930d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d930d-108">EXAMPLES</span></span>

### <span data-ttu-id="d930d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d930d-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="d930d-110">W przypadku bramy usługi Azure Virtual Network o nazwie gatewayname w grupie Resource Group (zasób wirtualny platformy Azure) są pobierane trasy z tej bramy.</span><span class="sxs-lookup"><span data-stu-id="d930d-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="d930d-111">Brama sieci wirtualnej platformy Azure w tym przypadku ma dwie trasy statyczne (10.1.0.0/16 oraz 10.0.0.254/32), a także o jednej trasie uzyskanej za pośrednictwem protokołu BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="d930d-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="d930d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d930d-112">PARAMETERS</span></span>

### <span data-ttu-id="d930d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d930d-113">-AsJob</span></span>
<span data-ttu-id="d930d-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d930d-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d930d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d930d-115">-DefaultProfile</span></span>
<span data-ttu-id="d930d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d930d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d930d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d930d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d930d-118">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d930d-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d930d-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d930d-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d930d-120">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d930d-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="d930d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d930d-121">CommonParameters</span></span>
<span data-ttu-id="d930d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d930d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d930d-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d930d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d930d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d930d-124">INPUTS</span></span>

### <span data-ttu-id="d930d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d930d-125">System.String</span></span>

## <span data-ttu-id="d930d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d930d-126">OUTPUTS</span></span>

### <span data-ttu-id="d930d-127">Microsoft. Azure. Commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="d930d-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="d930d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d930d-128">NOTES</span></span>

## <span data-ttu-id="d930d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d930d-129">RELATED LINKS</span></span>
