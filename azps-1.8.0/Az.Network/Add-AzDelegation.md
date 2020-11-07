---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: e7646ff4a52131aaf1468cf32534235f71e7bf7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709690"
---
# <span data-ttu-id="ccbb4-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="ccbb4-101">Add-AzDelegation</span></span>

## <span data-ttu-id="ccbb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbb4-103">Dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="ccbb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccbb4-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccbb4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ccbb4-105">DESCRIPTION</span></span>
<span data-ttu-id="ccbb4-106">Polecenie cmdlet **Add-AzDelegation** umożliwia dodanie delegowania usługi do podsieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="ccbb4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccbb4-107">EXAMPLES</span></span>

### <span data-ttu-id="ccbb4-108">1: Dodawanie delegacji</span><span class="sxs-lookup"><span data-stu-id="ccbb4-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="ccbb4-109">Pierwsze polecenie pobiera sieć wirtualną, w której znajduje się podsieć.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="ccbb4-110">Drugie polecenie izoluje podsieć zainteresowania, którą chcesz delegować.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="ccbb4-111">Trzecie polecenie dodaje delegowanie do podsieci.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="ccbb4-112">Ten przykład jest przydatny, gdy chcesz włączyć funkcję SQL w celu tworzenia punktów końcowych interfejsu w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="ccbb4-113">Polecenie ostatnie wysyła zaktualizowaną podsieć do serwera w celu zaktualizowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="ccbb4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccbb4-114">PARAMETERS</span></span>

### <span data-ttu-id="ccbb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbb4-115">-DefaultProfile</span></span>
<span data-ttu-id="ccbb4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccbb4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccbb4-117">-Name</span></span>
<span data-ttu-id="ccbb4-118">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="ccbb4-118">The name of the delegation</span></span>

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

### <span data-ttu-id="ccbb4-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ccbb4-119">-ServiceName</span></span>
<span data-ttu-id="ccbb4-120">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="ccbb4-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="ccbb4-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="ccbb4-121">-Subnet</span></span>
<span data-ttu-id="ccbb4-122">Podsieć</span><span class="sxs-lookup"><span data-stu-id="ccbb4-122">The subnet</span></span>

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

### <span data-ttu-id="ccbb4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbb4-123">CommonParameters</span></span>
<span data-ttu-id="ccbb4-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbb4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbb4-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbb4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbb4-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccbb4-126">INPUTS</span></span>

### <span data-ttu-id="ccbb4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ccbb4-127">System.String</span></span>

### <span data-ttu-id="ccbb4-128">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ccbb4-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ccbb4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccbb4-129">OUTPUTS</span></span>

### <span data-ttu-id="ccbb4-130">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ccbb4-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ccbb4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccbb4-131">NOTES</span></span>

## <span data-ttu-id="ccbb4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccbb4-132">RELATED LINKS</span></span>

<span data-ttu-id="ccbb4-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="ccbb4-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>