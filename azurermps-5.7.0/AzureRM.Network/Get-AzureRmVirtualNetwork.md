---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528058"
---
# <span data-ttu-id="99436-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99436-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="99436-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99436-102">SYNOPSIS</span></span>
<span data-ttu-id="99436-103">Pobiera sieć wirtualną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="99436-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99436-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99436-104">SYNTAX</span></span>

### <span data-ttu-id="99436-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="99436-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99436-106">Większa</span><span class="sxs-lookup"><span data-stu-id="99436-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99436-107">Opis</span><span class="sxs-lookup"><span data-stu-id="99436-107">DESCRIPTION</span></span>
<span data-ttu-id="99436-108">Polecenie cmdlet **Get-AzureRmVirtualNetwork umożliwia pobranie** jednej lub większej liczby sieci wirtualnych: n grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="99436-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="99436-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99436-109">EXAMPLES</span></span>

### <span data-ttu-id="99436-110">1: pobieranie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="99436-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="99436-111">To polecenie pobiera sieć wirtualną o nazwie MyVirtualNetwork w grupie zasób TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99436-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="99436-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99436-112">PARAMETERS</span></span>

### <span data-ttu-id="99436-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99436-113">-DefaultProfile</span></span>
<span data-ttu-id="99436-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99436-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99436-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="99436-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99436-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99436-116">-Name</span></span>
<span data-ttu-id="99436-117">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99436-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99436-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99436-118">-ResourceGroupName</span></span>
<span data-ttu-id="99436-119">Określa nazwę grupy zasobów, do której należy Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="99436-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99436-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99436-120">CommonParameters</span></span>
<span data-ttu-id="99436-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99436-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99436-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99436-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99436-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99436-123">INPUTS</span></span>

### <span data-ttu-id="99436-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="99436-124">None</span></span>
<span data-ttu-id="99436-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="99436-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99436-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99436-126">OUTPUTS</span></span>

### <span data-ttu-id="99436-127">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99436-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="99436-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99436-128">NOTES</span></span>

## <span data-ttu-id="99436-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99436-129">RELATED LINKS</span></span>

[<span data-ttu-id="99436-130">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99436-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="99436-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99436-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="99436-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99436-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


