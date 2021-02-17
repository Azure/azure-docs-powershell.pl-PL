---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187930"
---
# <span data-ttu-id="5ef5e-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="5ef5e-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="5ef5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ef5e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef5e-103">Aktualizuje słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="5ef5e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ef5e-104">SYNTAX</span></span>

### <span data-ttu-id="5ef5e-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5ef5e-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ef5e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5ef5e-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ef5e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ef5e-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef5e-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="5ef5e-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef5e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ef5e-109">DESCRIPTION</span></span>
<span data-ttu-id="5ef5e-110">Polecenie Update-AzAvailabilityGroupListener aktualizuje słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="5ef5e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ef5e-111">EXAMPLES</span></span>

### <span data-ttu-id="5ef5e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ef5e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="5ef5e-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef5e-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="5ef5e-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="5ef5e-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="5ef5e-115">Aktualizuje listę maszyn wirtualnych SQL dla słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="5ef5e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ef5e-116">PARAMETERS</span></span>

### <span data-ttu-id="5ef5e-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef5e-117">-AsJob</span></span>
<span data-ttu-id="5ef5e-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="5ef5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef5e-119">-DefaultProfile</span></span>
<span data-ttu-id="5ef5e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ef5e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ef5e-121">-InputObject</span></span>
<span data-ttu-id="5ef5e-122">Obiekt Słuchacz grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5ef5e-123">-Name</span></span>
<span data-ttu-id="5ef5e-124">Nazwa słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef5e-125">-ResourceGroupName</span></span>
<span data-ttu-id="5ef5e-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ef5e-127">-ResourceId</span></span>
<span data-ttu-id="5ef5e-128">Identyfikator zasobu słuchacza grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="5ef5e-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5ef5e-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="5ef5e-130">Lista identyfikatorów zasobów maszyny wirtualnej języka Sql</span><span class="sxs-lookup"><span data-stu-id="5ef5e-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef5e-131">-SqlVMGroupName</span></span>
<span data-ttu-id="5ef5e-132">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="5ef5e-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="5ef5e-134">Obiekt Sql Virtual Machine Group.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef5e-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ef5e-135">-Confirm</span></span>
<span data-ttu-id="5ef5e-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef5e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef5e-137">-WhatIf</span></span>
<span data-ttu-id="5ef5e-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef5e-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef5e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef5e-140">CommonParameters</span></span>
<span data-ttu-id="5ef5e-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef5e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef5e-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ef5e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef5e-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ef5e-143">INPUTS</span></span>

### <span data-ttu-id="5ef5e-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="5ef5e-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="5ef5e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5ef5e-145">System.String</span></span>

### <span data-ttu-id="5ef5e-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="5ef5e-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="5ef5e-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ef5e-147">OUTPUTS</span></span>

### <span data-ttu-id="5ef5e-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="5ef5e-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="5ef5e-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ef5e-149">NOTES</span></span>

## <span data-ttu-id="5ef5e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ef5e-150">RELATED LINKS</span></span>
