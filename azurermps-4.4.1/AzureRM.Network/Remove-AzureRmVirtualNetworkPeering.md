---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719524"
---
# <span data-ttu-id="4217e-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4217e-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="4217e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4217e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4217e-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4217e-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4217e-104">Opis</span><span class="sxs-lookup"><span data-stu-id="4217e-104">DESCRIPTION</span></span>

## <span data-ttu-id="4217e-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4217e-105">EXAMPLES</span></span>

### <span data-ttu-id="4217e-106">Przykład 1: usuwanie komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4217e-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="4217e-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4217e-107">PARAMETERS</span></span>

### <span data-ttu-id="4217e-108">-Force</span><span class="sxs-lookup"><span data-stu-id="4217e-108">-Force</span></span>
<span data-ttu-id="4217e-109">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4217e-109">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4217e-110">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4217e-110">-Name</span></span>
<span data-ttu-id="4217e-111">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4217e-111">The virtual network peering name.</span></span>

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

### <span data-ttu-id="4217e-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4217e-112">-PassThru</span></span>
<span data-ttu-id="4217e-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="4217e-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4217e-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4217e-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4217e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4217e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4217e-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4217e-116">The resource group name</span></span>

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

### <span data-ttu-id="4217e-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4217e-117">-VirtualNetworkName</span></span>
<span data-ttu-id="4217e-118">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4217e-118">The virtual network name.</span></span>

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

### <span data-ttu-id="4217e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4217e-119">-Confirm</span></span>
<span data-ttu-id="4217e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4217e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4217e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4217e-121">-WhatIf</span></span>
<span data-ttu-id="4217e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4217e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4217e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4217e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4217e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4217e-124">-DefaultProfile</span></span>
<span data-ttu-id="4217e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4217e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4217e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4217e-126">CommonParameters</span></span>
<span data-ttu-id="4217e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4217e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4217e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4217e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4217e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4217e-129">INPUTS</span></span>

## <span data-ttu-id="4217e-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4217e-130">OUTPUTS</span></span>

## <span data-ttu-id="4217e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4217e-131">NOTES</span></span>

## <span data-ttu-id="4217e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4217e-132">RELATED LINKS</span></span>

