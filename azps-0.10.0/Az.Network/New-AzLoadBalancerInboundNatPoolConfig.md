---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9a6879d2b5ad18c33ca53befd94d5e8dc03225df
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890486"
---
# <span data-ttu-id="fa8e7-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fa8e7-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="fa8e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa8e7-102">SYNOPSIS</span></span>

## <span data-ttu-id="fa8e7-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa8e7-103">SYNTAX</span></span>

### <span data-ttu-id="fa8e7-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa8e7-104">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa8e7-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fa8e7-105">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa8e7-106">Opis</span><span class="sxs-lookup"><span data-stu-id="fa8e7-106">DESCRIPTION</span></span>

## <span data-ttu-id="fa8e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="fa8e7-108">1:1</span><span class="sxs-lookup"><span data-stu-id="fa8e7-108">1:</span></span>
```

```

## <span data-ttu-id="fa8e7-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa8e7-109">PARAMETERS</span></span>

### <span data-ttu-id="fa8e7-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fa8e7-110">-BackendPort</span></span>
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

### <span data-ttu-id="fa8e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa8e7-111">-DefaultProfile</span></span>
<span data-ttu-id="fa8e7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa8e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa8e7-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa8e7-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="fa8e7-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fa8e7-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="fa8e7-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="fa8e7-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="fa8e7-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="fa8e7-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="fa8e7-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa8e7-117">-Name</span></span>
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

### <span data-ttu-id="fa8e7-118">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="fa8e7-118">-Protocol</span></span>
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

### <span data-ttu-id="fa8e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa8e7-119">CommonParameters</span></span>
<span data-ttu-id="fa8e7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa8e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa8e7-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa8e7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa8e7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa8e7-122">INPUTS</span></span>

## <span data-ttu-id="fa8e7-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa8e7-123">OUTPUTS</span></span>

### <span data-ttu-id="fa8e7-124">Microsoft. Azure. Commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="fa8e7-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="fa8e7-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa8e7-125">NOTES</span></span>

## <span data-ttu-id="fa8e7-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa8e7-126">RELATED LINKS</span></span>

