---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 744b5941335666078f33d04bd053faac51adb4bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050077"
---
# <span data-ttu-id="546ce-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="546ce-101">Add-AzDelegation</span></span>

## <span data-ttu-id="546ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="546ce-102">SYNOPSIS</span></span>
<span data-ttu-id="546ce-103">Dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="546ce-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="546ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="546ce-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="546ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="546ce-105">DESCRIPTION</span></span>
<span data-ttu-id="546ce-106">Polecenie cmdlet **Add-AzDelegation** umożliwia dodanie delegowania usługi do podsieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="546ce-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="546ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="546ce-107">EXAMPLES</span></span>

### <span data-ttu-id="546ce-108">1: Dodawanie delegacji</span><span class="sxs-lookup"><span data-stu-id="546ce-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="546ce-109">Pierwsze polecenie pobiera sieć wirtualną, w której znajduje się podsieć.</span><span class="sxs-lookup"><span data-stu-id="546ce-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="546ce-110">Drugie polecenie izoluje podsieć zainteresowania, którą chcesz delegować.</span><span class="sxs-lookup"><span data-stu-id="546ce-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="546ce-111">Trzecie polecenie dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="546ce-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="546ce-112">Ten przykład jest przydatny, gdy chcesz włączyć funkcję SQL w celu tworzenia punktów końcowych interfejsu w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="546ce-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="546ce-113">Polecenie ostatnie wysyła zaktualizowaną podsieć do serwera w celu zaktualizowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="546ce-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="546ce-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="546ce-114">PARAMETERS</span></span>

### <span data-ttu-id="546ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546ce-115">-DefaultProfile</span></span>
<span data-ttu-id="546ce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="546ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546ce-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="546ce-117">-Name</span></span>
<span data-ttu-id="546ce-118">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="546ce-118">The name of the delegation</span></span>

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

### <span data-ttu-id="546ce-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="546ce-119">-ServiceName</span></span>
<span data-ttu-id="546ce-120">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="546ce-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="546ce-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="546ce-121">-Subnet</span></span>
<span data-ttu-id="546ce-122">Podsieć</span><span class="sxs-lookup"><span data-stu-id="546ce-122">The subnet</span></span>

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

### <span data-ttu-id="546ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546ce-123">CommonParameters</span></span>
<span data-ttu-id="546ce-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546ce-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546ce-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546ce-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="546ce-126">INPUTS</span></span>

### <span data-ttu-id="546ce-127">System. String</span><span class="sxs-lookup"><span data-stu-id="546ce-127">System.String</span></span>

### <span data-ttu-id="546ce-128">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="546ce-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="546ce-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="546ce-129">OUTPUTS</span></span>

### <span data-ttu-id="546ce-130">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="546ce-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="546ce-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="546ce-131">NOTES</span></span>

## <span data-ttu-id="546ce-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="546ce-132">RELATED LINKS</span></span>

<span data-ttu-id="546ce-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="546ce-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>