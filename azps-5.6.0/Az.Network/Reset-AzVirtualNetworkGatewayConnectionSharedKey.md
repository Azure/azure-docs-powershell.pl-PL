---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 6b2121c581d3d7da990813884cf0097064b73f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979546"
---
# <span data-ttu-id="14834-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="14834-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="14834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14834-102">SYNOPSIS</span></span>
<span data-ttu-id="14834-103">Resetuje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="14834-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="14834-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14834-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14834-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14834-105">DESCRIPTION</span></span>
<span data-ttu-id="14834-106">Resetuje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="14834-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="14834-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14834-107">EXAMPLES</span></span>

### <span data-ttu-id="14834-108">Przykład 1.</span><span class="sxs-lookup"><span data-stu-id="14834-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="14834-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14834-109">PARAMETERS</span></span>

### <span data-ttu-id="14834-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14834-110">-DefaultProfile</span></span>
<span data-ttu-id="14834-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14834-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14834-112">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="14834-112">-Force</span></span>
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

### <span data-ttu-id="14834-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="14834-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14834-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14834-114">-Name</span></span>
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

### <span data-ttu-id="14834-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14834-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="14834-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14834-116">-Confirm</span></span>
<span data-ttu-id="14834-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14834-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14834-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14834-118">-WhatIf</span></span>
<span data-ttu-id="14834-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14834-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14834-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="14834-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14834-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14834-121">CommonParameters</span></span>
<span data-ttu-id="14834-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14834-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14834-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14834-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14834-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14834-124">INPUTS</span></span>

### <span data-ttu-id="14834-125">System.String</span><span class="sxs-lookup"><span data-stu-id="14834-125">System.String</span></span>

### <span data-ttu-id="14834-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="14834-126">System.UInt32</span></span>

## <span data-ttu-id="14834-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14834-127">OUTPUTS</span></span>

### <span data-ttu-id="14834-128">System.String</span><span class="sxs-lookup"><span data-stu-id="14834-128">System.String</span></span>

## <span data-ttu-id="14834-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14834-129">NOTES</span></span>

## <span data-ttu-id="14834-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14834-130">RELATED LINKS</span></span>

[<span data-ttu-id="14834-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="14834-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="14834-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="14834-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
