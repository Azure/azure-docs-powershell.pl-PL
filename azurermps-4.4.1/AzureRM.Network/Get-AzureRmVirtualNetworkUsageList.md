---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 618fdf2ebe32f365bce72353f6e148fa3059cf66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554342"
---
# <span data-ttu-id="f15ee-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="f15ee-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="f15ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f15ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f15ee-103">Pobiera bieżące użycie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f15ee-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f15ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f15ee-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f15ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f15ee-105">DESCRIPTION</span></span>
<span data-ttu-id="f15ee-106">Polecenie cmdlet **Get-AzureRmVirtualNetworkUsageList** pobiera za użycie podsieci dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f15ee-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="f15ee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f15ee-107">EXAMPLES</span></span>

### <span data-ttu-id="f15ee-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f15ee-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="f15ee-109">Pobiera bieżące wartości użycia w podsieci dla sieci wirtualnej usagetest.</span><span class="sxs-lookup"><span data-stu-id="f15ee-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="f15ee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f15ee-110">PARAMETERS</span></span>

### <span data-ttu-id="f15ee-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f15ee-111">-Name</span></span>
<span data-ttu-id="f15ee-112">Określa nazwę sieci wirtualnej, do której mają być wyświetlane użycia.</span><span class="sxs-lookup"><span data-stu-id="f15ee-112">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="f15ee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15ee-113">-ResourceGroupName</span></span>
<span data-ttu-id="f15ee-114">Określa nazwę grupy zasobów, do której należy Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="f15ee-114">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="f15ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15ee-115">-DefaultProfile</span></span>
<span data-ttu-id="f15ee-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f15ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f15ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15ee-117">CommonParameters</span></span>
<span data-ttu-id="f15ee-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f15ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15ee-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15ee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15ee-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f15ee-120">INPUTS</span></span>

### <span data-ttu-id="f15ee-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f15ee-121">System.String</span></span>

## <span data-ttu-id="f15ee-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f15ee-122">OUTPUTS</span></span>

### <span data-ttu-id="f15ee-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="f15ee-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="f15ee-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f15ee-124">NOTES</span></span>

## <span data-ttu-id="f15ee-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f15ee-125">RELATED LINKS</span></span>

