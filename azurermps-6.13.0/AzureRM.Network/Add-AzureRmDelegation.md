---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551191"
---
# <span data-ttu-id="5ec42-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="5ec42-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="5ec42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ec42-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec42-103">Dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ec42-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ec42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ec42-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ec42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ec42-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec42-106">Polecenie cmdlet **Add-AzureRmDelegation** umożliwia dodanie delegowania usługi do podsieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec42-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="5ec42-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ec42-107">EXAMPLES</span></span>

### <span data-ttu-id="5ec42-108">1: Dodawanie delegacji</span><span class="sxs-lookup"><span data-stu-id="5ec42-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="5ec42-109">Pierwsze polecenie pobiera sieć wirtualną, w której znajduje się podsieć.</span><span class="sxs-lookup"><span data-stu-id="5ec42-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="5ec42-110">Drugie polecenie izoluje podsieć zainteresowania, którą chcesz delegować.</span><span class="sxs-lookup"><span data-stu-id="5ec42-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="5ec42-111">Trzecie polecenie dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ec42-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="5ec42-112">Ten przykład jest przydatny, gdy chcesz włączyć funkcję SQL w celu tworzenia punktów końcowych interfejsu w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ec42-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="5ec42-113">Polecenie ostatnie wysyła zaktualizowaną podsieć do serwera w celu zaktualizowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ec42-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="5ec42-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ec42-114">PARAMETERS</span></span>

### <span data-ttu-id="5ec42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec42-115">-DefaultProfile</span></span>
<span data-ttu-id="5ec42-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec42-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ec42-117">-Name</span></span>
<span data-ttu-id="5ec42-118">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="5ec42-118">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec42-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5ec42-119">-ServiceName</span></span>
<span data-ttu-id="5ec42-120">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="5ec42-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ec42-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="5ec42-121">-Subnet</span></span>
<span data-ttu-id="5ec42-122">Podsieć</span><span class="sxs-lookup"><span data-stu-id="5ec42-122">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ec42-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec42-123">CommonParameters</span></span>
<span data-ttu-id="5ec42-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec42-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5ec42-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec42-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec42-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ec42-126">INPUTS</span></span>

### <span data-ttu-id="5ec42-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5ec42-127">System.String</span></span>

### <span data-ttu-id="5ec42-128">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5ec42-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5ec42-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ec42-129">OUTPUTS</span></span>

### <span data-ttu-id="5ec42-130">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5ec42-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5ec42-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ec42-131">NOTES</span></span>

## <span data-ttu-id="5ec42-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ec42-132">RELATED LINKS</span></span>
<span data-ttu-id="5ec42-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5ec42-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
