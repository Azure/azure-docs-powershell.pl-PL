---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219661"
---
# <span data-ttu-id="b6259-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="b6259-101">New-AzAksCluster</span></span>

## <span data-ttu-id="b6259-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6259-102">SYNOPSIS</span></span>
<span data-ttu-id="b6259-103">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b6259-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="b6259-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6259-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6259-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6259-105">DESCRIPTION</span></span>

<span data-ttu-id="b6259-106">Utwórz nowy klaster usługi Azure Kubernetes Service (AKS).</span><span class="sxs-lookup"><span data-stu-id="b6259-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="b6259-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6259-107">EXAMPLES</span></span>

### <span data-ttu-id="b6259-108">Nowy AKS z wartością domyślną params.</span><span class="sxs-lookup"><span data-stu-id="b6259-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="b6259-109">Utwórz kontener systemu Windows Server na AKS.</span><span class="sxs-lookup"><span data-stu-id="b6259-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="b6259-110">Aby utworzyć kontener systemu Windows Server na AKS, musisz określić co najmniej cztery poniższe parametry podczas tworzenia AKS, a wartość `NetworkPlugin` i `NodeVmSetType` musi być `azure` `VirtualMachineScaleSets` odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="b6259-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="b6259-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6259-111">PARAMETERS</span></span>

### <span data-ttu-id="b6259-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="b6259-112">-AcrNameToAttach</span></span>
<span data-ttu-id="b6259-113">Przydziel rolę "acrpull" określonej ACR usłudze AKS Service Principal, na przykład myacr</span><span class="sxs-lookup"><span data-stu-id="b6259-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="b6259-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="b6259-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="b6259-115">Nazwy dodatków, które mają być włączone po utworzeniu klastra.</span><span class="sxs-lookup"><span data-stu-id="b6259-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="b6259-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6259-116">-AsJob</span></span>
<span data-ttu-id="b6259-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b6259-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6259-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6259-118">-DefaultProfile</span></span>
<span data-ttu-id="b6259-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6259-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6259-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="b6259-120">-DnsNamePrefix</span></span>
<span data-ttu-id="b6259-121">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="b6259-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="b6259-122">Długość musi być <= 9, jeśli użytkownicy planują dodać kontener systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b6259-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="b6259-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="b6259-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="b6259-124">Czy włączyć funkcję automatycznej skalowania</span><span class="sxs-lookup"><span data-stu-id="b6259-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="b6259-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="b6259-125">-EnableRbac</span></span>
<span data-ttu-id="b6259-126">Czy włączyć Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="b6259-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="b6259-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b6259-127">-Force</span></span>
<span data-ttu-id="b6259-128">Utwórz klaster, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="b6259-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="b6259-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="b6259-129">-GenerateSshKey</span></span>
<span data-ttu-id="b6259-130">Generuj plik klucza SSH na {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="b6259-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="b6259-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="b6259-131">-KubernetesVersion</span></span>
<span data-ttu-id="b6259-132">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="b6259-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="b6259-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="b6259-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="b6259-134">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="b6259-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="b6259-135">-LoadBalancerSku</span></span>
<span data-ttu-id="b6259-136">Wersja SKU modułu równoważenia obciążenia dla zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="b6259-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="b6259-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6259-137">-Location</span></span>
<span data-ttu-id="b6259-138">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="b6259-138">Azure location for the cluster.</span></span>
<span data-ttu-id="b6259-139">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6259-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="b6259-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6259-140">-Name</span></span>
<span data-ttu-id="b6259-141">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="b6259-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="b6259-142">-NetworkPlugin</span></span>
<span data-ttu-id="b6259-143">Wtyczka sieciowa używana do tworzenia sieci Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b6259-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="b6259-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b6259-144">-NodeCount</span></span>
<span data-ttu-id="b6259-145">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="b6259-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="b6259-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="b6259-146">-NodeMaxCount</span></span>
<span data-ttu-id="b6259-147">Maksymalna liczba węzłów do automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="b6259-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="b6259-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="b6259-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="b6259-149">Maksymalna liczba identyfikatorów (), które mogą być uruchamiane w węźle.</span><span class="sxs-lookup"><span data-stu-id="b6259-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="b6259-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="b6259-150">-NodeMinCount</span></span>
<span data-ttu-id="b6259-151">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="b6259-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="b6259-152">-Nodename</span><span class="sxs-lookup"><span data-stu-id="b6259-152">-NodeName</span></span>
<span data-ttu-id="b6259-153">Unikatowa nazwa profilu puli agentów w kontekście subskrypcji i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6259-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="b6259-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="b6259-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="b6259-155">Rozmiar dysku systemu operacyjnego w GB dla każdego węzła w puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="b6259-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="b6259-156">Minimum 30 GB.</span><span class="sxs-lookup"><span data-stu-id="b6259-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="b6259-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="b6259-157">-NodeOsType</span></span>
<span data-ttu-id="b6259-158">OsType, który ma być wykorzystywany do określenia typu OS.</span><span class="sxs-lookup"><span data-stu-id="b6259-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="b6259-159">Wybierz pozycję z systemu Linux lub Windows.</span><span class="sxs-lookup"><span data-stu-id="b6259-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="b6259-160">Domyślnie jest to Linux.</span><span class="sxs-lookup"><span data-stu-id="b6259-160">Default to Linux.</span></span>

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

### <span data-ttu-id="b6259-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="b6259-161">-NodePoolMode</span></span>
<span data-ttu-id="b6259-162">NodePoolMode reprezentuje tryb puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="b6259-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="b6259-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6259-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="b6259-164">ScaleSetEvictionPolicy do użycia w celu określenia zasad wykluczenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b6259-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="b6259-165">Domyślnie można usunąć.</span><span class="sxs-lookup"><span data-stu-id="b6259-165">Default to Delete.</span></span>

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

### <span data-ttu-id="b6259-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="b6259-166">-NodeSetPriority</span></span>
<span data-ttu-id="b6259-167">ScaleSetPriority, aby określić priorytet zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6259-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="b6259-168">Domyślnie na regularny.</span><span class="sxs-lookup"><span data-stu-id="b6259-168">Default to regular.</span></span>

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

### <span data-ttu-id="b6259-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="b6259-169">-NodeVmSetType</span></span>
<span data-ttu-id="b6259-170">AgentPoolType reprezentuje typy puli agentów.</span><span class="sxs-lookup"><span data-stu-id="b6259-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="b6259-171">Możliwe wartości obejmują: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="b6259-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="b6259-172">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="b6259-172">-NodeVmSize</span></span>
<span data-ttu-id="b6259-173">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6259-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="b6259-174">Wartość domyślna to Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="b6259-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="b6259-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="b6259-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="b6259-176">SubnetID VNet określa identyfikator podsieci VNet.</span><span class="sxs-lookup"><span data-stu-id="b6259-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="b6259-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6259-177">-ResourceGroupName</span></span>
<span data-ttu-id="b6259-178">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6259-178">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-179">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="b6259-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="b6259-180">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="b6259-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="b6259-181">-SshKeyValue</span></span>
<span data-ttu-id="b6259-182">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="b6259-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="b6259-183">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="b6259-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-184">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="b6259-184">-SubnetName</span></span>
<span data-ttu-id="b6259-185">Nazwa podsieci dodatku VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="b6259-185">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6259-186">-Tag</span></span>
<span data-ttu-id="b6259-187">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="b6259-187">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="b6259-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="b6259-189">Nazwa użytkownika administratora na potrzeby maszyn wirtualnych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b6259-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="b6259-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="b6259-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="b6259-191">Hasło administratora, które ma być używane w przypadku maszyn wirtualnych systemu Windows, musi zawierać co najmniej jedno małe litery, tzn. jeden `[a-z]` `[A-Z]` znak specjalny `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="b6259-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b6259-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="b6259-193">Identyfikator zasobu obszaru roboczego dla dodatku monitorowania.</span><span class="sxs-lookup"><span data-stu-id="b6259-193">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6259-194">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6259-194">-Confirm</span></span>
<span data-ttu-id="b6259-195">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6259-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6259-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6259-196">-WhatIf</span></span>
<span data-ttu-id="b6259-197">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6259-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6259-198">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6259-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6259-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6259-199">CommonParameters</span></span>
<span data-ttu-id="b6259-200">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6259-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6259-201">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6259-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6259-202">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6259-202">INPUTS</span></span>

### <span data-ttu-id="b6259-203">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6259-203">None</span></span>

## <span data-ttu-id="b6259-204">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6259-204">OUTPUTS</span></span>

### <span data-ttu-id="b6259-205">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b6259-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b6259-206">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6259-206">NOTES</span></span>

## <span data-ttu-id="b6259-207">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6259-207">RELATED LINKS</span></span>
