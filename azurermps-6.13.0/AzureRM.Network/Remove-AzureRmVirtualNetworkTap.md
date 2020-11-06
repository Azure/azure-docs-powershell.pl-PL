---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543608"
---
# <span data-ttu-id="0e7dc-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0e7dc-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="0e7dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7dc-103">Usuwa naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e7dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e7dc-104">SYNTAX</span></span>

### <span data-ttu-id="0e7dc-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e7dc-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e7dc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e7dc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e7dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0e7dc-108">DESCRIPTION</span></span>
<span data-ttu-id="0e7dc-109">Polecenie cmdlet **Remove-AzureRmVirtualNetworkTap** usuwa pozycję Sieć wirtualna Azure.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="0e7dc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e7dc-110">EXAMPLES</span></span>

### <span data-ttu-id="0e7dc-111">Przykład 1: usuwanie sieci virtuak naciśnięcie</span><span class="sxs-lookup"><span data-stu-id="0e7dc-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="0e7dc-112">To polecenie usuwa VirtualNetworkTap1 w grupie zasób ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="0e7dc-113">Ponieważ parametr *Force* nie jest wykorzystywany, użytkownik zostanie poproszony o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="0e7dc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e7dc-114">PARAMETERS</span></span>

### <span data-ttu-id="0e7dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e7dc-115">-AsJob</span></span>
<span data-ttu-id="0e7dc-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0e7dc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e7dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7dc-117">-DefaultProfile</span></span>
<span data-ttu-id="0e7dc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7dc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0e7dc-119">-Force</span></span>
<span data-ttu-id="0e7dc-120">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="0e7dc-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="0e7dc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e7dc-121">-InputObject</span></span>
<span data-ttu-id="0e7dc-122">Odwołanie do zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0e7dc-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e7dc-123">-Name</span></span>
<span data-ttu-id="0e7dc-124">Nazwa naciśnięcia przycisku.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e7dc-125">-PassThru</span></span>
<span data-ttu-id="0e7dc-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e7dc-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e7dc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e7dc-128">-ResourceGroupName</span></span>
<span data-ttu-id="0e7dc-129">Nazwa grupy zasobów naciśnięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7dc-130">-ResourceId</span></span>
<span data-ttu-id="0e7dc-131">Identyfikator zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0e7dc-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e7dc-132">-Confirm</span></span>
<span data-ttu-id="0e7dc-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e7dc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e7dc-134">-WhatIf</span></span>
<span data-ttu-id="0e7dc-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e7dc-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e7dc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7dc-137">CommonParameters</span></span>
<span data-ttu-id="0e7dc-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7dc-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e7dc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7dc-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e7dc-140">INPUTS</span></span>

### <span data-ttu-id="0e7dc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0e7dc-141">System.String</span></span>

## <span data-ttu-id="0e7dc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e7dc-142">OUTPUTS</span></span>

### <span data-ttu-id="0e7dc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e7dc-143">System.Boolean</span></span>

## <span data-ttu-id="0e7dc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e7dc-144">NOTES</span></span>

## <span data-ttu-id="0e7dc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e7dc-145">RELATED LINKS</span></span>
