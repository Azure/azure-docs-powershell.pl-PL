---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063291"
---
# <span data-ttu-id="2b694-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="2b694-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b694-102">SYNOPSIS</span></span>
<span data-ttu-id="2b694-103">Umożliwia zaktualizowanie naciśnięcia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2b694-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="2b694-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b694-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b694-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b694-105">DESCRIPTION</span></span>
<span data-ttu-id="2b694-106">Polecenie cmdlet **Set-AzVirtualNetworkTap** umożliwia zaktualizowanie naciśnięcia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2b694-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="2b694-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b694-107">EXAMPLES</span></span>

### <span data-ttu-id="2b694-108">Przykład 1: Konfigurowanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2b694-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="2b694-109">Polecenie aktualizuje docelowy element IpConfiguration i aktualizuje naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2b694-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="2b694-110">W przypadku jakichkolwiek odwołujących się do niej konfiguracji, nie zostanie on uruchomiony jako dublowany do nowej aktualizacji docelowa Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="2b694-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="2b694-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b694-111">PARAMETERS</span></span>

### <span data-ttu-id="2b694-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b694-112">-AsJob</span></span>
<span data-ttu-id="2b694-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2b694-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b694-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b694-114">-DefaultProfile</span></span>
<span data-ttu-id="2b694-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b694-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b694-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="2b694-117">Sieć wirtualna, naciśnij</span><span class="sxs-lookup"><span data-stu-id="2b694-117">The virtual network tap</span></span>

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

### <span data-ttu-id="2b694-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b694-118">-Confirm</span></span>
<span data-ttu-id="2b694-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b694-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b694-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b694-120">-WhatIf</span></span>
<span data-ttu-id="2b694-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b694-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b694-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b694-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b694-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b694-123">CommonParameters</span></span>
<span data-ttu-id="2b694-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b694-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b694-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b694-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b694-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b694-126">INPUTS</span></span>

### <span data-ttu-id="2b694-127">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2b694-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b694-128">OUTPUTS</span></span>

### <span data-ttu-id="2b694-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2b694-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b694-130">NOTES</span></span>

## <span data-ttu-id="2b694-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b694-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b694-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="2b694-133">Nowe — AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="2b694-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2b694-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
