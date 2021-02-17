---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191570"
---
# <span data-ttu-id="6a110-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="6a110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a110-102">SYNOPSIS</span></span>
<span data-ttu-id="6a110-103">Aktualizuje dotknięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a110-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="6a110-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a110-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a110-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a110-105">DESCRIPTION</span></span>
<span data-ttu-id="6a110-106">Polecenie **cmdlet Set-AzVirtualNetworkTap** aktualizuje naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a110-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="6a110-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a110-107">EXAMPLES</span></span>

### <span data-ttu-id="6a110-108">Przykład 1. Konfigurowanie naciśnięcia sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6a110-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="6a110-109">Polecenie aktualizuje docelową konfigurację IpConfiguration i aktualizuje naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a110-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="6a110-110">Jeśli istnieją jakiekolwiek konfiguracje typu tap odwołujące się do niego, po aktualizacji nie rozpocznie się dublowanie całego ruchu źródłowego do nowej konfiguracji adresu IP lokalizacji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6a110-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="6a110-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a110-111">PARAMETERS</span></span>

### <span data-ttu-id="6a110-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6a110-112">-AsJob</span></span>
<span data-ttu-id="6a110-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6a110-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a110-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a110-114">-DefaultProfile</span></span>
<span data-ttu-id="6a110-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a110-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a110-116">— VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="6a110-117">Sieć wirtualna naciska</span><span class="sxs-lookup"><span data-stu-id="6a110-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a110-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a110-118">-Confirm</span></span>
<span data-ttu-id="6a110-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a110-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a110-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a110-120">-WhatIf</span></span>
<span data-ttu-id="6a110-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a110-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a110-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6a110-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a110-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a110-123">CommonParameters</span></span>
<span data-ttu-id="6a110-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a110-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a110-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a110-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a110-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a110-126">INPUTS</span></span>

### <span data-ttu-id="6a110-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="6a110-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a110-128">OUTPUTS</span></span>

### <span data-ttu-id="6a110-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="6a110-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a110-130">NOTES</span></span>

## <span data-ttu-id="6a110-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a110-131">RELATED LINKS</span></span>

[<span data-ttu-id="6a110-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="6a110-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="6a110-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a110-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
