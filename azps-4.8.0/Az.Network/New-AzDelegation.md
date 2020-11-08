---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221974"
---
# <span data-ttu-id="bc3fd-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="bc3fd-101">New-AzDelegation</span></span>

## <span data-ttu-id="bc3fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3fd-103">Tworzy Delegowanie usługi.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-103">Creates a service delegation.</span></span>

## <span data-ttu-id="bc3fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc3fd-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc3fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="bc3fd-106">Polecenie cmdlet **New-AzDelegation** tworzy Delegowanie usługi, które można dodać do podsieci.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="bc3fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="bc3fd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc3fd-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="bc3fd-109">Pierwsze polecenie cmdlet tworzy delegowanie, które można dodać do podsieci, i zapisuje je w zmiennej $delegation.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="bc3fd-110">Drugie i trzecie polecenia cmdlet pobierają podsieć do delegowania.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="bc3fd-111">Czwarty polecenie cmdlet umożliwia dodanie utworzonej delegacji do podsieci, a w ostatnim poleceniu cmdlet jest wysyłana zaktualizowana konfiguracja do serwera.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="bc3fd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc3fd-112">PARAMETERS</span></span>

### <span data-ttu-id="bc3fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3fd-113">-DefaultProfile</span></span>
<span data-ttu-id="bc3fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc3fd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc3fd-115">-Name</span></span>
<span data-ttu-id="bc3fd-116">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="bc3fd-116">The name of the delegation</span></span>

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

### <span data-ttu-id="bc3fd-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-117">-ServiceName</span></span>
<span data-ttu-id="bc3fd-118">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="bc3fd-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="bc3fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3fd-119">CommonParameters</span></span>
<span data-ttu-id="bc3fd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3fd-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc3fd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3fd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc3fd-122">INPUTS</span></span>

### <span data-ttu-id="bc3fd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bc3fd-123">System.String</span></span>

## <span data-ttu-id="bc3fd-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc3fd-124">OUTPUTS</span></span>

### <span data-ttu-id="bc3fd-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="bc3fd-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="bc3fd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc3fd-126">NOTES</span></span>

## <span data-ttu-id="bc3fd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc3fd-127">RELATED LINKS</span></span>

<span data-ttu-id="bc3fd-128">[Dodaj-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="bc3fd-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>