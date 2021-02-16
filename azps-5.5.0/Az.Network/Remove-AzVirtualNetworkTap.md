---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179451"
---
# <span data-ttu-id="0b9a3-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b9a3-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="0b9a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9a3-103">Usuwa dotknięcie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="0b9a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b9a3-104">SYNTAX</span></span>

### <span data-ttu-id="0b9a3-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0b9a3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b9a3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b9a3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b9a3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b9a3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b9a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b9a3-108">DESCRIPTION</span></span>
<span data-ttu-id="0b9a3-109">Polecenie **cmdlet Remove-AzVirtualNetworkTap** usuwa naciśnięcie sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="0b9a3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b9a3-110">EXAMPLES</span></span>

### <span data-ttu-id="0b9a3-111">Przykład 1. Usuwanie naciśnięcia sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0b9a3-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="0b9a3-112">To polecenie usuwa przycisk VirtualNetworkTap1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="0b9a3-113">Ponieważ parametr *Force* nie jest używany, użytkownik zostanie wyświetlony monit o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="0b9a3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b9a3-114">PARAMETERS</span></span>

### <span data-ttu-id="0b9a3-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0b9a3-115">-AsJob</span></span>
<span data-ttu-id="0b9a3-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0b9a3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b9a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9a3-117">-DefaultProfile</span></span>
<span data-ttu-id="0b9a3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b9a3-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0b9a3-119">-Force</span></span>
<span data-ttu-id="0b9a3-120">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="0b9a3-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="0b9a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b9a3-121">-InputObject</span></span>
<span data-ttu-id="0b9a3-122">Odwołanie do zasobu VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b9a3-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="0b9a3-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b9a3-123">-Name</span></span>
<span data-ttu-id="0b9a3-124">Nazwa naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-124">The name of the tap.</span></span>

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

### <span data-ttu-id="0b9a3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b9a3-125">-PassThru</span></span>
<span data-ttu-id="0b9a3-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b9a3-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b9a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b9a3-129">Nazwa grupy zasobów sieci wirtualnej naciśnij.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="0b9a3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b9a3-130">-ResourceId</span></span>
<span data-ttu-id="0b9a3-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="0b9a3-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="0b9a3-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b9a3-132">-Confirm</span></span>
<span data-ttu-id="0b9a3-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b9a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b9a3-134">-WhatIf</span></span>
<span data-ttu-id="0b9a3-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b9a3-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b9a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9a3-137">CommonParameters</span></span>
<span data-ttu-id="0b9a3-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b9a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9a3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b9a3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9a3-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b9a3-140">INPUTS</span></span>

### <span data-ttu-id="0b9a3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0b9a3-141">System.String</span></span>

### <span data-ttu-id="0b9a3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b9a3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="0b9a3-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b9a3-143">OUTPUTS</span></span>

### <span data-ttu-id="0b9a3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b9a3-144">System.Boolean</span></span>

## <span data-ttu-id="0b9a3-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b9a3-145">NOTES</span></span>

## <span data-ttu-id="0b9a3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b9a3-146">RELATED LINKS</span></span>

[<span data-ttu-id="0b9a3-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b9a3-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="0b9a3-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b9a3-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="0b9a3-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b9a3-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
