---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: b4daa24f787633d2f18896910faed340a969a0f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997711"
---
# <span data-ttu-id="6de1a-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="6de1a-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="6de1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de1a-102">SYNOPSIS</span></span>
<span data-ttu-id="6de1a-103">Pobiera bieżące użycie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6de1a-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="6de1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6de1a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de1a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6de1a-105">DESCRIPTION</span></span>
<span data-ttu-id="6de1a-106">Polecenie **cmdlet Get-AzVirtualNetworkUsageList** pobiera użycie podsieci dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6de1a-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="6de1a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6de1a-107">EXAMPLES</span></span>

### <span data-ttu-id="6de1a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6de1a-108">Example 1</span></span>
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

<span data-ttu-id="6de1a-109">Pobiera na podsieci bieżące wartości użycia dla sieci wirtualnej test użycia.</span><span class="sxs-lookup"><span data-stu-id="6de1a-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="6de1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6de1a-110">PARAMETERS</span></span>

### <span data-ttu-id="6de1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de1a-111">-DefaultProfile</span></span>
<span data-ttu-id="6de1a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6de1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de1a-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6de1a-113">-Name</span></span>
<span data-ttu-id="6de1a-114">Określa nazwę sieci wirtualnej, dla których mają być wyświetlane użycia.</span><span class="sxs-lookup"><span data-stu-id="6de1a-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="6de1a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de1a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6de1a-116">Określa nazwę grupy zasobów, do której należy sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="6de1a-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="6de1a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de1a-117">CommonParameters</span></span>
<span data-ttu-id="6de1a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de1a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de1a-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6de1a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de1a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6de1a-120">INPUTS</span></span>

### <span data-ttu-id="6de1a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6de1a-121">System.String</span></span>

## <span data-ttu-id="6de1a-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6de1a-122">OUTPUTS</span></span>

### <span data-ttu-id="6de1a-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="6de1a-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="6de1a-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6de1a-124">NOTES</span></span>

## <span data-ttu-id="6de1a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6de1a-125">RELATED LINKS</span></span>
