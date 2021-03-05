---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: 333e245b77869903b74973a4f851d020d70c0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985825"
---
# <span data-ttu-id="1292f-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="1292f-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="1292f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1292f-102">SYNOPSIS</span></span>
<span data-ttu-id="1292f-103">Adresy IP assoicated do zapory w centrum wirtualnym</span><span class="sxs-lookup"><span data-stu-id="1292f-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="1292f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1292f-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1292f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1292f-105">DESCRIPTION</span></span>
<span data-ttu-id="1292f-106">Adresy IP assoicated do zapory w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="1292f-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="1292f-107">Mogą to być adresy publiczne i prywatne</span><span class="sxs-lookup"><span data-stu-id="1292f-107">These can be public and private addresses</span></span>

## <span data-ttu-id="1292f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1292f-108">EXAMPLES</span></span>

### <span data-ttu-id="1292f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1292f-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="1292f-110">W tym przykładzie jest tworzenie obiektu adresu IP centrum z liczną 2 publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="1292f-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="1292f-111">Obiekt HubIPAddress jest skojarzony z zaporą w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="1292f-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="1292f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1292f-112">PARAMETERS</span></span>

### <span data-ttu-id="1292f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1292f-113">-DefaultProfile</span></span>
<span data-ttu-id="1292f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1292f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1292f-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="1292f-115">-PrivateIPAddress</span></span>
<span data-ttu-id="1292f-116">Prywatny adres IP zapory dołączonej do centrum</span><span class="sxs-lookup"><span data-stu-id="1292f-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="1292f-117">— PublicIPs</span><span class="sxs-lookup"><span data-stu-id="1292f-117">-PublicIPs</span></span>
<span data-ttu-id="1292f-118">Adresy IP zapory podłączonej do centrum</span><span class="sxs-lookup"><span data-stu-id="1292f-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1292f-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1292f-119">-Confirm</span></span>
<span data-ttu-id="1292f-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1292f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1292f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1292f-121">-WhatIf</span></span>
<span data-ttu-id="1292f-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1292f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1292f-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1292f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1292f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1292f-124">CommonParameters</span></span>
<span data-ttu-id="1292f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1292f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1292f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1292f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1292f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1292f-127">INPUTS</span></span>

### <span data-ttu-id="1292f-128">Brak</span><span class="sxs-lookup"><span data-stu-id="1292f-128">None</span></span>

## <span data-ttu-id="1292f-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1292f-129">OUTPUTS</span></span>

### <span data-ttu-id="1292f-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="1292f-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="1292f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1292f-131">NOTES</span></span>

## <span data-ttu-id="1292f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1292f-132">RELATED LINKS</span></span>
