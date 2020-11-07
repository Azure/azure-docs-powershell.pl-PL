---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718808"
---
# <span data-ttu-id="1d75e-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="1d75e-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="1d75e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d75e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d75e-103">Usuwa Delegowanie usługi z podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1d75e-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d75e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d75e-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d75e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d75e-105">DESCRIPTION</span></span>
<span data-ttu-id="1d75e-106">Polecenie cmdlet **Remove-AzureRmDelegation** pobiera w podsieci z delegacjami i usuwa nazwane delegowanie z tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1d75e-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="1d75e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d75e-107">EXAMPLES</span></span>

### <span data-ttu-id="1d75e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d75e-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="1d75e-109">W tym przykładzie pierwsza połowa (znaleziona w obszarze _"Dodawanie delegacji do istniejącej podsieci"_ ) jest identyczna z poleceniem [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="1d75e-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="1d75e-110">W drugiej połowie pierwsze dwa polecenia cmdlet pobierają podsieć zainteresowania, odświeżając kopię lokalną za pomocą tego, co znajduje się na serwerze.</span><span class="sxs-lookup"><span data-stu-id="1d75e-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="1d75e-111">Trzecie polecenie cmdlet usuwa delegowanie utworzone w pierwszej połowie z _podsieci_ i przechowuje zaktualizowaną podsieć w _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="1d75e-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="1d75e-112">Ostatnie polecenie cmdlet umożliwia zaktualizowanie serwera za pomocą usuniętego delegowania.</span><span class="sxs-lookup"><span data-stu-id="1d75e-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="1d75e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d75e-113">PARAMETERS</span></span>

### <span data-ttu-id="1d75e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d75e-114">-DefaultProfile</span></span>
<span data-ttu-id="1d75e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d75e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d75e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d75e-116">-Name</span></span>
<span data-ttu-id="1d75e-117">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="1d75e-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d75e-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1d75e-118">-ServiceName</span></span>
<span data-ttu-id="1d75e-119">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="1d75e-119">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d75e-120">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="1d75e-120">-Subnet</span></span>
<span data-ttu-id="1d75e-121">Podsieć, z której ma zostać usunięte delegowanie</span><span class="sxs-lookup"><span data-stu-id="1d75e-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="1d75e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d75e-122">CommonParameters</span></span>
<span data-ttu-id="1d75e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d75e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d75e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d75e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d75e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d75e-125">INPUTS</span></span>

### <span data-ttu-id="1d75e-126">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="1d75e-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="1d75e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1d75e-127">System.String</span></span>
## <span data-ttu-id="1d75e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d75e-128">OUTPUTS</span></span>

### <span data-ttu-id="1d75e-129">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="1d75e-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="1d75e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d75e-130">NOTES</span></span>

## <span data-ttu-id="1d75e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d75e-131">RELATED LINKS</span></span>

<span data-ttu-id="1d75e-132">[Dodaj-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Nowe — AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="1d75e-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
