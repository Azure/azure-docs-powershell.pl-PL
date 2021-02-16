---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199842"
---
# <span data-ttu-id="dd654-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="dd654-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="dd654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd654-102">SYNOPSIS</span></span>
<span data-ttu-id="dd654-103">Utwórz nową pulę węzła w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="dd654-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="dd654-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd654-104">SYNTAX</span></span>

### <span data-ttu-id="dd654-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd654-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd654-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd654-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd654-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd654-107">DESCRIPTION</span></span>
<span data-ttu-id="dd654-108">Utwórz nową pulę węzła w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="dd654-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="dd654-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd654-109">EXAMPLES</span></span>

### <span data-ttu-id="dd654-110">Tworzenie puli węzła z parametrami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="dd654-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="dd654-111">Tworzenie kontenera systemu Windows Server na serwerze AKS</span><span class="sxs-lookup"><span data-stu-id="dd654-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="dd654-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd654-112">PARAMETERS</span></span>

### <span data-ttu-id="dd654-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd654-113">-ClusterName</span></span>
<span data-ttu-id="dd654-114">Nazwa zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="dd654-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-115">- ClusterObject</span><span class="sxs-lookup"><span data-stu-id="dd654-115">-ClusterObject</span></span>
<span data-ttu-id="dd654-116">Określ obiekt klastrów, w którym ma być tworzyć pulę węzła.</span><span class="sxs-lookup"><span data-stu-id="dd654-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-117">— Liczba</span><span class="sxs-lookup"><span data-stu-id="dd654-117">-Count</span></span>
<span data-ttu-id="dd654-118">Domyślna liczba węzłów dla pul węzłów.</span><span class="sxs-lookup"><span data-stu-id="dd654-118">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd654-119">-DefaultProfile</span></span>
<span data-ttu-id="dd654-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd654-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd654-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="dd654-121">-EnableAutoScaling</span></span>
<span data-ttu-id="dd654-122">Czy włączyć automatyczny skaler</span><span class="sxs-lookup"><span data-stu-id="dd654-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="dd654-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="dd654-123">-Force</span></span>
<span data-ttu-id="dd654-124">Tworzenie puli węzła, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="dd654-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="dd654-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="dd654-125">-KubernetesVersion</span></span>
<span data-ttu-id="dd654-126">Wersja programu Kubernetes do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="dd654-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="dd654-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="dd654-127">-MaxCount</span></span>
<span data-ttu-id="dd654-128">Maksymalna liczba węzłów na skalowanie automatyczne</span><span class="sxs-lookup"><span data-stu-id="dd654-128">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="dd654-129">-MaxPodCount</span></span>
<span data-ttu-id="dd654-130">Maksymalna liczba zasobników, które mogą być uruchamiane w węźle.</span><span class="sxs-lookup"><span data-stu-id="dd654-130">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="dd654-131">-MinCount</span></span>
<span data-ttu-id="dd654-132">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="dd654-132">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd654-133">-Name</span></span>
<span data-ttu-id="dd654-134">Nazwa puli węzła.</span><span class="sxs-lookup"><span data-stu-id="dd654-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="dd654-135">-OsSizeSize</span><span class="sxs-lookup"><span data-stu-id="dd654-135">-OsDiskSize</span></span>
<span data-ttu-id="dd654-136">Domyślna liczba węzłów dla pul węzłów.</span><span class="sxs-lookup"><span data-stu-id="dd654-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-137">- OsType</span><span class="sxs-lookup"><span data-stu-id="dd654-137">-OsType</span></span>
<span data-ttu-id="dd654-138">Typ OsType używany do określania typu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="dd654-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="dd654-139">Do wyboru są systemy Linux i Windows.</span><span class="sxs-lookup"><span data-stu-id="dd654-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="dd654-140">Domyślnie linux.</span><span class="sxs-lookup"><span data-stu-id="dd654-140">Default to Linux.</span></span>

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

### <span data-ttu-id="dd654-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd654-141">-ResourceGroupName</span></span>
<span data-ttu-id="dd654-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd654-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd654-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd654-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="dd654-144">ScaleSetEvictionPolicy, która ma być używana do określania zasad wywrócenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="dd654-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="dd654-145">Domyślnie usuń.</span><span class="sxs-lookup"><span data-stu-id="dd654-145">Default to Delete.</span></span>

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

### <span data-ttu-id="dd654-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="dd654-146">-ScaleSetPriority</span></span>
<span data-ttu-id="dd654-147">ScaleSetPriority, która ma być używana do określania priorytetu zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dd654-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="dd654-148">Domyślnie jest to zwykły.</span><span class="sxs-lookup"><span data-stu-id="dd654-148">Default to regular.</span></span>

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

### <span data-ttu-id="dd654-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="dd654-149">-VmSetType</span></span>
<span data-ttu-id="dd654-150">Reprezentuje typy puli węzła.</span><span class="sxs-lookup"><span data-stu-id="dd654-150">Represents types of an node pool.</span></span>
<span data-ttu-id="dd654-151">Możliwe wartości: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="dd654-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="dd654-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="dd654-152">-VmSize</span></span>
<span data-ttu-id="dd654-153">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dd654-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="dd654-154">Wartość domyślna to Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="dd654-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="dd654-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="dd654-155">-VnetSubnetID</span></span>
<span data-ttu-id="dd654-156">Identyfikator podsieci wirtualnej określa identyfikator podsieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dd654-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="dd654-157">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd654-157">-Confirm</span></span>
<span data-ttu-id="dd654-158">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd654-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd654-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd654-159">-WhatIf</span></span>
<span data-ttu-id="dd654-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd654-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd654-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd654-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd654-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd654-162">CommonParameters</span></span>
<span data-ttu-id="dd654-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd654-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd654-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd654-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd654-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd654-165">INPUTS</span></span>

### <span data-ttu-id="dd654-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="dd654-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="dd654-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd654-167">OUTPUTS</span></span>

### <span data-ttu-id="dd654-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="dd654-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="dd654-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd654-169">NOTES</span></span>

## <span data-ttu-id="dd654-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd654-170">RELATED LINKS</span></span>
