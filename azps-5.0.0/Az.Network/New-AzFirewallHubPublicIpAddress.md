---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232792"
---
# <span data-ttu-id="ab6d5-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ab6d5-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="ab6d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6d5-103">Publiczny adres IP assoicated dla zapory na wirtualnym koncentratorze</span><span class="sxs-lookup"><span data-stu-id="ab6d5-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="ab6d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab6d5-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab6d5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab6d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ab6d5-106">Publiczny adres IP assoicated dla zapory na wirtualnym koncentratorze</span><span class="sxs-lookup"><span data-stu-id="ab6d5-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="ab6d5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab6d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ab6d5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab6d5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="ab6d5-109">Spowoduje to utworzenie 2 publicznych adresów IP na zaporze podłączonej do koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="ab6d5-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="ab6d5-110">Spowoduje to utworzenie adresu IP w wewnętrznej bazie danych. Nie możemy jawnie udostępnić adresu IP dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="ab6d5-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="ab6d5-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ab6d5-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="ab6d5-112">Spowoduje to utworzenie 1 nowego publicznego adresu IP na zaporze przez zatrzymanie $publicIp 1, $publicIp 2, które już istnieją w zaporze.</span><span class="sxs-lookup"><span data-stu-id="ab6d5-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="ab6d5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab6d5-113">PARAMETERS</span></span>

### <span data-ttu-id="ab6d5-114">— Adresy</span><span class="sxs-lookup"><span data-stu-id="ab6d5-114">-Addresses</span></span>
<span data-ttu-id="ab6d5-115">Publiczne adresy IP zapory podłączonej do koncentratora</span><span class="sxs-lookup"><span data-stu-id="ab6d5-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="ab6d5-116">-Count</span><span class="sxs-lookup"><span data-stu-id="ab6d5-116">-Count</span></span>
<span data-ttu-id="ab6d5-117">Liczba publicznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="ab6d5-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="ab6d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6d5-118">-DefaultProfile</span></span>
<span data-ttu-id="ab6d5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab6d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6d5-120">CommonParameters</span></span>
<span data-ttu-id="ab6d5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab6d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6d5-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab6d5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6d5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab6d5-123">INPUTS</span></span>

### <span data-ttu-id="ab6d5-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ab6d5-124">None</span></span>

## <span data-ttu-id="ab6d5-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab6d5-125">OUTPUTS</span></span>

### <span data-ttu-id="ab6d5-126">Microsoft. Azure. Commands. Network. models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="ab6d5-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="ab6d5-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab6d5-127">NOTES</span></span>

## <span data-ttu-id="ab6d5-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab6d5-128">RELATED LINKS</span></span>
