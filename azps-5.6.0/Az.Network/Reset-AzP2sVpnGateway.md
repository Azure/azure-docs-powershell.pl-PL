---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: c813f5d5921f0291174a77cf6cdc4b0a1f7ee6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958161"
---
# <span data-ttu-id="f4275-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="f4275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4275-102">SYNOPSIS</span></span>
<span data-ttu-id="f4275-103">Resetuje skalowalną bramę SIECI VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="f4275-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="f4275-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4275-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4275-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f4275-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4275-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f4275-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4275-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f4275-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4275-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4275-108">DESCRIPTION</span></span>
<span data-ttu-id="f4275-109">Resetuje bramę P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="f4275-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4275-110">EXAMPLES</span></span>

### <span data-ttu-id="f4275-111">Przykład 1.</span><span class="sxs-lookup"><span data-stu-id="f4275-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="f4275-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4275-112">PARAMETERS</span></span>

### <span data-ttu-id="f4275-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f4275-113">-AsJob</span></span>
<span data-ttu-id="f4275-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f4275-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4275-115">-DefaultProfile</span></span>
<span data-ttu-id="f4275-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4275-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4275-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="f4275-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4275-118">CommonParameters</span></span>
<span data-ttu-id="f4275-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4275-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4275-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4275-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4275-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4275-121">INPUTS</span></span>

### <span data-ttu-id="f4275-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="f4275-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f4275-123">System.String</span></span>

## <span data-ttu-id="f4275-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4275-124">OUTPUTS</span></span>

### <span data-ttu-id="f4275-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="f4275-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4275-126">NOTES</span></span>

## <span data-ttu-id="f4275-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4275-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4275-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="f4275-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="f4275-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="f4275-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4275-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
