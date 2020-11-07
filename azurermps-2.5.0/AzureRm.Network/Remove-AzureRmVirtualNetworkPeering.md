---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: de39828183f06f8435078ceffc8c303c376e6186
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899223"
---
# <span data-ttu-id="d1268-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d1268-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="d1268-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1268-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1268-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1268-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1268-104">Opis</span><span class="sxs-lookup"><span data-stu-id="d1268-104">DESCRIPTION</span></span>

## <span data-ttu-id="d1268-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1268-105">EXAMPLES</span></span>

### <span data-ttu-id="d1268-106">Przykład 1: usuwanie komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d1268-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d1268-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1268-107">PARAMETERS</span></span>

### <span data-ttu-id="d1268-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1268-108">-AsJob</span></span>
<span data-ttu-id="d1268-109">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d1268-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1268-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1268-110">-DefaultProfile</span></span>
<span data-ttu-id="d1268-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1268-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1268-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d1268-112">-Force</span></span>
<span data-ttu-id="d1268-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d1268-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d1268-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1268-114">-Name</span></span>
<span data-ttu-id="d1268-115">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1268-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="d1268-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1268-116">-PassThru</span></span>
<span data-ttu-id="d1268-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d1268-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d1268-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d1268-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1268-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1268-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1268-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d1268-120">The resource group name</span></span>

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

### <span data-ttu-id="d1268-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d1268-121">-VirtualNetworkName</span></span>
<span data-ttu-id="d1268-122">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d1268-122">The virtual network name.</span></span>

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

### <span data-ttu-id="d1268-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1268-123">-Confirm</span></span>
<span data-ttu-id="d1268-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1268-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1268-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1268-125">-WhatIf</span></span>
<span data-ttu-id="d1268-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1268-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1268-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1268-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1268-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1268-128">CommonParameters</span></span>
<span data-ttu-id="d1268-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1268-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1268-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1268-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1268-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1268-131">INPUTS</span></span>

## <span data-ttu-id="d1268-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1268-132">OUTPUTS</span></span>

## <span data-ttu-id="d1268-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1268-133">NOTES</span></span>

## <span data-ttu-id="d1268-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1268-134">RELATED LINKS</span></span>

