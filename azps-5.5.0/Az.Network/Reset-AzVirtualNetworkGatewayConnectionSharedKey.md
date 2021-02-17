---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184259"
---
# <span data-ttu-id="a79a4-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a79a4-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a79a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a79a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a79a4-103">Resetuje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a79a4-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="a79a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a79a4-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79a4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a79a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a79a4-106">Resetuje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a79a4-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="a79a4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a79a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a79a4-108">Przykład 1.</span><span class="sxs-lookup"><span data-stu-id="a79a4-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="a79a4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a79a4-109">PARAMETERS</span></span>

### <span data-ttu-id="a79a4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79a4-110">-DefaultProfile</span></span>
<span data-ttu-id="a79a4-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a79a4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a79a4-112">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a79a4-112">-Force</span></span>
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

### <span data-ttu-id="a79a4-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="a79a4-113">-KeyLength</span></span>
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

### <span data-ttu-id="a79a4-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a79a4-114">-Name</span></span>
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

### <span data-ttu-id="a79a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79a4-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a79a4-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a79a4-116">-Confirm</span></span>
<span data-ttu-id="a79a4-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a79a4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a79a4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79a4-118">-WhatIf</span></span>
<span data-ttu-id="a79a4-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a79a4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a79a4-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a79a4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a79a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79a4-121">CommonParameters</span></span>
<span data-ttu-id="a79a4-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79a4-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79a4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79a4-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a79a4-124">INPUTS</span></span>

### <span data-ttu-id="a79a4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a79a4-125">System.String</span></span>

### <span data-ttu-id="a79a4-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="a79a4-126">System.UInt32</span></span>

## <span data-ttu-id="a79a4-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a79a4-127">OUTPUTS</span></span>

### <span data-ttu-id="a79a4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a79a4-128">System.String</span></span>

## <span data-ttu-id="a79a4-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a79a4-129">NOTES</span></span>

## <span data-ttu-id="a79a4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a79a4-130">RELATED LINKS</span></span>

[<span data-ttu-id="a79a4-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a79a4-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a79a4-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a79a4-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
