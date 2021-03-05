---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: 43a92375126411d392623095a6753072757f49a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985811"
---
# <span data-ttu-id="504cb-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="504cb-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="504cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504cb-102">SYNOPSIS</span></span>
<span data-ttu-id="504cb-103">Publiczny adres IP assoicated do zapory w centrum wirtualnym</span><span class="sxs-lookup"><span data-stu-id="504cb-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="504cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="504cb-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="504cb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="504cb-105">DESCRIPTION</span></span>
<span data-ttu-id="504cb-106">Publiczny adres IP assoicated do zapory w centrum wirtualnym</span><span class="sxs-lookup"><span data-stu-id="504cb-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="504cb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="504cb-107">EXAMPLES</span></span>

### <span data-ttu-id="504cb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="504cb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="504cb-109">Spowoduje to utworzenie 2 publicznych adresów IP na zaporze dołączonej do centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="504cb-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="504cb-110">Spowoduje to utworzenie adresu IP w zaplecza. Nie możemy jawnie udostępnić tychdresses dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="504cb-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="504cb-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="504cb-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="504cb-112">Spowoduje to utworzenie 1 nowego publicznego adresu IP w zaporze przez zachowanie $publicIp 1, $publicIp 2 istniejących już w zaporze.</span><span class="sxs-lookup"><span data-stu-id="504cb-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="504cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="504cb-113">PARAMETERS</span></span>

### <span data-ttu-id="504cb-114">—Adresy</span><span class="sxs-lookup"><span data-stu-id="504cb-114">-Addresses</span></span>
<span data-ttu-id="504cb-115">Publiczne adresy IP zapory dołączonej do centrum</span><span class="sxs-lookup"><span data-stu-id="504cb-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504cb-116">— Liczba</span><span class="sxs-lookup"><span data-stu-id="504cb-116">-Count</span></span>
<span data-ttu-id="504cb-117">Liczba publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="504cb-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504cb-118">-DefaultProfile</span></span>
<span data-ttu-id="504cb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="504cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="504cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504cb-120">CommonParameters</span></span>
<span data-ttu-id="504cb-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="504cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504cb-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="504cb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504cb-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="504cb-123">INPUTS</span></span>

### <span data-ttu-id="504cb-124">Brak</span><span class="sxs-lookup"><span data-stu-id="504cb-124">None</span></span>

## <span data-ttu-id="504cb-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="504cb-125">OUTPUTS</span></span>

### <span data-ttu-id="504cb-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="504cb-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="504cb-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="504cb-127">NOTES</span></span>

## <span data-ttu-id="504cb-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="504cb-128">RELATED LINKS</span></span>
