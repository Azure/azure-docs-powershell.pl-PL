---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: d837355891f3b8095da0380fd91a9ac58a74acff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870047"
---
# <span data-ttu-id="73edd-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="73edd-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="73edd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73edd-102">SYNOPSIS</span></span>
<span data-ttu-id="73edd-103">Pobiera parametry IPsec sieci VPN ustawione w bramie sieci wirtualnej dla połączeń z witryną.</span><span class="sxs-lookup"><span data-stu-id="73edd-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="73edd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73edd-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73edd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="73edd-105">DESCRIPTION</span></span>
<span data-ttu-id="73edd-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="73edd-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="73edd-107">Polecenie cmdlet **Get-AzVpnClientIpsecParameter** zwraca obiekt parametrów protokołu IPSec VPN ustawiony w bramie na platformie Azure na podstawie nazwy bramy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73edd-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="73edd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73edd-108">EXAMPLES</span></span>

### <span data-ttu-id="73edd-109">1: Pobiera parametry IPSec VPN ustawione w bramie sieci wirtualnej dla połączenia z witryną.</span><span class="sxs-lookup"><span data-stu-id="73edd-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="73edd-110">Zwraca obiekt parametrów VPN IPSec ustawionych dla bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="73edd-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="73edd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73edd-111">PARAMETERS</span></span>

### <span data-ttu-id="73edd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73edd-112">-DefaultProfile</span></span>
<span data-ttu-id="73edd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73edd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73edd-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73edd-114">-Name</span></span>
<span data-ttu-id="73edd-115">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="73edd-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73edd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73edd-116">-ResourceGroupName</span></span>
<span data-ttu-id="73edd-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73edd-117">The resource group name.</span></span>

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

### <span data-ttu-id="73edd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73edd-118">CommonParameters</span></span>
<span data-ttu-id="73edd-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73edd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73edd-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73edd-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73edd-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73edd-121">INPUTS</span></span>

### <span data-ttu-id="73edd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="73edd-122">System.String</span></span>

## <span data-ttu-id="73edd-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73edd-123">OUTPUTS</span></span>

### <span data-ttu-id="73edd-124">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="73edd-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="73edd-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73edd-125">NOTES</span></span>

## <span data-ttu-id="73edd-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73edd-126">RELATED LINKS</span></span>

[<span data-ttu-id="73edd-127">Nowe — AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="73edd-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="73edd-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="73edd-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="73edd-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="73edd-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
