---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063329"
---
# <span data-ttu-id="39738-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="39738-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39738-102">SYNOPSIS</span></span>
<span data-ttu-id="39738-103">Umożliwia zresetowanie bramy sieci VPN skalowalnego P2S.</span><span class="sxs-lookup"><span data-stu-id="39738-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="39738-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39738-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39738-105">ByP2SVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39738-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39738-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="39738-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39738-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="39738-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39738-108">Opis</span><span class="sxs-lookup"><span data-stu-id="39738-108">DESCRIPTION</span></span>
<span data-ttu-id="39738-109">Resetowanie P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="39738-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39738-110">EXAMPLES</span></span>

### <span data-ttu-id="39738-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="39738-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="39738-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39738-112">PARAMETERS</span></span>

### <span data-ttu-id="39738-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39738-113">-AsJob</span></span>
<span data-ttu-id="39738-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="39738-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39738-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39738-115">-DefaultProfile</span></span>
<span data-ttu-id="39738-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39738-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39738-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-117">-P2SVpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39738-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39738-118">CommonParameters</span></span>
<span data-ttu-id="39738-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39738-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39738-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39738-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39738-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39738-121">INPUTS</span></span>

### <span data-ttu-id="39738-122">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="39738-123">System. String</span><span class="sxs-lookup"><span data-stu-id="39738-123">System.String</span></span>

## <span data-ttu-id="39738-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39738-124">OUTPUTS</span></span>

### <span data-ttu-id="39738-125">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="39738-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39738-126">NOTES</span></span>

## <span data-ttu-id="39738-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39738-127">RELATED LINKS</span></span>

[<span data-ttu-id="39738-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="39738-129">Nowe — AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="39738-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="39738-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39738-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
