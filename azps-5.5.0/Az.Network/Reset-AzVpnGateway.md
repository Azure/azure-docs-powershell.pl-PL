---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184251"
---
# <span data-ttu-id="a3146-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="a3146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3146-102">SYNOPSIS</span></span>
<span data-ttu-id="a3146-103">Resetuje skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="a3146-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="a3146-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3146-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3146-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a3146-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3146-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a3146-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3146-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a3146-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3146-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3146-108">DESCRIPTION</span></span>
<span data-ttu-id="a3146-109">Resetuje sieć VpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="a3146-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3146-110">EXAMPLES</span></span>

### <span data-ttu-id="a3146-111">Przykład 1.</span><span class="sxs-lookup"><span data-stu-id="a3146-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="a3146-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3146-112">PARAMETERS</span></span>

### <span data-ttu-id="a3146-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a3146-113">-AsJob</span></span>
<span data-ttu-id="a3146-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a3146-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3146-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3146-115">-DefaultProfile</span></span>
<span data-ttu-id="a3146-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3146-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3146-117">- VpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-117">-VpnGateway</span></span>
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

### <span data-ttu-id="a3146-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3146-118">CommonParameters</span></span>
<span data-ttu-id="a3146-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3146-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3146-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3146-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3146-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3146-121">INPUTS</span></span>

### <span data-ttu-id="a3146-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="a3146-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a3146-123">System.String</span></span>

## <span data-ttu-id="a3146-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3146-124">OUTPUTS</span></span>

### <span data-ttu-id="a3146-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="a3146-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3146-126">NOTES</span></span>

## <span data-ttu-id="a3146-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3146-127">RELATED LINKS</span></span>

[<span data-ttu-id="a3146-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="a3146-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="a3146-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="a3146-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3146-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
