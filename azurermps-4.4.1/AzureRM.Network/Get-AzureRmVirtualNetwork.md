---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546955"
---
# <span data-ttu-id="935b5-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="935b5-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="935b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="935b5-102">SYNOPSIS</span></span>
<span data-ttu-id="935b5-103">Pobiera sieć wirtualną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="935b5-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="935b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="935b5-104">SYNTAX</span></span>

### <span data-ttu-id="935b5-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="935b5-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="935b5-106">Większa</span><span class="sxs-lookup"><span data-stu-id="935b5-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935b5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="935b5-107">DESCRIPTION</span></span>
<span data-ttu-id="935b5-108">Polecenie cmdlet **Get-AzureRmVirtualNetwork umożliwia pobranie** jednej lub większej liczby sieci wirtualnych: n grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="935b5-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="935b5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="935b5-109">EXAMPLES</span></span>

### <span data-ttu-id="935b5-110">1: pobieranie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="935b5-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="935b5-111">To polecenie pobiera sieć wirtualną o nazwie MyVirtualNetwork w grupie zasób TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="935b5-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="935b5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="935b5-112">PARAMETERS</span></span>

### <span data-ttu-id="935b5-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="935b5-113">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b5-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="935b5-114">-Name</span></span>
<span data-ttu-id="935b5-115">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935b5-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="935b5-117">Określa nazwę grupy zasobów, do której należy Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="935b5-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935b5-118">-DefaultProfile</span></span>
<span data-ttu-id="935b5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="935b5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="935b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935b5-120">CommonParameters</span></span>
<span data-ttu-id="935b5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935b5-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935b5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935b5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="935b5-123">INPUTS</span></span>

## <span data-ttu-id="935b5-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="935b5-124">OUTPUTS</span></span>

### <span data-ttu-id="935b5-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="935b5-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="935b5-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="935b5-126">NOTES</span></span>

## <span data-ttu-id="935b5-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="935b5-127">RELATED LINKS</span></span>

[<span data-ttu-id="935b5-128">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="935b5-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="935b5-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="935b5-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="935b5-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="935b5-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


