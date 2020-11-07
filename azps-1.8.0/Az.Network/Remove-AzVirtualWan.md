---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: d1ec777d6574aa34a6b19fa7cdc94d9c349dbc48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709059"
---
# <span data-ttu-id="f05d9-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f05d9-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="f05d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f05d9-102">SYNOPSIS</span></span>
<span data-ttu-id="f05d9-103">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f05d9-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="f05d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f05d9-104">SYNTAX</span></span>

### <span data-ttu-id="f05d9-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f05d9-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05d9-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="f05d9-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05d9-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="f05d9-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f05d9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f05d9-108">DESCRIPTION</span></span>
<span data-ttu-id="f05d9-109">Usuwa wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f05d9-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="f05d9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f05d9-110">EXAMPLES</span></span>

### <span data-ttu-id="f05d9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f05d9-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="f05d9-112">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="f05d9-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="f05d9-113">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="f05d9-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="f05d9-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f05d9-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="f05d9-115">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="f05d9-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="f05d9-116">To usuwanie jest wykonywane przy użyciu wirtualnego obiektu sieci WAN zwróconego przez nowe-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f05d9-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="f05d9-117">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="f05d9-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="f05d9-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f05d9-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="f05d9-119">W tym przykładzie przedstawiono tworzenie wirtualnej sieci WAN w grupie zasobów, a następnie natychmiastowe usunięcie jej.</span><span class="sxs-lookup"><span data-stu-id="f05d9-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="f05d9-120">To usuwanie jest wykonywane przy użyciu identyfikatora zasobu wirtualnego sieci WAN zwróconego przez nowe-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f05d9-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="f05d9-121">Aby zapobiec wyświetlaniu monitu podczas usuwania wirtualnej sieci WAN, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="f05d9-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="f05d9-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f05d9-122">PARAMETERS</span></span>

### <span data-ttu-id="f05d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05d9-123">-DefaultProfile</span></span>
<span data-ttu-id="f05d9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f05d9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05d9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f05d9-125">-Force</span></span>
<span data-ttu-id="f05d9-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f05d9-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f05d9-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f05d9-127">-InputObject</span></span>
<span data-ttu-id="f05d9-128">Wirtualny obiekt sieci WAN, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f05d9-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="f05d9-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f05d9-129">-Name</span></span>
<span data-ttu-id="f05d9-130">Nazwa wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="f05d9-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="f05d9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f05d9-131">-PassThru</span></span>
<span data-ttu-id="f05d9-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f05d9-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f05d9-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f05d9-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f05d9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05d9-134">-ResourceGroupName</span></span>
<span data-ttu-id="f05d9-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f05d9-135">The resource group name.</span></span>

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

### <span data-ttu-id="f05d9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f05d9-136">-ResourceId</span></span>
<span data-ttu-id="f05d9-137">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f05d9-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="f05d9-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f05d9-138">-Confirm</span></span>
<span data-ttu-id="f05d9-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f05d9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f05d9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05d9-140">-WhatIf</span></span>
<span data-ttu-id="f05d9-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f05d9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f05d9-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f05d9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f05d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05d9-143">CommonParameters</span></span>
<span data-ttu-id="f05d9-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05d9-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05d9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05d9-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f05d9-146">INPUTS</span></span>

### <span data-ttu-id="f05d9-147">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f05d9-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="f05d9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f05d9-148">System.String</span></span>

## <span data-ttu-id="f05d9-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f05d9-149">OUTPUTS</span></span>

### <span data-ttu-id="f05d9-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f05d9-150">System.Boolean</span></span>

## <span data-ttu-id="f05d9-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f05d9-151">NOTES</span></span>

## <span data-ttu-id="f05d9-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f05d9-152">RELATED LINKS</span></span>

[<span data-ttu-id="f05d9-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f05d9-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="f05d9-154">Nowe — AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f05d9-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="f05d9-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f05d9-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)