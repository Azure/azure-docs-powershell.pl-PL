---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 32398b235ef28872730f5839cef52023fe0f4ee9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709326"
---
# <span data-ttu-id="9bfb2-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="9bfb2-101">New-AzDelegation</span></span>

## <span data-ttu-id="9bfb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bfb2-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfb2-103">Tworzy Delegowanie usługi.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-103">Creates a service delegation.</span></span>

## <span data-ttu-id="9bfb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bfb2-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bfb2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9bfb2-105">DESCRIPTION</span></span>
<span data-ttu-id="9bfb2-106">Polecenie cmdlet **New-AzDelegation** tworzy Delegowanie usługi, które można dodać do podsieci.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="9bfb2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bfb2-107">EXAMPLES</span></span>

### <span data-ttu-id="9bfb2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bfb2-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="9bfb2-109">Pierwsze polecenie cmdlet tworzy delegowanie, które można dodać do podsieci, i zapisuje je w zmiennej $delegation.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="9bfb2-110">Drugie i trzecie polecenia cmdlet pobierają podsieć do delegowania.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="9bfb2-111">Czwarty polecenie cmdlet umożliwia dodanie utworzonej delegacji do podsieci, a w ostatnim poleceniu cmdlet jest wysyłana zaktualizowana konfiguracja do serwera.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="9bfb2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bfb2-112">PARAMETERS</span></span>

### <span data-ttu-id="9bfb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfb2-113">-DefaultProfile</span></span>
<span data-ttu-id="9bfb2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bfb2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bfb2-115">-Name</span></span>
<span data-ttu-id="9bfb2-116">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="9bfb2-116">The name of the delegation</span></span>

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

### <span data-ttu-id="9bfb2-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9bfb2-117">-ServiceName</span></span>
<span data-ttu-id="9bfb2-118">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="9bfb2-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="9bfb2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfb2-119">CommonParameters</span></span>
<span data-ttu-id="9bfb2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bfb2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfb2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfb2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfb2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bfb2-122">INPUTS</span></span>

### <span data-ttu-id="9bfb2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9bfb2-123">System.String</span></span>

## <span data-ttu-id="9bfb2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bfb2-124">OUTPUTS</span></span>

### <span data-ttu-id="9bfb2-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="9bfb2-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="9bfb2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bfb2-126">NOTES</span></span>

## <span data-ttu-id="9bfb2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bfb2-127">RELATED LINKS</span></span>

<span data-ttu-id="9bfb2-128">[Dodaj-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="9bfb2-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>