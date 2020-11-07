---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890674"
---
# <span data-ttu-id="6ebdb-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ebdb-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="6ebdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ebdb-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebdb-103">Pobiera sieć wirtualną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ebdb-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="6ebdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ebdb-104">SYNTAX</span></span>

### <span data-ttu-id="6ebdb-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="6ebdb-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ebdb-106">Większa</span><span class="sxs-lookup"><span data-stu-id="6ebdb-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ebdb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6ebdb-107">DESCRIPTION</span></span>
<span data-ttu-id="6ebdb-108">Polecenie cmdlet **Get-AzVirtualNetwork umożliwia pobranie** jednej lub większej liczby sieci wirtualnych: n grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ebdb-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="6ebdb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ebdb-109">EXAMPLES</span></span>

### <span data-ttu-id="6ebdb-110">1: pobieranie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6ebdb-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="6ebdb-111">To polecenie pobiera sieć wirtualną o nazwie MyVirtualNetwork w grupie zasób TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ebdb-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="6ebdb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ebdb-112">PARAMETERS</span></span>

### <span data-ttu-id="6ebdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebdb-113">-DefaultProfile</span></span>
<span data-ttu-id="6ebdb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ebdb-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6ebdb-115">-ExpandResource</span></span>
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

### <span data-ttu-id="6ebdb-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ebdb-116">-Name</span></span>
<span data-ttu-id="6ebdb-117">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ebdb-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6ebdb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebdb-118">-ResourceGroupName</span></span>
<span data-ttu-id="6ebdb-119">Określa nazwę grupy zasobów, do której należy Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="6ebdb-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="6ebdb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebdb-120">CommonParameters</span></span>
<span data-ttu-id="6ebdb-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ebdb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebdb-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebdb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebdb-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ebdb-123">INPUTS</span></span>

## <span data-ttu-id="6ebdb-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ebdb-124">OUTPUTS</span></span>

### <span data-ttu-id="6ebdb-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ebdb-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6ebdb-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ebdb-126">NOTES</span></span>

## <span data-ttu-id="6ebdb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ebdb-127">RELATED LINKS</span></span>

[<span data-ttu-id="6ebdb-128">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ebdb-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="6ebdb-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ebdb-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="6ebdb-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ebdb-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


