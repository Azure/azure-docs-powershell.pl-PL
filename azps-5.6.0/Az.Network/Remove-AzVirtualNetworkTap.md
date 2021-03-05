---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: a0188236a5ce0b4da29a61b38d7c1889bc909968
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005962"
---
# <span data-ttu-id="8dbaf-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dbaf-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="8dbaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbaf-103">Usuwa dotknięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="8dbaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8dbaf-104">SYNTAX</span></span>

### <span data-ttu-id="8dbaf-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8dbaf-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbaf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbaf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbaf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbaf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dbaf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8dbaf-108">DESCRIPTION</span></span>
<span data-ttu-id="8dbaf-109">Polecenie **cmdlet Remove-AzVirtualNetworkTap** usuwa naciśnięcie sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="8dbaf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8dbaf-110">EXAMPLES</span></span>

### <span data-ttu-id="8dbaf-111">Przykład 1. Usuwanie naciśnięcia sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8dbaf-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="8dbaf-112">To polecenie usuwa przycisk VirtualNetworkTap1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="8dbaf-113">Ponieważ parametr *Force* nie jest używany, użytkownik zostanie wyświetlony monit o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="8dbaf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dbaf-114">PARAMETERS</span></span>

### <span data-ttu-id="8dbaf-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8dbaf-115">-AsJob</span></span>
<span data-ttu-id="8dbaf-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8dbaf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dbaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbaf-117">-DefaultProfile</span></span>
<span data-ttu-id="8dbaf-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dbaf-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8dbaf-119">-Force</span></span>
<span data-ttu-id="8dbaf-120">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="8dbaf-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8dbaf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dbaf-121">-InputObject</span></span>
<span data-ttu-id="8dbaf-122">Odwołanie do zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dbaf-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="8dbaf-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8dbaf-123">-Name</span></span>
<span data-ttu-id="8dbaf-124">Nazwa naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-124">The name of the tap.</span></span>

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

### <span data-ttu-id="8dbaf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dbaf-125">-PassThru</span></span>
<span data-ttu-id="8dbaf-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8dbaf-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8dbaf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbaf-128">-ResourceGroupName</span></span>
<span data-ttu-id="8dbaf-129">Nazwa grupy zasobów sieci wirtualnej naciśnij.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="8dbaf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dbaf-130">-ResourceId</span></span>
<span data-ttu-id="8dbaf-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="8dbaf-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="8dbaf-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8dbaf-132">-Confirm</span></span>
<span data-ttu-id="8dbaf-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dbaf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dbaf-134">-WhatIf</span></span>
<span data-ttu-id="8dbaf-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dbaf-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dbaf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbaf-137">CommonParameters</span></span>
<span data-ttu-id="8dbaf-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dbaf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbaf-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dbaf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbaf-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dbaf-140">INPUTS</span></span>

### <span data-ttu-id="8dbaf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8dbaf-141">System.String</span></span>

### <span data-ttu-id="8dbaf-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dbaf-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8dbaf-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dbaf-143">OUTPUTS</span></span>

### <span data-ttu-id="8dbaf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8dbaf-144">System.Boolean</span></span>

## <span data-ttu-id="8dbaf-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8dbaf-145">NOTES</span></span>

## <span data-ttu-id="8dbaf-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dbaf-146">RELATED LINKS</span></span>

[<span data-ttu-id="8dbaf-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dbaf-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="8dbaf-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dbaf-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="8dbaf-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dbaf-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
