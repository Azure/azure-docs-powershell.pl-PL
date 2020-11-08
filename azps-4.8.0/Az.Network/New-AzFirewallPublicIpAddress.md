---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220551"
---
# <span data-ttu-id="89877-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89877-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="89877-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89877-102">SYNOPSIS</span></span>
<span data-ttu-id="89877-103">Jest to symbol zastępczy adresu IP, którego można użyć do obsługi wielopip (Zapora Azure).</span><span class="sxs-lookup"><span data-stu-id="89877-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="89877-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89877-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89877-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89877-105">DESCRIPTION</span></span>
<span data-ttu-id="89877-106">Jest to symbol zastępczy adresu IP, którego można użyć do obsługi wielopip (Zapora Azure).</span><span class="sxs-lookup"><span data-stu-id="89877-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="89877-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89877-107">EXAMPLES</span></span>

### <span data-ttu-id="89877-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89877-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="89877-109">$publicIp będzie symbolem zastępczym adresu IP 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="89877-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="89877-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89877-110">PARAMETERS</span></span>

### <span data-ttu-id="89877-111">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="89877-111">-Address</span></span>
<span data-ttu-id="89877-112">Adresy IP zapory podłączonej do koncentratora</span><span class="sxs-lookup"><span data-stu-id="89877-112">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89877-113">-DefaultProfile</span></span>
<span data-ttu-id="89877-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89877-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89877-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89877-115">-Confirm</span></span>
<span data-ttu-id="89877-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89877-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89877-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89877-117">-WhatIf</span></span>
<span data-ttu-id="89877-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89877-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89877-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89877-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89877-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89877-120">CommonParameters</span></span>
<span data-ttu-id="89877-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89877-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89877-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89877-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89877-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89877-123">INPUTS</span></span>

### <span data-ttu-id="89877-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="89877-124">None</span></span>

## <span data-ttu-id="89877-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89877-125">OUTPUTS</span></span>

### <span data-ttu-id="89877-126">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89877-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="89877-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89877-127">NOTES</span></span>

## <span data-ttu-id="89877-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89877-128">RELATED LINKS</span></span>
