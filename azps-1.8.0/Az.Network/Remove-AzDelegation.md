---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: de345650553771078c03d728551b4713b5696fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709151"
---
# <span data-ttu-id="b7026-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="b7026-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="b7026-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7026-102">SYNOPSIS</span></span>
<span data-ttu-id="b7026-103">Usuwa Delegowanie usługi z podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="b7026-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="b7026-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7026-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7026-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7026-105">DESCRIPTION</span></span>
<span data-ttu-id="b7026-106">Polecenie cmdlet **Remove-AzDelegation** pobiera w podsieci z delegacjami i usuwa nazwane delegowanie z tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="b7026-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="b7026-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7026-107">EXAMPLES</span></span>

### <span data-ttu-id="b7026-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7026-108">Example 1</span></span>
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

<span data-ttu-id="b7026-109">W tym przykładzie pierwsza połowa (znaleziona w obszarze _"Dodawanie delegacji do istniejącej podsieci"_ ) jest identyczna z poleceniem [Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="b7026-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="b7026-110">W drugiej połowie pierwsze dwa polecenia cmdlet pobierają podsieć zainteresowania, odświeżając kopię lokalną za pomocą tego, co znajduje się na serwerze.</span><span class="sxs-lookup"><span data-stu-id="b7026-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="b7026-111">Trzecie polecenie cmdlet usuwa delegowanie utworzone w pierwszej połowie z _podsieci_ i przechowuje zaktualizowaną podsieć w _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="b7026-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="b7026-112">Ostatnie polecenie cmdlet umożliwia zaktualizowanie serwera za pomocą usuniętego delegowania.</span><span class="sxs-lookup"><span data-stu-id="b7026-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="b7026-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7026-113">PARAMETERS</span></span>

### <span data-ttu-id="b7026-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7026-114">-DefaultProfile</span></span>
<span data-ttu-id="b7026-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7026-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7026-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7026-116">-Name</span></span>
<span data-ttu-id="b7026-117">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="b7026-117">The name of the delegation</span></span>

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

### <span data-ttu-id="b7026-118">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="b7026-118">-Subnet</span></span>
<span data-ttu-id="b7026-119">Podsieć, z której ma zostać usunięte delegowanie</span><span class="sxs-lookup"><span data-stu-id="b7026-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="b7026-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7026-120">CommonParameters</span></span>
<span data-ttu-id="b7026-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7026-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7026-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7026-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7026-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7026-123">INPUTS</span></span>

### <span data-ttu-id="b7026-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b7026-124">System.String</span></span>

### <span data-ttu-id="b7026-125">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b7026-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b7026-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7026-126">OUTPUTS</span></span>

### <span data-ttu-id="b7026-127">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b7026-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b7026-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7026-128">NOTES</span></span>

## <span data-ttu-id="b7026-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7026-129">RELATED LINKS</span></span>

<span data-ttu-id="b7026-130">[Dodaj-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Nowe — AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="b7026-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>