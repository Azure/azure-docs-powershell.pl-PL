---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370657"
---
# <span data-ttu-id="e0ecb-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e0ecb-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="e0ecb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ecb-103">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e0ecb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0ecb-104">SYNTAX</span></span>

### <span data-ttu-id="e0ecb-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e0ecb-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ecb-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="e0ecb-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ecb-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ecb-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ecb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e0ecb-108">DESCRIPTION</span></span>
<span data-ttu-id="e0ecb-109">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e0ecb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0ecb-110">EXAMPLES</span></span>

### <span data-ttu-id="e0ecb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0ecb-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="e0ecb-112">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e0ecb-113">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="e0ecb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e0ecb-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="e0ecb-115">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e0ecb-116">To usuwanie jest wykonywane przy użyciu wirtualnego obiektu sieci WAN zwróconego przez nowe-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="e0ecb-117">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="e0ecb-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e0ecb-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="e0ecb-119">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e0ecb-120">To usuwanie jest wykonywane przy użyciu identyfikatora zasobu wirtualnego sieci WAN zwróconego przez nowe-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="e0ecb-121">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="e0ecb-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0ecb-122">PARAMETERS</span></span>

### <span data-ttu-id="e0ecb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ecb-123">-DefaultProfile</span></span>
<span data-ttu-id="e0ecb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ecb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e0ecb-125">-Force</span></span>
<span data-ttu-id="e0ecb-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e0ecb-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0ecb-127">-InputObject</span></span>
<span data-ttu-id="e0ecb-128">Wirtualny obiekt sieci WAN, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="e0ecb-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0ecb-129">-Name</span></span>
<span data-ttu-id="e0ecb-130">Nazwa wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="e0ecb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0ecb-131">-PassThru</span></span>
<span data-ttu-id="e0ecb-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0ecb-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0ecb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ecb-134">-ResourceGroupName</span></span>
<span data-ttu-id="e0ecb-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-135">The resource group name.</span></span>

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

### <span data-ttu-id="e0ecb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ecb-136">-ResourceId</span></span>
<span data-ttu-id="e0ecb-137">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="e0ecb-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0ecb-138">-Confirm</span></span>
<span data-ttu-id="e0ecb-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ecb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ecb-140">-WhatIf</span></span>
<span data-ttu-id="e0ecb-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ecb-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ecb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ecb-143">CommonParameters</span></span>
<span data-ttu-id="e0ecb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ecb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ecb-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ecb-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ecb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ecb-146">INPUTS</span></span>

### <span data-ttu-id="e0ecb-147">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e0ecb-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="e0ecb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e0ecb-148">System.String</span></span>

## <span data-ttu-id="e0ecb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0ecb-149">OUTPUTS</span></span>

### <span data-ttu-id="e0ecb-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0ecb-150">System.Boolean</span></span>

## <span data-ttu-id="e0ecb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0ecb-151">NOTES</span></span>

## <span data-ttu-id="e0ecb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0ecb-152">RELATED LINKS</span></span>

[<span data-ttu-id="e0ecb-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e0ecb-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="e0ecb-154">Nowe — AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e0ecb-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="e0ecb-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e0ecb-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
