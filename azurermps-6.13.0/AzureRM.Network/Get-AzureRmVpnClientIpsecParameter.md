---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543736"
---
# <span data-ttu-id="95a5d-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="95a5d-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="95a5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="95a5d-103">Pobiera parametry IPsec sieci VPN ustawione w bramie sieci wirtualnej dla połączeń z witryną.</span><span class="sxs-lookup"><span data-stu-id="95a5d-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95a5d-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95a5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="95a5d-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="95a5d-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="95a5d-107">Polecenie cmdlet **Get-AzureRmVpnClientIpsecParameter** zwraca obiekt parametrów protokołu IPSec VPN ustawiony w bramie na platformie Azure na podstawie nazwy bramy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="95a5d-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="95a5d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95a5d-108">EXAMPLES</span></span>

### <span data-ttu-id="95a5d-109">1: Pobiera parametry IPSec VPN ustawione w bramie sieci wirtualnej dla połączenia z witryną.</span><span class="sxs-lookup"><span data-stu-id="95a5d-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="95a5d-110">Zwraca obiekt parametrów VPN IPSec ustawionych dla bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="95a5d-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="95a5d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95a5d-111">PARAMETERS</span></span>

### <span data-ttu-id="95a5d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a5d-112">-DefaultProfile</span></span>
<span data-ttu-id="95a5d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95a5d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95a5d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95a5d-114">-Name</span></span>
<span data-ttu-id="95a5d-115">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="95a5d-115">The resource name.</span></span>

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

### <span data-ttu-id="95a5d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a5d-116">-ResourceGroupName</span></span>
<span data-ttu-id="95a5d-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="95a5d-117">The resource group name.</span></span>

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

### <span data-ttu-id="95a5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a5d-118">CommonParameters</span></span>
<span data-ttu-id="95a5d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a5d-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a5d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a5d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95a5d-121">INPUTS</span></span>

### <span data-ttu-id="95a5d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="95a5d-122">System.String</span></span>

## <span data-ttu-id="95a5d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95a5d-123">OUTPUTS</span></span>

### <span data-ttu-id="95a5d-124">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="95a5d-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="95a5d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95a5d-125">NOTES</span></span>

## <span data-ttu-id="95a5d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95a5d-126">RELATED LINKS</span></span>
