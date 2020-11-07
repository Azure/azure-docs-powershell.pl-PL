---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719409"
---
# <span data-ttu-id="77f60-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="77f60-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="77f60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77f60-102">SYNOPSIS</span></span>
<span data-ttu-id="77f60-103">Pobiera usługę Azure VirtualHub, używając nazwy i ResourceGroupName albo listę wszystkich wirtualnych koncentratorów przez ResourceGroupName/abonament.</span><span class="sxs-lookup"><span data-stu-id="77f60-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77f60-104">SYNTAX</span></span>

### <span data-ttu-id="77f60-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77f60-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77f60-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f60-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77f60-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77f60-107">DESCRIPTION</span></span>
<span data-ttu-id="77f60-108">Pobiera usługę Azure VirtualHub, używając nazwy i ResourceGroupName albo listę wszystkich wirtualnych koncentratorów przez ResourceGroupName/abonament.</span><span class="sxs-lookup"><span data-stu-id="77f60-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="77f60-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77f60-109">EXAMPLES</span></span>

### <span data-ttu-id="77f60-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77f60-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="77f60-111">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="77f60-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="77f60-112">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="77f60-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="77f60-113">Następnie pobiera koncentrator wirtualny przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="77f60-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="77f60-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77f60-114">PARAMETERS</span></span>

### <span data-ttu-id="77f60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f60-115">-DefaultProfile</span></span>
<span data-ttu-id="77f60-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77f60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f60-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77f60-117">-Name</span></span>
<span data-ttu-id="77f60-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="77f60-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f60-119">-ResourceGroupName</span></span>
<span data-ttu-id="77f60-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77f60-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f60-121">CommonParameters</span></span>
<span data-ttu-id="77f60-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f60-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f60-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f60-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77f60-124">INPUTS</span></span>

### <span data-ttu-id="77f60-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77f60-125">None</span></span>

## <span data-ttu-id="77f60-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77f60-126">OUTPUTS</span></span>

### <span data-ttu-id="77f60-127">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="77f60-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="77f60-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77f60-128">NOTES</span></span>

## <span data-ttu-id="77f60-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77f60-129">RELATED LINKS</span></span>
