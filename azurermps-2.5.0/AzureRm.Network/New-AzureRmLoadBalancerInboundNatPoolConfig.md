---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898281"
---
# <span data-ttu-id="b4d7a-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b4d7a-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b4d7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4d7a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4d7a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4d7a-103">SYNTAX</span></span>

### <span data-ttu-id="b4d7a-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d7a-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d7a-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4d7a-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4d7a-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b4d7a-106">DESCRIPTION</span></span>

## <span data-ttu-id="b4d7a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4d7a-107">EXAMPLES</span></span>

### <span data-ttu-id="b4d7a-108">1:1</span><span class="sxs-lookup"><span data-stu-id="b4d7a-108">1:</span></span>
```

```

## <span data-ttu-id="b4d7a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4d7a-109">PARAMETERS</span></span>

### <span data-ttu-id="b4d7a-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b4d7a-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d7a-111">-DefaultProfile</span></span>
<span data-ttu-id="b4d7a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d7a-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d7a-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d7a-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4d7a-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d7a-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="b4d7a-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d7a-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="b4d7a-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d7a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4d7a-117">-Name</span></span>
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

### <span data-ttu-id="b4d7a-118">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b4d7a-118">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d7a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d7a-119">CommonParameters</span></span>
<span data-ttu-id="b4d7a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d7a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d7a-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d7a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d7a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4d7a-122">INPUTS</span></span>

## <span data-ttu-id="b4d7a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4d7a-123">OUTPUTS</span></span>

### <span data-ttu-id="b4d7a-124">Microsoft. Azure. Commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="b4d7a-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="b4d7a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4d7a-125">NOTES</span></span>

## <span data-ttu-id="b4d7a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4d7a-126">RELATED LINKS</span></span>

