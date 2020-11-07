---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892894"
---
# <span data-ttu-id="94b4a-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="94b4a-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="94b4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94b4a-102">SYNOPSIS</span></span>

## <span data-ttu-id="94b4a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94b4a-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94b4a-104">Opis</span><span class="sxs-lookup"><span data-stu-id="94b4a-104">DESCRIPTION</span></span>

## <span data-ttu-id="94b4a-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94b4a-105">EXAMPLES</span></span>

### <span data-ttu-id="94b4a-106">Przykład 1: usuwanie komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94b4a-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="94b4a-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94b4a-107">PARAMETERS</span></span>

### <span data-ttu-id="94b4a-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94b4a-108">-AsJob</span></span>
<span data-ttu-id="94b4a-109">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="94b4a-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94b4a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b4a-110">-DefaultProfile</span></span>
<span data-ttu-id="94b4a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94b4a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94b4a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="94b4a-112">-Force</span></span>
<span data-ttu-id="94b4a-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94b4a-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94b4a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94b4a-114">-Name</span></span>
<span data-ttu-id="94b4a-115">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94b4a-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="94b4a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94b4a-116">-PassThru</span></span>
<span data-ttu-id="94b4a-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="94b4a-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94b4a-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="94b4a-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94b4a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b4a-119">-ResourceGroupName</span></span>
<span data-ttu-id="94b4a-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="94b4a-120">The resource group name</span></span>

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

### <span data-ttu-id="94b4a-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="94b4a-121">-VirtualNetworkName</span></span>
<span data-ttu-id="94b4a-122">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94b4a-122">The virtual network name.</span></span>

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

### <span data-ttu-id="94b4a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94b4a-123">-Confirm</span></span>
<span data-ttu-id="94b4a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b4a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b4a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b4a-125">-WhatIf</span></span>
<span data-ttu-id="94b4a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b4a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b4a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94b4a-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b4a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b4a-128">CommonParameters</span></span>
<span data-ttu-id="94b4a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b4a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b4a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b4a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b4a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94b4a-131">INPUTS</span></span>

## <span data-ttu-id="94b4a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94b4a-132">OUTPUTS</span></span>

## <span data-ttu-id="94b4a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94b4a-133">NOTES</span></span>

## <span data-ttu-id="94b4a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94b4a-134">RELATED LINKS</span></span>

