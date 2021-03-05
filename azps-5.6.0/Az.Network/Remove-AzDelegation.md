---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 65149a0a52bc1bbb696b78033ec38670db97da48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993798"
---
# <span data-ttu-id="d4b06-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="d4b06-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="d4b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b06-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b06-103">Usuwa delegowanie usługi z podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="d4b06-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="d4b06-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4b06-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4b06-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4b06-105">DESCRIPTION</span></span>
<span data-ttu-id="d4b06-106">Polecenie **cmdlet Remove-AzDelegation** pobiera podsieci z delegowaniami i usuwa nazwane delegowanie z tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="d4b06-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="d4b06-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4b06-107">EXAMPLES</span></span>

### <span data-ttu-id="d4b06-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4b06-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="d4b06-109">W tym przykładzie pierwsza połowa (znaleziona w obszarze _"Dodawanie delegowania_ do istniejącej podsieci") jest identyczna jak w przypadku dodatku [AzDelegation.](./Add-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="d4b06-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="d4b06-110">W drugiej połowie pierwsze dwa polecenia cmdlet pobierają zainteresowaną podsieci, odświeżając kopię lokalną z tym, co jest na serwerze.</span><span class="sxs-lookup"><span data-stu-id="d4b06-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="d4b06-111">Trzecie polecenie cmdlet usuwa delegowanie utworzone w pierwszej połowie z _mojejubnetu_ i zapisuje zaktualizowaną podsieci w _$subnet._</span><span class="sxs-lookup"><span data-stu-id="d4b06-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="d4b06-112">Ostatnie polecenie cmdlet aktualizuje serwer przy użyciu usuniętej delegowania.</span><span class="sxs-lookup"><span data-stu-id="d4b06-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="d4b06-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4b06-113">PARAMETERS</span></span>

### <span data-ttu-id="d4b06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b06-114">-DefaultProfile</span></span>
<span data-ttu-id="d4b06-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4b06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4b06-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d4b06-116">-Name</span></span>
<span data-ttu-id="d4b06-117">Nazwa delegowania</span><span class="sxs-lookup"><span data-stu-id="d4b06-117">The name of the delegation</span></span>

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

### <span data-ttu-id="d4b06-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d4b06-118">-Subnet</span></span>
<span data-ttu-id="d4b06-119">Podsieci, z której należy usunąć delegowanie</span><span class="sxs-lookup"><span data-stu-id="d4b06-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="d4b06-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b06-120">CommonParameters</span></span>
<span data-ttu-id="d4b06-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b06-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b06-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b06-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b06-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4b06-123">INPUTS</span></span>

### <span data-ttu-id="d4b06-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d4b06-124">System.String</span></span>

### <span data-ttu-id="d4b06-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d4b06-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d4b06-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4b06-126">OUTPUTS</span></span>

### <span data-ttu-id="d4b06-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d4b06-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d4b06-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4b06-128">NOTES</span></span>

## <span data-ttu-id="d4b06-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4b06-129">RELATED LINKS</span></span>

<span data-ttu-id="d4b06-130">[Add-azDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="d4b06-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>