---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232794"
---
# <span data-ttu-id="fcf6e-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="fcf6e-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="fcf6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf6e-103">Adresy IP assoicated do zapory na wirtualnym koncentratorze</span><span class="sxs-lookup"><span data-stu-id="fcf6e-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="fcf6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcf6e-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf6e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcf6e-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf6e-106">Adresy IP assoicated zaporę w wirtualnym koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="fcf6e-107">Mogą to być adresy publiczne i prywatne</span><span class="sxs-lookup"><span data-stu-id="fcf6e-107">These can be public and private addresses</span></span>

## <span data-ttu-id="fcf6e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcf6e-108">EXAMPLES</span></span>

### <span data-ttu-id="fcf6e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fcf6e-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="fcf6e-110">W tym przykładzie jest tworzony obiekt centralny adres IP z liczbą 2 publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="fcf6e-111">Obiekt HubIPAddress jest ssociated z zaporą w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="fcf6e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcf6e-112">PARAMETERS</span></span>

### <span data-ttu-id="fcf6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf6e-113">-DefaultProfile</span></span>
<span data-ttu-id="fcf6e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf6e-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="fcf6e-115">-PrivateIPAddress</span></span>
<span data-ttu-id="fcf6e-116">Prywatny adres IP zapory podłączonej do koncentratora</span><span class="sxs-lookup"><span data-stu-id="fcf6e-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="fcf6e-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="fcf6e-117">-PublicIPs</span></span>
<span data-ttu-id="fcf6e-118">Adresy IP zapory podłączonej do koncentratora</span><span class="sxs-lookup"><span data-stu-id="fcf6e-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="fcf6e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcf6e-119">-Confirm</span></span>
<span data-ttu-id="fcf6e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf6e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf6e-121">-WhatIf</span></span>
<span data-ttu-id="fcf6e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcf6e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf6e-124">CommonParameters</span></span>
<span data-ttu-id="fcf6e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf6e-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcf6e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf6e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcf6e-127">INPUTS</span></span>

### <span data-ttu-id="fcf6e-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fcf6e-128">None</span></span>

## <span data-ttu-id="fcf6e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcf6e-129">OUTPUTS</span></span>

### <span data-ttu-id="fcf6e-130">Microsoft. Azure. Commands. Network. models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="fcf6e-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="fcf6e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcf6e-131">NOTES</span></span>

## <span data-ttu-id="fcf6e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcf6e-132">RELATED LINKS</span></span>
