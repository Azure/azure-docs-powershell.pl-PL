---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549347"
---
# <span data-ttu-id="a2657-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a2657-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="a2657-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2657-102">SYNOPSIS</span></span>
<span data-ttu-id="a2657-103">Tworzy Delegowanie usługi.</span><span class="sxs-lookup"><span data-stu-id="a2657-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2657-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2657-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2657-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2657-105">DESCRIPTION</span></span>
<span data-ttu-id="a2657-106">Polecenie cmdlet **New-AzureRmDelegation** tworzy Delegowanie usługi, które można dodać do podsieci.</span><span class="sxs-lookup"><span data-stu-id="a2657-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="a2657-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2657-107">EXAMPLES</span></span>

### <span data-ttu-id="a2657-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2657-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="a2657-109">Pierwsze polecenie cmdlet tworzy delegowanie, które można dodać do podsieci, i zapisuje je w zmiennej $delegation.</span><span class="sxs-lookup"><span data-stu-id="a2657-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="a2657-110">Drugie i trzecie polecenia cmdlet pobierają podsieć do delegowania.</span><span class="sxs-lookup"><span data-stu-id="a2657-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="a2657-111">Czwarty polecenie cmdlet umożliwia dodanie utworzonej delegacji do podsieci, a w ostatnim poleceniu cmdlet jest wysyłana zaktualizowana konfiguracja do serwera.</span><span class="sxs-lookup"><span data-stu-id="a2657-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="a2657-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2657-112">PARAMETERS</span></span>

### <span data-ttu-id="a2657-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2657-113">-DefaultProfile</span></span>
<span data-ttu-id="a2657-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2657-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2657-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2657-115">-Name</span></span>
<span data-ttu-id="a2657-116">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="a2657-116">The name of the delegation</span></span>

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

### <span data-ttu-id="a2657-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a2657-117">-ServiceName</span></span>
<span data-ttu-id="a2657-118">Nazwa usługi, do której należy delegować podsieć</span><span class="sxs-lookup"><span data-stu-id="a2657-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="a2657-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2657-119">CommonParameters</span></span>
<span data-ttu-id="a2657-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2657-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a2657-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2657-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2657-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2657-122">INPUTS</span></span>

### <span data-ttu-id="a2657-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a2657-123">System.String</span></span>

## <span data-ttu-id="a2657-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2657-124">OUTPUTS</span></span>

### <span data-ttu-id="a2657-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a2657-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a2657-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2657-126">NOTES</span></span>

## <span data-ttu-id="a2657-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2657-127">RELATED LINKS</span></span>
<span data-ttu-id="a2657-128">[Dodaj-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="a2657-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
