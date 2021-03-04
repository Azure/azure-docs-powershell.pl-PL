---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006266"
---
# <span data-ttu-id="fcd8f-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fcd8f-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="fcd8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd8f-103">Pobiera parametry Ipsec sieci VPN ustawione w wirtualnej bramie sieciowej dla połączeń Typuj z witryną.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="fcd8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcd8f-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcd8f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcd8f-105">DESCRIPTION</span></span>
<span data-ttu-id="fcd8f-106">Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="fcd8f-107">Polecenie **cmdlet Get-AzVpnClientIpsecParameters** zwraca obiekt parametrów ipsec połączenia vpn ustawiony na bramie na platformie Azure na podstawie nazwy bramy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="fcd8f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcd8f-108">EXAMPLES</span></span>

### <span data-ttu-id="fcd8f-109">Przykład 1. Pobiera parametry ipsec sieci vpn ustawione w wirtualnej bramie sieciowej dla połączeń typu Punkt do witryny.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fcd8f-110">Zwraca obiekt parametrów ipsec sieci vpn ustawionych w wirtualnej bramie sieciowej o nazwie "myGateway" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="fcd8f-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="fcd8f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcd8f-111">PARAMETERS</span></span>

### <span data-ttu-id="fcd8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd8f-112">-DefaultProfile</span></span>
<span data-ttu-id="fcd8f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd8f-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fcd8f-114">-Name</span></span>
<span data-ttu-id="fcd8f-115">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-115">The resource name.</span></span>

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

### <span data-ttu-id="fcd8f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd8f-116">-ResourceGroupName</span></span>
<span data-ttu-id="fcd8f-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-117">The resource group name.</span></span>

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

### <span data-ttu-id="fcd8f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8f-118">CommonParameters</span></span>
<span data-ttu-id="fcd8f-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd8f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd8f-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcd8f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd8f-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcd8f-121">INPUTS</span></span>

### <span data-ttu-id="fcd8f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="fcd8f-122">System.String</span></span>

## <span data-ttu-id="fcd8f-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcd8f-123">OUTPUTS</span></span>

### <span data-ttu-id="fcd8f-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8f-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="fcd8f-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcd8f-125">NOTES</span></span>

## <span data-ttu-id="fcd8f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcd8f-126">RELATED LINKS</span></span>

[<span data-ttu-id="fcd8f-127">New-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8f-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fcd8f-128">Remove-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8f-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fcd8f-129">Set-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="fcd8f-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
