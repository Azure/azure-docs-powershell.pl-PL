---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063348"
---
# <span data-ttu-id="51460-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="51460-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="51460-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51460-102">SYNOPSIS</span></span>
<span data-ttu-id="51460-103">Usuwa Delegowanie usługi z podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="51460-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="51460-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51460-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51460-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51460-105">DESCRIPTION</span></span>
<span data-ttu-id="51460-106">Polecenie cmdlet **Remove-AzDelegation** pobiera w podsieci z delegacjami i usuwa nazwane delegowanie z tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="51460-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="51460-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51460-107">EXAMPLES</span></span>

### <span data-ttu-id="51460-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51460-108">Example 1</span></span>
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

<span data-ttu-id="51460-109">W tym przykładzie pierwsza połowa (znaleziona w obszarze _"Dodawanie delegacji do istniejącej podsieci"_ ) jest identyczna z poleceniem [Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="51460-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="51460-110">W drugiej połowie pierwsze dwa polecenia cmdlet pobierają podsieć zainteresowania, odświeżając kopię lokalną za pomocą tego, co znajduje się na serwerze.</span><span class="sxs-lookup"><span data-stu-id="51460-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="51460-111">Trzecie polecenie cmdlet usuwa delegowanie utworzone w pierwszej połowie z _podsieci_ i przechowuje zaktualizowaną podsieć w _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="51460-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="51460-112">Ostatnie polecenie cmdlet umożliwia zaktualizowanie serwera za pomocą usuniętego delegowania.</span><span class="sxs-lookup"><span data-stu-id="51460-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="51460-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51460-113">PARAMETERS</span></span>

### <span data-ttu-id="51460-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51460-114">-DefaultProfile</span></span>
<span data-ttu-id="51460-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51460-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51460-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51460-116">-Name</span></span>
<span data-ttu-id="51460-117">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="51460-117">The name of the delegation</span></span>

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

### <span data-ttu-id="51460-118">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="51460-118">-Subnet</span></span>
<span data-ttu-id="51460-119">Podsieć, z której ma zostać usunięte delegowanie</span><span class="sxs-lookup"><span data-stu-id="51460-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="51460-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51460-120">CommonParameters</span></span>
<span data-ttu-id="51460-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51460-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51460-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51460-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51460-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51460-123">INPUTS</span></span>

### <span data-ttu-id="51460-124">System. String</span><span class="sxs-lookup"><span data-stu-id="51460-124">System.String</span></span>

### <span data-ttu-id="51460-125">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="51460-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="51460-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51460-126">OUTPUTS</span></span>

### <span data-ttu-id="51460-127">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="51460-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="51460-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51460-128">NOTES</span></span>

## <span data-ttu-id="51460-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51460-129">RELATED LINKS</span></span>

<span data-ttu-id="51460-130">[Dodaj-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Nowe — AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="51460-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>