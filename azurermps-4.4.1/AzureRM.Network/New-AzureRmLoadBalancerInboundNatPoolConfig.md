---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 85d58154d8dd1d93e37a55b9fd0b9d306283b899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553196"
---
# <span data-ttu-id="4fbb8-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4fbb8-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="4fbb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fbb8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fbb8-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fbb8-103">SYNTAX</span></span>

### <span data-ttu-id="4fbb8-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fbb8-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbb8-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4fbb8-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fbb8-106">Opis</span><span class="sxs-lookup"><span data-stu-id="4fbb8-106">DESCRIPTION</span></span>

## <span data-ttu-id="4fbb8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fbb8-107">EXAMPLES</span></span>

## <span data-ttu-id="4fbb8-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fbb8-108">PARAMETERS</span></span>

### <span data-ttu-id="4fbb8-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4fbb8-109">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-110">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fbb8-110">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-111">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4fbb8-111">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-112">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="4fbb8-112">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-113">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="4fbb8-113">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fbb8-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-115">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="4fbb8-115">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fbb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbb8-116">-DefaultProfile</span></span>
<span data-ttu-id="4fbb8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fbb8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fbb8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbb8-118">CommonParameters</span></span>
<span data-ttu-id="4fbb8-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fbb8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbb8-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbb8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbb8-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fbb8-121">INPUTS</span></span>

## <span data-ttu-id="4fbb8-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fbb8-122">OUTPUTS</span></span>

### <span data-ttu-id="4fbb8-123">Microsoft. Azure. Commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="4fbb8-123">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="4fbb8-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fbb8-124">NOTES</span></span>

## <span data-ttu-id="4fbb8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fbb8-125">RELATED LINKS</span></span>

