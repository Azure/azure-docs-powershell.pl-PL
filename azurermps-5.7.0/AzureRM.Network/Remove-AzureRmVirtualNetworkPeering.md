---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a128f7c9e9440255ed01b32c4460ffd180655928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553655"
---
# <span data-ttu-id="c045d-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c045d-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="c045d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c045d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c045d-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c045d-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c045d-104">Opis</span><span class="sxs-lookup"><span data-stu-id="c045d-104">DESCRIPTION</span></span>

## <span data-ttu-id="c045d-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c045d-105">EXAMPLES</span></span>

### <span data-ttu-id="c045d-106">Przykład 1: usuwanie komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c045d-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="c045d-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c045d-107">PARAMETERS</span></span>

### <span data-ttu-id="c045d-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c045d-108">-AsJob</span></span>
<span data-ttu-id="c045d-109">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c045d-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c045d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c045d-110">-DefaultProfile</span></span>
<span data-ttu-id="c045d-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c045d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c045d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c045d-112">-Force</span></span>
<span data-ttu-id="c045d-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c045d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c045d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c045d-114">-Name</span></span>
<span data-ttu-id="c045d-115">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c045d-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="c045d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c045d-116">-PassThru</span></span>
<span data-ttu-id="c045d-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c045d-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c045d-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c045d-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c045d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c045d-119">-ResourceGroupName</span></span>
<span data-ttu-id="c045d-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c045d-120">The resource group name</span></span>

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

### <span data-ttu-id="c045d-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c045d-121">-VirtualNetworkName</span></span>
<span data-ttu-id="c045d-122">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c045d-122">The virtual network name.</span></span>

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

### <span data-ttu-id="c045d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c045d-123">-Confirm</span></span>
<span data-ttu-id="c045d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c045d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c045d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c045d-125">-WhatIf</span></span>
<span data-ttu-id="c045d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c045d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c045d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c045d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c045d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c045d-128">CommonParameters</span></span>
<span data-ttu-id="c045d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c045d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c045d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c045d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c045d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c045d-131">INPUTS</span></span>

### <span data-ttu-id="c045d-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c045d-132">None</span></span>
<span data-ttu-id="c045d-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c045d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c045d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c045d-134">OUTPUTS</span></span>

## <span data-ttu-id="c045d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c045d-135">NOTES</span></span>

## <span data-ttu-id="c045d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c045d-136">RELATED LINKS</span></span>

