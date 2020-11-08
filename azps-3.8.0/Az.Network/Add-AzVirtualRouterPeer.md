---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: ce0d27bb091192db8f1cbc157daf1bb847f869d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051486"
---
# <span data-ttu-id="3b5fd-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3b5fd-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="3b5fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5fd-103">Dodawanie elementu równorzędnego do usługi Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3b5fd-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="3b5fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b5fd-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b5fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b5fd-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5fd-106">Polecenie cmdlet **Add-AzVirtualRouterPeer** dodaje VirtualRouter peer do usługi Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3b5fd-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>


## <span data-ttu-id="3b5fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b5fd-107">EXAMPLES</span></span>

### <span data-ttu-id="3b5fd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b5fd-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="3b5fd-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b5fd-109">PARAMETERS</span></span>

### <span data-ttu-id="3b5fd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b5fd-110">-AsJob</span></span>
<span data-ttu-id="3b5fd-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3b5fd-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5fd-112">-DefaultProfile</span></span>
<span data-ttu-id="3b5fd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3b5fd-114">-Force</span></span>
<span data-ttu-id="3b5fd-115">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="3b5fd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="3b5fd-116">-PeerAsn</span></span>
<span data-ttu-id="3b5fd-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-117">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="3b5fd-118">-PeerIp</span></span>
<span data-ttu-id="3b5fd-119">Adres IP elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-119">Peer Ip.</span></span>

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

### <span data-ttu-id="3b5fd-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3b5fd-120">-PeerName</span></span>
<span data-ttu-id="3b5fd-121">Nazwa węzła równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-121">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b5fd-123">Nazwa grupy zasobów wirtualnego routera/elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="3b5fd-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="3b5fd-124">-VirtualRouterName</span></span>
<span data-ttu-id="3b5fd-125">Router wirtualny, na którym znajduje się element równorzędny.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="3b5fd-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b5fd-126">-Confirm</span></span>
<span data-ttu-id="3b5fd-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5fd-128">-WhatIf</span></span>
<span data-ttu-id="3b5fd-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b5fd-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5fd-131">CommonParameters</span></span>
<span data-ttu-id="3b5fd-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b5fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5fd-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5fd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5fd-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b5fd-134">INPUTS</span></span>

### <span data-ttu-id="3b5fd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3b5fd-135">System.String</span></span>

### <span data-ttu-id="3b5fd-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="3b5fd-136">System.UInt32</span></span>

## <span data-ttu-id="3b5fd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b5fd-137">OUTPUTS</span></span>

### <span data-ttu-id="3b5fd-138">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3b5fd-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="3b5fd-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b5fd-139">NOTES</span></span>

## <span data-ttu-id="3b5fd-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b5fd-140">RELATED LINKS</span></span>
