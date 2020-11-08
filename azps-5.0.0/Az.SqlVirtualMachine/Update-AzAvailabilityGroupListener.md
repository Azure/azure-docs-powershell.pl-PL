---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225485"
---
# <span data-ttu-id="716a2-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="716a2-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="716a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="716a2-102">SYNOPSIS</span></span>
<span data-ttu-id="716a2-103">Umożliwia zaktualizowanie odbiornika grup dostępności.</span><span class="sxs-lookup"><span data-stu-id="716a2-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="716a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="716a2-104">SYNTAX</span></span>

### <span data-ttu-id="716a2-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="716a2-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="716a2-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="716a2-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="716a2-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="716a2-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="716a2-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="716a2-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="716a2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="716a2-109">DESCRIPTION</span></span>
<span data-ttu-id="716a2-110">Polecenie cmdlet Update-AzAvailabilityGroupListener aktualizuje odbiornik grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="716a2-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="716a2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="716a2-111">EXAMPLES</span></span>

### <span data-ttu-id="716a2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="716a2-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="716a2-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="716a2-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="716a2-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="716a2-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="716a2-115">Aktualizuje listę wirtualnych maszyn wirtualnych SQL dla odbiornika grup dostępności.</span><span class="sxs-lookup"><span data-stu-id="716a2-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="716a2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="716a2-116">PARAMETERS</span></span>

### <span data-ttu-id="716a2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="716a2-117">-AsJob</span></span>
<span data-ttu-id="716a2-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="716a2-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="716a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716a2-119">-DefaultProfile</span></span>
<span data-ttu-id="716a2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="716a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="716a2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="716a2-121">-InputObject</span></span>
<span data-ttu-id="716a2-122">Obiekt odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="716a2-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="716a2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="716a2-123">-Name</span></span>
<span data-ttu-id="716a2-124">Nazwa odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="716a2-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="716a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="716a2-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="716a2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="716a2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="716a2-127">-ResourceId</span></span>
<span data-ttu-id="716a2-128">Identyfikator zasobu odbiornika grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="716a2-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="716a2-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="716a2-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="716a2-130">Lista identyfikatorów zasobów maszyny wirtualnej SQL</span><span class="sxs-lookup"><span data-stu-id="716a2-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="716a2-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="716a2-131">-SqlVMGroupName</span></span>
<span data-ttu-id="716a2-132">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="716a2-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="716a2-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="716a2-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="716a2-134">Obiekt grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="716a2-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="716a2-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="716a2-135">-Confirm</span></span>
<span data-ttu-id="716a2-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="716a2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716a2-137">-WhatIf</span></span>
<span data-ttu-id="716a2-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="716a2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="716a2-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="716a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716a2-140">CommonParameters</span></span>
<span data-ttu-id="716a2-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="716a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716a2-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="716a2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716a2-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="716a2-143">INPUTS</span></span>

### <span data-ttu-id="716a2-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="716a2-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="716a2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="716a2-145">System.String</span></span>

### <span data-ttu-id="716a2-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="716a2-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="716a2-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="716a2-147">OUTPUTS</span></span>

### <span data-ttu-id="716a2-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="716a2-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="716a2-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="716a2-149">NOTES</span></span>

## <span data-ttu-id="716a2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="716a2-150">RELATED LINKS</span></span>
