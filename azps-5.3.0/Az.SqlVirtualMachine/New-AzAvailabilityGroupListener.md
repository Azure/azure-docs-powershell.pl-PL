---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501333"
---
# <span data-ttu-id="eba1e-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="eba1e-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="eba1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eba1e-102">SYNOPSIS</span></span>
<span data-ttu-id="eba1e-103">Tworzy nowy odbiornik grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="eba1e-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="eba1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eba1e-104">SYNTAX</span></span>

### <span data-ttu-id="eba1e-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="eba1e-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eba1e-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="eba1e-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba1e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eba1e-107">DESCRIPTION</span></span>
<span data-ttu-id="eba1e-108">Polecenie cmdlet New-AzAvailabilityGroupListener umożliwia utworzenie nowego odbiornika grupowego dostępności.</span><span class="sxs-lookup"><span data-stu-id="eba1e-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="eba1e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eba1e-109">EXAMPLES</span></span>

### <span data-ttu-id="eba1e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eba1e-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="eba1e-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="eba1e-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="eba1e-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="eba1e-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="eba1e-113">Tworzy nowy AgListener01 odbiornika grup dostępności dla AvailabilityGroup01 grupy dostępności w SqlVmGroup01 grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="eba1e-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="eba1e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eba1e-114">PARAMETERS</span></span>

### <span data-ttu-id="eba1e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba1e-115">-AsJob</span></span>
<span data-ttu-id="eba1e-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="eba1e-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="eba1e-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="eba1e-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="eba1e-118">Nazwa grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="eba1e-118">Availability Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba1e-119">-DefaultProfile</span></span>
<span data-ttu-id="eba1e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eba1e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba1e-121">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="eba1e-121">-IpAddress</span></span>
<span data-ttu-id="eba1e-122">Prywatny adres IP</span><span class="sxs-lookup"><span data-stu-id="eba1e-122">Private Ip Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="eba1e-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="eba1e-124">Identyfikator modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="eba1e-124">Load Balancer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eba1e-125">-Name</span></span>
<span data-ttu-id="eba1e-126">Nazwa odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="eba1e-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-127">-Port</span><span class="sxs-lookup"><span data-stu-id="eba1e-127">-Port</span></span>
<span data-ttu-id="eba1e-128">Numer portu dla odbiornika AG.</span><span class="sxs-lookup"><span data-stu-id="eba1e-128">Port number of AG Listener.</span></span> <span data-ttu-id="eba1e-129">Wartość domyślna to 1433.</span><span class="sxs-lookup"><span data-stu-id="eba1e-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="eba1e-130">-ProbePort</span></span>
<span data-ttu-id="eba1e-131">Port sondy</span><span class="sxs-lookup"><span data-stu-id="eba1e-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="eba1e-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="eba1e-133">Identyfikator zasobu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="eba1e-133">Public Ip Address Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba1e-134">-ResourceGroupName</span></span>
<span data-ttu-id="eba1e-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eba1e-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="eba1e-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="eba1e-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="eba1e-137">Lista identyfikatorów zasobów maszyny wirtualnej SQL</span><span class="sxs-lookup"><span data-stu-id="eba1e-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="eba1e-138">-SqlVMGroupName</span></span>
<span data-ttu-id="eba1e-139">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="eba1e-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="eba1e-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="eba1e-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="eba1e-141">Obiekt grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="eba1e-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="eba1e-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="eba1e-142">-SubnetId</span></span>
<span data-ttu-id="eba1e-143">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="eba1e-143">Subnet Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba1e-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eba1e-144">-Confirm</span></span>
<span data-ttu-id="eba1e-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba1e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba1e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba1e-146">-WhatIf</span></span>
<span data-ttu-id="eba1e-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba1e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba1e-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eba1e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba1e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba1e-149">CommonParameters</span></span>
<span data-ttu-id="eba1e-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba1e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba1e-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba1e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba1e-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eba1e-152">INPUTS</span></span>

### <span data-ttu-id="eba1e-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="eba1e-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="eba1e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eba1e-154">OUTPUTS</span></span>

### <span data-ttu-id="eba1e-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="eba1e-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="eba1e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eba1e-156">NOTES</span></span>

## <span data-ttu-id="eba1e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eba1e-157">RELATED LINKS</span></span>
