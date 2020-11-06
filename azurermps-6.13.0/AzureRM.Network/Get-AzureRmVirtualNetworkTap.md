---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543747"
---
# <span data-ttu-id="095a7-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="095a7-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="095a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="095a7-102">SYNOPSIS</span></span>
<span data-ttu-id="095a7-103">Umożliwia wybranie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="095a7-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="095a7-104">SYNTAX</span></span>

### <span data-ttu-id="095a7-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="095a7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="095a7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="095a7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="095a7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="095a7-107">DESCRIPTION</span></span>
<span data-ttu-id="095a7-108">Polecenie cmdlet **Get-AzureRmVirtualNetworkTap umożliwia pobranie** wirtualnej sieci Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="095a7-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="095a7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="095a7-109">EXAMPLES</span></span>

### <span data-ttu-id="095a7-110">Przykład 1: Uzyskaj sieć wirtualną naciśnij</span><span class="sxs-lookup"><span data-stu-id="095a7-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="095a7-111">To polecenie pobiera VirtualNetwork, dla którego otrzymano odwołanie "VirtualTap1" w "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="095a7-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="095a7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="095a7-112">PARAMETERS</span></span>

### <span data-ttu-id="095a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095a7-113">-DefaultProfile</span></span>
<span data-ttu-id="095a7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="095a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095a7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="095a7-115">-Name</span></span>
<span data-ttu-id="095a7-116">Nazwa naciśnięcia przycisku.</span><span class="sxs-lookup"><span data-stu-id="095a7-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="095a7-118">Nazwa grupy zasobów naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="095a7-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095a7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="095a7-119">-ResourceId</span></span>
<span data-ttu-id="095a7-120">Identyfikator zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="095a7-120">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095a7-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="095a7-121">-Confirm</span></span>
<span data-ttu-id="095a7-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095a7-123">-WhatIf</span></span>
<span data-ttu-id="095a7-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="095a7-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="095a7-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095a7-126">CommonParameters</span></span>
<span data-ttu-id="095a7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095a7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095a7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="095a7-129">INPUTS</span></span>

### <span data-ttu-id="095a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="095a7-130">System.String</span></span>

## <span data-ttu-id="095a7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="095a7-131">OUTPUTS</span></span>

### <span data-ttu-id="095a7-132">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="095a7-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="095a7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="095a7-133">NOTES</span></span>

## <span data-ttu-id="095a7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="095a7-134">RELATED LINKS</span></span>
