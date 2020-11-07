---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 07c7d0e099cb5b83a0f98cfe8404be7e79b0427a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890630"
---
# <span data-ttu-id="39e40-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="39e40-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="39e40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39e40-102">SYNOPSIS</span></span>
<span data-ttu-id="39e40-103">Pobiera bieżące użycie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39e40-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="39e40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39e40-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39e40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39e40-105">DESCRIPTION</span></span>
<span data-ttu-id="39e40-106">Polecenie cmdlet **Get-AzVirtualNetworkUsageList** pobiera za użycie podsieci dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39e40-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="39e40-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39e40-107">EXAMPLES</span></span>

### <span data-ttu-id="39e40-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39e40-108">Example 1</span></span>
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

<span data-ttu-id="39e40-109">Pobiera bieżące wartości użycia w podsieci dla sieci wirtualnej usagetest.</span><span class="sxs-lookup"><span data-stu-id="39e40-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="39e40-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39e40-110">PARAMETERS</span></span>

### <span data-ttu-id="39e40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e40-111">-DefaultProfile</span></span>
<span data-ttu-id="39e40-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39e40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e40-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39e40-113">-Name</span></span>
<span data-ttu-id="39e40-114">Określa nazwę sieci wirtualnej, do której mają być wyświetlane użycia.</span><span class="sxs-lookup"><span data-stu-id="39e40-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="39e40-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e40-115">-ResourceGroupName</span></span>
<span data-ttu-id="39e40-116">Określa nazwę grupy zasobów, do której należy Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="39e40-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="39e40-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e40-117">CommonParameters</span></span>
<span data-ttu-id="39e40-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e40-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e40-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e40-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e40-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39e40-120">INPUTS</span></span>

### <span data-ttu-id="39e40-121">System. String</span><span class="sxs-lookup"><span data-stu-id="39e40-121">System.String</span></span>

## <span data-ttu-id="39e40-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39e40-122">OUTPUTS</span></span>

### <span data-ttu-id="39e40-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="39e40-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="39e40-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39e40-124">NOTES</span></span>

## <span data-ttu-id="39e40-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39e40-125">RELATED LINKS</span></span>

