---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379822"
---
# <span data-ttu-id="6309c-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="6309c-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="6309c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6309c-102">SYNOPSIS</span></span>
<span data-ttu-id="6309c-103">Pobiera bieżące użycie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6309c-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="6309c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6309c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6309c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6309c-105">DESCRIPTION</span></span>
<span data-ttu-id="6309c-106">Polecenie cmdlet **Get-AzVirtualNetworkUsageList** pobiera za użycie podsieci dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6309c-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="6309c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6309c-107">EXAMPLES</span></span>

### <span data-ttu-id="6309c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6309c-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="6309c-109">Pobiera bieżące wartości użycia w podsieci dla sieci wirtualnej usagetest.</span><span class="sxs-lookup"><span data-stu-id="6309c-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="6309c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6309c-110">PARAMETERS</span></span>

### <span data-ttu-id="6309c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6309c-111">-DefaultProfile</span></span>
<span data-ttu-id="6309c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6309c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6309c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6309c-113">-Name</span></span>
<span data-ttu-id="6309c-114">Określa nazwę sieci wirtualnej, do której mają być wyświetlane użycia.</span><span class="sxs-lookup"><span data-stu-id="6309c-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="6309c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6309c-115">-ResourceGroupName</span></span>
<span data-ttu-id="6309c-116">Określa nazwę grupy zasobów, do której należy Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="6309c-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="6309c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6309c-117">CommonParameters</span></span>
<span data-ttu-id="6309c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6309c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6309c-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6309c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6309c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6309c-120">INPUTS</span></span>

### <span data-ttu-id="6309c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6309c-121">System.String</span></span>

## <span data-ttu-id="6309c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6309c-122">OUTPUTS</span></span>

### <span data-ttu-id="6309c-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="6309c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="6309c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6309c-124">NOTES</span></span>

## <span data-ttu-id="6309c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6309c-125">RELATED LINKS</span></span>
