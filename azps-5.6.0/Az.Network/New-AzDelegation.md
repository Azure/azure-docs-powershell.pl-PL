---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: d383ddc5c7e0cf1b4ddb618fa11089883049d327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958561"
---
# <span data-ttu-id="7d651-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="7d651-101">New-AzDelegation</span></span>

## <span data-ttu-id="7d651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d651-102">SYNOPSIS</span></span>
<span data-ttu-id="7d651-103">Tworzy delegowanie usługi.</span><span class="sxs-lookup"><span data-stu-id="7d651-103">Creates a service delegation.</span></span>

## <span data-ttu-id="7d651-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d651-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d651-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d651-105">DESCRIPTION</span></span>
<span data-ttu-id="7d651-106">Polecenie **cmdlet New-AzDelegation** tworzy delegowanie usługi, które można dodać do podsieci.</span><span class="sxs-lookup"><span data-stu-id="7d651-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="7d651-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d651-107">EXAMPLES</span></span>

### <span data-ttu-id="7d651-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d651-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="7d651-109">Pierwsze polecenie cmdlet tworzy delegowanie, które można dodać do podsieci, i zapisuje je w $delegation danych.</span><span class="sxs-lookup"><span data-stu-id="7d651-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="7d651-110">Drugie i trzecie polecenia cmdlet pobierają podsieci do delegowania.</span><span class="sxs-lookup"><span data-stu-id="7d651-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="7d651-111">Czwarte polecenie cmdlet dodaje utworzone delegowanie do interesującej podsieci, a ostatnie polecenie cmdlet wysyła zaktualizowaną konfigurację do serwera.</span><span class="sxs-lookup"><span data-stu-id="7d651-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="7d651-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d651-112">PARAMETERS</span></span>

### <span data-ttu-id="7d651-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d651-113">-DefaultProfile</span></span>
<span data-ttu-id="7d651-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d651-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d651-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7d651-115">-Name</span></span>
<span data-ttu-id="7d651-116">Nazwa delegowania</span><span class="sxs-lookup"><span data-stu-id="7d651-116">The name of the delegation</span></span>

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

### <span data-ttu-id="7d651-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7d651-117">-ServiceName</span></span>
<span data-ttu-id="7d651-118">Nazwa usługi, do której należy delegować podsieci</span><span class="sxs-lookup"><span data-stu-id="7d651-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="7d651-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d651-119">CommonParameters</span></span>
<span data-ttu-id="7d651-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d651-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d651-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d651-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d651-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d651-122">INPUTS</span></span>

### <span data-ttu-id="7d651-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7d651-123">System.String</span></span>

## <span data-ttu-id="7d651-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d651-124">OUTPUTS</span></span>

### <span data-ttu-id="7d651-125">Microsoft.Azure.Commands.Network.Models.PSDelegacja</span><span class="sxs-lookup"><span data-stu-id="7d651-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="7d651-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d651-126">NOTES</span></span>

## <span data-ttu-id="7d651-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d651-127">RELATED LINKS</span></span>

<span data-ttu-id="7d651-128">[Add-azDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="7d651-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>