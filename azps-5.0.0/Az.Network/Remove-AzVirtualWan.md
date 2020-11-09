---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318577"
---
# <span data-ttu-id="28d3e-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28d3e-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="28d3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="28d3e-103">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28d3e-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="28d3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28d3e-104">SYNTAX</span></span>

### <span data-ttu-id="28d3e-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28d3e-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d3e-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="28d3e-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d3e-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="28d3e-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28d3e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="28d3e-108">DESCRIPTION</span></span>
<span data-ttu-id="28d3e-109">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28d3e-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="28d3e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28d3e-110">EXAMPLES</span></span>

### <span data-ttu-id="28d3e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28d3e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="28d3e-112">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="28d3e-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="28d3e-113">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="28d3e-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="28d3e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="28d3e-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="28d3e-115">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="28d3e-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="28d3e-116">To usuwanie jest wykonywane przy użyciu wirtualnego obiektu sieci WAN zwróconego przez nowe-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="28d3e-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="28d3e-117">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="28d3e-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="28d3e-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="28d3e-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="28d3e-119">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="28d3e-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="28d3e-120">To usuwanie jest wykonywane przy użyciu identyfikatora zasobu wirtualnego sieci WAN zwróconego przez nowe-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="28d3e-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="28d3e-121">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="28d3e-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="28d3e-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28d3e-122">PARAMETERS</span></span>

### <span data-ttu-id="28d3e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d3e-123">-DefaultProfile</span></span>
<span data-ttu-id="28d3e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28d3e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28d3e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="28d3e-125">-Force</span></span>
<span data-ttu-id="28d3e-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="28d3e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28d3e-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28d3e-127">-InputObject</span></span>
<span data-ttu-id="28d3e-128">Wirtualny obiekt sieci WAN, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="28d3e-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="28d3e-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28d3e-129">-Name</span></span>
<span data-ttu-id="28d3e-130">Nazwa wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="28d3e-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="28d3e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28d3e-131">-PassThru</span></span>
<span data-ttu-id="28d3e-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="28d3e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28d3e-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="28d3e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28d3e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d3e-134">-ResourceGroupName</span></span>
<span data-ttu-id="28d3e-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="28d3e-135">The resource group name.</span></span>

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

### <span data-ttu-id="28d3e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28d3e-136">-ResourceId</span></span>
<span data-ttu-id="28d3e-137">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="28d3e-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="28d3e-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28d3e-138">-Confirm</span></span>
<span data-ttu-id="28d3e-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28d3e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d3e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d3e-140">-WhatIf</span></span>
<span data-ttu-id="28d3e-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28d3e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d3e-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28d3e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d3e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d3e-143">CommonParameters</span></span>
<span data-ttu-id="28d3e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28d3e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d3e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d3e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d3e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28d3e-146">INPUTS</span></span>

### <span data-ttu-id="28d3e-147">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28d3e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="28d3e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="28d3e-148">System.String</span></span>

## <span data-ttu-id="28d3e-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28d3e-149">OUTPUTS</span></span>

### <span data-ttu-id="28d3e-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28d3e-150">System.Boolean</span></span>

## <span data-ttu-id="28d3e-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28d3e-151">NOTES</span></span>

## <span data-ttu-id="28d3e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28d3e-152">RELATED LINKS</span></span>

[<span data-ttu-id="28d3e-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28d3e-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="28d3e-154">Nowe — AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28d3e-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="28d3e-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28d3e-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
