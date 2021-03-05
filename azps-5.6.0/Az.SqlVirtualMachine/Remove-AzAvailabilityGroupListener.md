---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: 56891d1dae20f89289b9c2f72bf87bfeed7bd347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978049"
---
# <span data-ttu-id="7c204-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="7c204-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="7c204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c204-102">SYNOPSIS</span></span>
<span data-ttu-id="7c204-103">Usuwa słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="7c204-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="7c204-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7c204-104">SYNTAX</span></span>

### <span data-ttu-id="7c204-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7c204-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c204-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7c204-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c204-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c204-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c204-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="7c204-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c204-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7c204-109">DESCRIPTION</span></span>
<span data-ttu-id="7c204-110">Polecenie Remove-AzAvailabilityGroupListener cmdlet usuwa słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="7c204-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="7c204-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7c204-111">EXAMPLES</span></span>

### <span data-ttu-id="7c204-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c204-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="7c204-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="7c204-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="7c204-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="7c204-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="7c204-115">Usuwa słuchacza grupy dostępności AgListener01 z grupy dostępności Grupy dostępności001.</span><span class="sxs-lookup"><span data-stu-id="7c204-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="7c204-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c204-116">PARAMETERS</span></span>

### <span data-ttu-id="7c204-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7c204-117">-AsJob</span></span>
<span data-ttu-id="7c204-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="7c204-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7c204-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c204-119">-DefaultProfile</span></span>
<span data-ttu-id="7c204-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c204-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c204-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c204-121">-InputObject</span></span>
<span data-ttu-id="7c204-122">Obiekt Słuchacz grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="7c204-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="7c204-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7c204-123">-Name</span></span>
<span data-ttu-id="7c204-124">Nazwa słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="7c204-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="7c204-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c204-125">-PassThru</span></span>
<span data-ttu-id="7c204-126">Określa, czy usunięty zasób ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c204-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="7c204-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c204-127">-ResourceGroupName</span></span>
<span data-ttu-id="7c204-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c204-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c204-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c204-129">-ResourceId</span></span>
<span data-ttu-id="7c204-130">Identyfikator zasobu słuchacza grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="7c204-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c204-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="7c204-131">-SqlVMGroupName</span></span>
<span data-ttu-id="7c204-132">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="7c204-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="7c204-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="7c204-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="7c204-134">Obiekt sql virtual machine Group.</span><span class="sxs-lookup"><span data-stu-id="7c204-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="7c204-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c204-135">-Confirm</span></span>
<span data-ttu-id="7c204-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c204-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c204-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c204-137">-WhatIf</span></span>
<span data-ttu-id="7c204-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c204-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c204-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7c204-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c204-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c204-140">CommonParameters</span></span>
<span data-ttu-id="7c204-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c204-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c204-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c204-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c204-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c204-143">INPUTS</span></span>

### <span data-ttu-id="7c204-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="7c204-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="7c204-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7c204-145">System.String</span></span>

### <span data-ttu-id="7c204-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="7c204-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="7c204-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c204-147">OUTPUTS</span></span>

### <span data-ttu-id="7c204-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="7c204-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="7c204-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7c204-149">NOTES</span></span>

## <span data-ttu-id="7c204-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c204-150">RELATED LINKS</span></span>
