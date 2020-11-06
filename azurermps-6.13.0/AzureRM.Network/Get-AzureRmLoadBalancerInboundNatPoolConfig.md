---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbd49a948108d23c0f824adaea2e06105152a36b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547484"
---
# <span data-ttu-id="e583f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e583f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e583f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e583f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e583f-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e583f-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e583f-104">Opis</span><span class="sxs-lookup"><span data-stu-id="e583f-104">DESCRIPTION</span></span>

## <span data-ttu-id="e583f-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e583f-105">EXAMPLES</span></span>

### <span data-ttu-id="e583f-106">1: Uzyskaj</span><span class="sxs-lookup"><span data-stu-id="e583f-106">1: Get</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzureRmLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="e583f-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e583f-107">PARAMETERS</span></span>

### <span data-ttu-id="e583f-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e583f-108">-DefaultProfile</span></span>
<span data-ttu-id="e583f-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e583f-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e583f-110">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e583f-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e583f-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e583f-111">-Name</span></span>
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

### <span data-ttu-id="e583f-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e583f-112">CommonParameters</span></span>
<span data-ttu-id="e583f-113">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e583f-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e583f-114">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e583f-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e583f-115">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e583f-115">INPUTS</span></span>

### <span data-ttu-id="e583f-116">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e583f-116">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e583f-117">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e583f-117">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="e583f-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e583f-118">OUTPUTS</span></span>

### <span data-ttu-id="e583f-119">Microsoft. Azure. Commands. Network. models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="e583f-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="e583f-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e583f-120">NOTES</span></span>

## <span data-ttu-id="e583f-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e583f-121">RELATED LINKS</span></span>
