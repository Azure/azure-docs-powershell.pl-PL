---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219764"
---
# <span data-ttu-id="f3348-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="f3348-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="f3348-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3348-102">SYNOPSIS</span></span>
<span data-ttu-id="f3348-103">Usuwa odbiornik grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f3348-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="f3348-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3348-104">SYNTAX</span></span>

### <span data-ttu-id="f3348-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f3348-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3348-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3348-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3348-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f3348-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3348-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="f3348-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3348-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f3348-109">DESCRIPTION</span></span>
<span data-ttu-id="f3348-110">Polecenie cmdlet Remove-AzAvailabilityGroupListener powoduje usunięcie odbiornika grupowego dostępności.</span><span class="sxs-lookup"><span data-stu-id="f3348-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="f3348-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3348-111">EXAMPLES</span></span>

### <span data-ttu-id="f3348-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3348-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="f3348-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="f3348-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="f3348-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="f3348-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="f3348-115">Usuwa AgListener01 odbiornika grup dostępności w AvailabilityGroup01 grupy dostępność.</span><span class="sxs-lookup"><span data-stu-id="f3348-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="f3348-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3348-116">PARAMETERS</span></span>

### <span data-ttu-id="f3348-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3348-117">-AsJob</span></span>
<span data-ttu-id="f3348-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="f3348-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f3348-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3348-119">-DefaultProfile</span></span>
<span data-ttu-id="f3348-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3348-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3348-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3348-121">-InputObject</span></span>
<span data-ttu-id="f3348-122">Obiekt odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f3348-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="f3348-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3348-123">-Name</span></span>
<span data-ttu-id="f3348-124">Nazwa odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="f3348-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="f3348-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3348-125">-PassThru</span></span>
<span data-ttu-id="f3348-126">Określa, czy usunięty zasób ma być wyprowadzany na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3348-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f3348-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3348-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3348-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3348-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3348-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3348-129">-ResourceId</span></span>
<span data-ttu-id="f3348-130">Identyfikator zasobu odbiornika grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="f3348-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="f3348-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="f3348-131">-SqlVMGroupName</span></span>
<span data-ttu-id="f3348-132">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="f3348-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="f3348-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="f3348-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="f3348-134">Obiekt grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="f3348-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="f3348-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3348-135">-Confirm</span></span>
<span data-ttu-id="f3348-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3348-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3348-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3348-137">-WhatIf</span></span>
<span data-ttu-id="f3348-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3348-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3348-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3348-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3348-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3348-140">CommonParameters</span></span>
<span data-ttu-id="f3348-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3348-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3348-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3348-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3348-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3348-143">INPUTS</span></span>

### <span data-ttu-id="f3348-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f3348-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="f3348-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f3348-145">System.String</span></span>

### <span data-ttu-id="f3348-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f3348-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f3348-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3348-147">OUTPUTS</span></span>

### <span data-ttu-id="f3348-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f3348-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="f3348-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3348-149">NOTES</span></span>

## <span data-ttu-id="f3348-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3348-150">RELATED LINKS</span></span>
