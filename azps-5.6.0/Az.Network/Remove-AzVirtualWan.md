---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: ae05b4afd18bb1cdb55c8c1b748068f1f6c5191f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960282"
---
# <span data-ttu-id="2ee5b-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2ee5b-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="2ee5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee5b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee5b-103">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="2ee5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ee5b-104">SYNTAX</span></span>

### <span data-ttu-id="2ee5b-105">ByVirtualWanName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="2ee5b-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee5b-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="2ee5b-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee5b-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="2ee5b-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ee5b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ee5b-108">DESCRIPTION</span></span>
<span data-ttu-id="2ee5b-109">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="2ee5b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ee5b-110">EXAMPLES</span></span>

### <span data-ttu-id="2ee5b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ee5b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="2ee5b-112">W tym przykładzie wirtualna sieć WAN jest kreślana w grupie zasobów, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2ee5b-113">Aby pominąć monit podczas usuwania wirtualnej sieci WAN, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="2ee5b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2ee5b-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="2ee5b-115">W tym przykładzie wirtualna sieć WAN jest kreślana w grupie zasobów, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2ee5b-116">To usunięcie następuje przy użyciu obiektu wirtualnego wan zwróconego przez użytkownika New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="2ee5b-117">Aby pominąć monit podczas usuwania wirtualnej sieci WAN, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="2ee5b-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2ee5b-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="2ee5b-119">W tym przykładzie wirtualna sieć WAN jest kreślana w grupie zasobów, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2ee5b-120">To usunięcie następuje przy użyciu wirtualnego identyfikatora zasobu wan zwróconego przez użytkownika New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="2ee5b-121">Aby pominąć monit podczas usuwania wirtualnej sieci WAN, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="2ee5b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ee5b-122">PARAMETERS</span></span>

### <span data-ttu-id="2ee5b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee5b-123">-DefaultProfile</span></span>
<span data-ttu-id="2ee5b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee5b-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2ee5b-125">-Force</span></span>
<span data-ttu-id="2ee5b-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2ee5b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ee5b-127">-InputObject</span></span>
<span data-ttu-id="2ee5b-128">Obiekt wirtualny wan do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee5b-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ee5b-129">-Name</span></span>
<span data-ttu-id="2ee5b-130">Wirtualna nazwa sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee5b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ee5b-131">-PassThru</span></span>
<span data-ttu-id="2ee5b-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ee5b-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ee5b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee5b-134">-ResourceGroupName</span></span>
<span data-ttu-id="2ee5b-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee5b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ee5b-136">-ResourceId</span></span>
<span data-ttu-id="2ee5b-137">Identyfikator zasobu Azure dla wirtualnej sieci Wan do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee5b-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ee5b-138">-Confirm</span></span>
<span data-ttu-id="2ee5b-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee5b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee5b-140">-WhatIf</span></span>
<span data-ttu-id="2ee5b-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee5b-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee5b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee5b-143">CommonParameters</span></span>
<span data-ttu-id="2ee5b-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee5b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee5b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee5b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee5b-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ee5b-146">INPUTS</span></span>

### <span data-ttu-id="2ee5b-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2ee5b-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="2ee5b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="2ee5b-148">System.String</span></span>

## <span data-ttu-id="2ee5b-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ee5b-149">OUTPUTS</span></span>

### <span data-ttu-id="2ee5b-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ee5b-150">System.Boolean</span></span>

## <span data-ttu-id="2ee5b-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ee5b-151">NOTES</span></span>

## <span data-ttu-id="2ee5b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ee5b-152">RELATED LINKS</span></span>

[<span data-ttu-id="2ee5b-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2ee5b-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="2ee5b-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2ee5b-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="2ee5b-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2ee5b-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
