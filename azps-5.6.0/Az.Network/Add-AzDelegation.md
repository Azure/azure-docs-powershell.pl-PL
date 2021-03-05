---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 779793bcc3df7ae62cc7ae7cc900ed863e8f4ee8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986770"
---
# <span data-ttu-id="5f2fd-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="5f2fd-101">Add-AzDelegation</span></span>

## <span data-ttu-id="5f2fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2fd-103">Dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="5f2fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f2fd-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f2fd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f2fd-105">DESCRIPTION</span></span>
<span data-ttu-id="5f2fd-106">Polecenie **cmdlet Add-AzDelegation** dodaje delegowanie usługi do podsieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="5f2fd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f2fd-107">EXAMPLES</span></span>

### <span data-ttu-id="5f2fd-108">Przykład 1. Dodawanie delegowania</span><span class="sxs-lookup"><span data-stu-id="5f2fd-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="5f2fd-109">Pierwsze polecenie pobiera sieć wirtualną, w której znajduje się podsieci.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="5f2fd-110">Drugie polecenie wyodrębnia zainteresowaną podsieci — to, którą chcesz delegować.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="5f2fd-111">Trzecie polecenie powoduje dodanie delegowania do podsieci.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="5f2fd-112">Ten konkretny przykład przydaje się, gdy chcesz włączyć język SQL do tworzenia punktów końcowych interfejsu w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="5f2fd-113">Ostatnie polecenie wysyła zaktualizowaną podsieci do serwera w celu jej zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="5f2fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f2fd-114">PARAMETERS</span></span>

### <span data-ttu-id="5f2fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2fd-115">-DefaultProfile</span></span>
<span data-ttu-id="5f2fd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f2fd-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5f2fd-117">-Name</span></span>
<span data-ttu-id="5f2fd-118">Nazwa delegowania</span><span class="sxs-lookup"><span data-stu-id="5f2fd-118">The name of the delegation</span></span>

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

### <span data-ttu-id="5f2fd-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5f2fd-119">-ServiceName</span></span>
<span data-ttu-id="5f2fd-120">Nazwa usługi, do której należy delegować podsieci</span><span class="sxs-lookup"><span data-stu-id="5f2fd-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="5f2fd-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="5f2fd-121">-Subnet</span></span>
<span data-ttu-id="5f2fd-122">Podsieci</span><span class="sxs-lookup"><span data-stu-id="5f2fd-122">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2fd-123">CommonParameters</span></span>
<span data-ttu-id="5f2fd-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2fd-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2fd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2fd-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f2fd-126">INPUTS</span></span>

### <span data-ttu-id="5f2fd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5f2fd-127">System.String</span></span>

### <span data-ttu-id="5f2fd-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5f2fd-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5f2fd-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f2fd-129">OUTPUTS</span></span>

### <span data-ttu-id="5f2fd-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5f2fd-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5f2fd-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f2fd-131">NOTES</span></span>

## <span data-ttu-id="5f2fd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f2fd-132">RELATED LINKS</span></span>

<span data-ttu-id="5f2fd-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5f2fd-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>