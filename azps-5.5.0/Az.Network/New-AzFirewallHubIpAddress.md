---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189682"
---
# <span data-ttu-id="86987-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="86987-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="86987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86987-102">SYNOPSIS</span></span>
<span data-ttu-id="86987-103">Adresy IP assoicated do zapory w centrum wirtualnym</span><span class="sxs-lookup"><span data-stu-id="86987-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="86987-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="86987-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86987-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="86987-105">DESCRIPTION</span></span>
<span data-ttu-id="86987-106">Adresy IP assoicated do zapory w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="86987-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="86987-107">Mogą to być adresy publiczne i prywatne</span><span class="sxs-lookup"><span data-stu-id="86987-107">These can be public and private addresses</span></span>

## <span data-ttu-id="86987-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="86987-108">EXAMPLES</span></span>

### <span data-ttu-id="86987-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86987-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="86987-110">W tym przykładzie jest tworzenie obiektu adresu IP Centrum z zliczaną 2 publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="86987-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="86987-111">Obiekt HubIPAddress jest skojarzony z zaporą w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="86987-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="86987-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86987-112">PARAMETERS</span></span>

### <span data-ttu-id="86987-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86987-113">-DefaultProfile</span></span>
<span data-ttu-id="86987-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="86987-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86987-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="86987-115">-PrivateIPAddress</span></span>
<span data-ttu-id="86987-116">Prywatny adres IP zapory dołączonej do centrum</span><span class="sxs-lookup"><span data-stu-id="86987-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="86987-117">- PublicIPs</span><span class="sxs-lookup"><span data-stu-id="86987-117">-PublicIPs</span></span>
<span data-ttu-id="86987-118">Adresy IP zapory podłączonej do centrum</span><span class="sxs-lookup"><span data-stu-id="86987-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="86987-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86987-119">-Confirm</span></span>
<span data-ttu-id="86987-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="86987-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86987-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86987-121">-WhatIf</span></span>
<span data-ttu-id="86987-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86987-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86987-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="86987-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86987-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86987-124">CommonParameters</span></span>
<span data-ttu-id="86987-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86987-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86987-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86987-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86987-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86987-127">INPUTS</span></span>

### <span data-ttu-id="86987-128">Brak</span><span class="sxs-lookup"><span data-stu-id="86987-128">None</span></span>

## <span data-ttu-id="86987-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86987-129">OUTPUTS</span></span>

### <span data-ttu-id="86987-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="86987-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="86987-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="86987-131">NOTES</span></span>

## <span data-ttu-id="86987-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86987-132">RELATED LINKS</span></span>
