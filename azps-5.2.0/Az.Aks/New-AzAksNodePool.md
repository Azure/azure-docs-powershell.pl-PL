---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360857"
---
# <span data-ttu-id="336fc-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="336fc-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="336fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="336fc-102">SYNOPSIS</span></span>
<span data-ttu-id="336fc-103">Tworzenie nowej puli węzłów w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="336fc-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="336fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="336fc-104">SYNTAX</span></span>

### <span data-ttu-id="336fc-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="336fc-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="336fc-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="336fc-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="336fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="336fc-107">DESCRIPTION</span></span>
<span data-ttu-id="336fc-108">Tworzenie nowej puli węzłów w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="336fc-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="336fc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="336fc-109">EXAMPLES</span></span>

### <span data-ttu-id="336fc-110">Tworzenie puli węzłów z parametrami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="336fc-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="336fc-111">Tworzenie kontenera systemu Windows Server na AKS</span><span class="sxs-lookup"><span data-stu-id="336fc-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="336fc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="336fc-112">PARAMETERS</span></span>

### <span data-ttu-id="336fc-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="336fc-113">-ClusterName</span></span>
<span data-ttu-id="336fc-114">Nazwa zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="336fc-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="336fc-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="336fc-115">-ClusterObject</span></span>
<span data-ttu-id="336fc-116">Określ obiekt klastra, w którym ma zostać utworzona Pula węzłów.</span><span class="sxs-lookup"><span data-stu-id="336fc-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="336fc-117">-Count</span><span class="sxs-lookup"><span data-stu-id="336fc-117">-Count</span></span>
<span data-ttu-id="336fc-118">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="336fc-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="336fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336fc-119">-DefaultProfile</span></span>
<span data-ttu-id="336fc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="336fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="336fc-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="336fc-121">-EnableAutoScaling</span></span>
<span data-ttu-id="336fc-122">Czy włączyć funkcję automatycznej skalowania</span><span class="sxs-lookup"><span data-stu-id="336fc-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="336fc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="336fc-123">-Force</span></span>
<span data-ttu-id="336fc-124">Tworzenie puli węzłów nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="336fc-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="336fc-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="336fc-125">-KubernetesVersion</span></span>
<span data-ttu-id="336fc-126">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="336fc-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="336fc-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="336fc-127">-MaxCount</span></span>
<span data-ttu-id="336fc-128">Maksymalna liczba węzłów do automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="336fc-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="336fc-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="336fc-129">-MaxPodCount</span></span>
<span data-ttu-id="336fc-130">Maksymalna liczba identyfikatorów (), które mogą być uruchamiane w węźle.</span><span class="sxs-lookup"><span data-stu-id="336fc-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="336fc-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="336fc-131">-MinCount</span></span>
<span data-ttu-id="336fc-132">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="336fc-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="336fc-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="336fc-133">-Name</span></span>
<span data-ttu-id="336fc-134">Nazwa puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="336fc-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="336fc-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="336fc-135">-OsDiskSize</span></span>
<span data-ttu-id="336fc-136">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="336fc-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="336fc-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="336fc-137">-OsType</span></span>
<span data-ttu-id="336fc-138">OsType, który ma być wykorzystywany do określenia typu OS.</span><span class="sxs-lookup"><span data-stu-id="336fc-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="336fc-139">Wybierz pozycję z systemu Linux lub Windows.</span><span class="sxs-lookup"><span data-stu-id="336fc-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="336fc-140">Domyślnie jest to Linux.</span><span class="sxs-lookup"><span data-stu-id="336fc-140">Default to Linux.</span></span>

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

### <span data-ttu-id="336fc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336fc-141">-ResourceGroupName</span></span>
<span data-ttu-id="336fc-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="336fc-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="336fc-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="336fc-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="336fc-144">ScaleSetEvictionPolicy do użycia w celu określenia zasad wykluczenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="336fc-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="336fc-145">Domyślnie można usunąć.</span><span class="sxs-lookup"><span data-stu-id="336fc-145">Default to Delete.</span></span>

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

### <span data-ttu-id="336fc-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="336fc-146">-ScaleSetPriority</span></span>
<span data-ttu-id="336fc-147">ScaleSetPriority, aby określić priorytet zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="336fc-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="336fc-148">Domyślnie na regularny.</span><span class="sxs-lookup"><span data-stu-id="336fc-148">Default to regular.</span></span>

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

### <span data-ttu-id="336fc-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="336fc-149">-VmSetType</span></span>
<span data-ttu-id="336fc-150">Reprezentuje typy puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="336fc-150">Represents types of an node pool.</span></span>
<span data-ttu-id="336fc-151">Możliwe wartości obejmują: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="336fc-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="336fc-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="336fc-152">-VmSize</span></span>
<span data-ttu-id="336fc-153">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="336fc-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="336fc-154">Wartość domyślna to Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="336fc-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="336fc-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="336fc-155">-VnetSubnetID</span></span>
<span data-ttu-id="336fc-156">SubnetID VNet określa identyfikator podsieci VNet.</span><span class="sxs-lookup"><span data-stu-id="336fc-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="336fc-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="336fc-157">-Confirm</span></span>
<span data-ttu-id="336fc-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336fc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="336fc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336fc-159">-WhatIf</span></span>
<span data-ttu-id="336fc-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336fc-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="336fc-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="336fc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="336fc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336fc-162">CommonParameters</span></span>
<span data-ttu-id="336fc-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336fc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336fc-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="336fc-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336fc-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="336fc-165">INPUTS</span></span>

### <span data-ttu-id="336fc-166">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="336fc-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="336fc-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="336fc-167">OUTPUTS</span></span>

### <span data-ttu-id="336fc-168">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="336fc-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="336fc-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="336fc-169">NOTES</span></span>

## <span data-ttu-id="336fc-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="336fc-170">RELATED LINKS</span></span>
