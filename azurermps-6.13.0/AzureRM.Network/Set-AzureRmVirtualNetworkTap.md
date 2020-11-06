---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553475"
---
# <span data-ttu-id="19e04-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="19e04-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="19e04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19e04-102">SYNOPSIS</span></span>
<span data-ttu-id="19e04-103">Ustawia stan celu dla sieci wirtualnej TAP.</span><span class="sxs-lookup"><span data-stu-id="19e04-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19e04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19e04-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19e04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19e04-105">DESCRIPTION</span></span>
<span data-ttu-id="19e04-106">**Zestaw-AzureRmVirtualNetworkTap** ustawia stan celu dla sieci wirtualnej usługi Azure Network.</span><span class="sxs-lookup"><span data-stu-id="19e04-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="19e04-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19e04-107">EXAMPLES</span></span>

### <span data-ttu-id="19e04-108">Przykład 1: Konfigurowanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="19e04-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="19e04-109">Polecenie aktualizuje docelowy element IpConfiguration i aktualizuje naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19e04-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="19e04-110">W przypadku jakichkolwiek odwołujących się do niej konfiguracji, nie zostanie on uruchomiony jako dublowany do nowej aktualizacji docelowa Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="19e04-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="19e04-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19e04-111">PARAMETERS</span></span>

### <span data-ttu-id="19e04-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19e04-112">-AsJob</span></span>
<span data-ttu-id="19e04-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="19e04-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19e04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e04-114">-DefaultProfile</span></span>
<span data-ttu-id="19e04-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19e04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e04-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="19e04-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="19e04-117">Sieć wirtualna, naciśnij</span><span class="sxs-lookup"><span data-stu-id="19e04-117">The virtual network tap</span></span>

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

### <span data-ttu-id="19e04-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19e04-118">-Confirm</span></span>
<span data-ttu-id="19e04-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e04-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e04-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e04-120">-WhatIf</span></span>
<span data-ttu-id="19e04-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e04-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19e04-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19e04-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e04-123">CommonParameters</span></span>
<span data-ttu-id="19e04-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e04-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e04-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e04-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19e04-126">INPUTS</span></span>

### <span data-ttu-id="19e04-127">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="19e04-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="19e04-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19e04-128">OUTPUTS</span></span>

### <span data-ttu-id="19e04-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="19e04-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="19e04-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19e04-130">NOTES</span></span>

## <span data-ttu-id="19e04-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19e04-131">RELATED LINKS</span></span>
