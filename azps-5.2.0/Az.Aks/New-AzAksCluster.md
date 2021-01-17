---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370797"
---
# <span data-ttu-id="22a49-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="22a49-101">New-AzAksCluster</span></span>

## <span data-ttu-id="22a49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22a49-102">SYNOPSIS</span></span>
<span data-ttu-id="22a49-103">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="22a49-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="22a49-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22a49-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="22a49-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22a49-105">DESCRIPTION</span></span>

<span data-ttu-id="22a49-106">Utwórz nowy klaster usługi Azure Kubernetes Service (AKS).</span><span class="sxs-lookup"><span data-stu-id="22a49-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="22a49-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22a49-107">EXAMPLES</span></span>

### <span data-ttu-id="22a49-108">Nowy AKS z wartością domyślną params.</span><span class="sxs-lookup"><span data-stu-id="22a49-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="22a49-109">Utwórz kontener systemu Windows Server na AKS.</span><span class="sxs-lookup"><span data-stu-id="22a49-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="22a49-110">Aby utworzyć kontener systemu Windows Server na AKS, musisz określić co najmniej cztery poniższe parametry podczas tworzenia AKS, a wartość `NetworkPlugin` i `NodeVmSetType` musi być `azure` `VirtualMachineScaleSets` odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="22a49-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="22a49-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22a49-111">PARAMETERS</span></span>

### <span data-ttu-id="22a49-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="22a49-112">-AcrNameToAttach</span></span>
<span data-ttu-id="22a49-113">Przydziel rolę "acrpull" określonej ACR usłudze AKS Service Principal, na przykład myacr</span><span class="sxs-lookup"><span data-stu-id="22a49-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="22a49-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="22a49-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="22a49-115">Nazwy dodatków, które mają być włączone po utworzeniu klastra.</span><span class="sxs-lookup"><span data-stu-id="22a49-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="22a49-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22a49-116">-AsJob</span></span>
<span data-ttu-id="22a49-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="22a49-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22a49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a49-118">-DefaultProfile</span></span>
<span data-ttu-id="22a49-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22a49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22a49-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="22a49-120">-DnsNamePrefix</span></span>
<span data-ttu-id="22a49-121">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="22a49-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="22a49-122">Długość musi być <= 9, jeśli użytkownicy planują dodać kontener systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="22a49-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="22a49-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="22a49-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="22a49-124">Czy włączyć funkcję automatycznej skalowania</span><span class="sxs-lookup"><span data-stu-id="22a49-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="22a49-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="22a49-125">-EnableRbac</span></span>
<span data-ttu-id="22a49-126">Czy włączyć Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="22a49-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="22a49-127">-Force</span><span class="sxs-lookup"><span data-stu-id="22a49-127">-Force</span></span>
<span data-ttu-id="22a49-128">Utwórz klaster, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="22a49-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="22a49-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="22a49-129">-GenerateSshKey</span></span>
<span data-ttu-id="22a49-130">Generuj plik klucza SSH na {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="22a49-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="22a49-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="22a49-131">-KubernetesVersion</span></span>
<span data-ttu-id="22a49-132">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="22a49-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="22a49-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="22a49-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="22a49-134">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="22a49-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="22a49-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="22a49-135">-LoadBalancerSku</span></span>
<span data-ttu-id="22a49-136">Wersja SKU modułu równoważenia obciążenia dla zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="22a49-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="22a49-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="22a49-137">-Location</span></span>
<span data-ttu-id="22a49-138">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="22a49-138">Azure location for the cluster.</span></span>
<span data-ttu-id="22a49-139">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22a49-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="22a49-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22a49-140">-Name</span></span>
<span data-ttu-id="22a49-141">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="22a49-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="22a49-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="22a49-142">-NetworkPlugin</span></span>
<span data-ttu-id="22a49-143">Wtyczka sieciowa używana do tworzenia sieci Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="22a49-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a49-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="22a49-144">-NodeCount</span></span>
<span data-ttu-id="22a49-145">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="22a49-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="22a49-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="22a49-146">-NodeMaxCount</span></span>
<span data-ttu-id="22a49-147">Maksymalna liczba węzłów do automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="22a49-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="22a49-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="22a49-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="22a49-149">Maksymalna liczba identyfikatorów (), które mogą być uruchamiane w węźle.</span><span class="sxs-lookup"><span data-stu-id="22a49-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="22a49-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="22a49-150">-NodeMinCount</span></span>
<span data-ttu-id="22a49-151">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="22a49-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="22a49-152">-Nodename</span><span class="sxs-lookup"><span data-stu-id="22a49-152">-NodeName</span></span>
<span data-ttu-id="22a49-153">Unikatowa nazwa profilu puli agentów w kontekście subskrypcji i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22a49-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="22a49-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="22a49-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="22a49-155">Rozmiar dysku systemu operacyjnego w GB dla każdego węzła w puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="22a49-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="22a49-156">Minimum 30 GB.</span><span class="sxs-lookup"><span data-stu-id="22a49-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="22a49-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="22a49-157">-NodePoolMode</span></span>
<span data-ttu-id="22a49-158">NodePoolMode reprezentuje tryb puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="22a49-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="22a49-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="22a49-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="22a49-160">ScaleSetEvictionPolicy do użycia w celu określenia zasad wykluczenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="22a49-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="22a49-161">Domyślnie można usunąć.</span><span class="sxs-lookup"><span data-stu-id="22a49-161">Default to Delete.</span></span>

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

### <span data-ttu-id="22a49-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="22a49-162">-NodeSetPriority</span></span>
<span data-ttu-id="22a49-163">ScaleSetPriority, aby określić priorytet zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22a49-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="22a49-164">Domyślnie na regularny.</span><span class="sxs-lookup"><span data-stu-id="22a49-164">Default to regular.</span></span>

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

### <span data-ttu-id="22a49-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="22a49-165">-NodeVmSetType</span></span>
<span data-ttu-id="22a49-166">AgentPoolType reprezentuje typy puli agentów.</span><span class="sxs-lookup"><span data-stu-id="22a49-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="22a49-167">Możliwe wartości obejmują: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="22a49-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a49-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="22a49-168">-NodeVmSize</span></span>
<span data-ttu-id="22a49-169">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22a49-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="22a49-170">Wartość domyślna to Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="22a49-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="22a49-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="22a49-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="22a49-172">SubnetID VNet określa identyfikator podsieci VNet.</span><span class="sxs-lookup"><span data-stu-id="22a49-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="22a49-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a49-173">-ResourceGroupName</span></span>
<span data-ttu-id="22a49-174">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22a49-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="22a49-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="22a49-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="22a49-176">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="22a49-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a49-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="22a49-177">-SshKeyValue</span></span>
<span data-ttu-id="22a49-178">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="22a49-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="22a49-179">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="22a49-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="22a49-180">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="22a49-180">-SubnetName</span></span>
<span data-ttu-id="22a49-181">Nazwa podsieci dodatku VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="22a49-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="22a49-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="22a49-182">-Tag</span></span>
<span data-ttu-id="22a49-183">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="22a49-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="22a49-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="22a49-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="22a49-185">Nazwa użytkownika administratora na potrzeby maszyn wirtualnych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="22a49-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="22a49-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="22a49-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="22a49-187">Hasło administratora, które ma być używane w przypadku maszyn wirtualnych systemu Windows, musi zawierać co najmniej jedno małe litery, tzn. jeden `[a-z]` `[A-Z]` znak specjalny `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="22a49-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="22a49-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="22a49-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="22a49-189">Identyfikator zasobu obszaru roboczego dla dodatku monitorowania.</span><span class="sxs-lookup"><span data-stu-id="22a49-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="22a49-190">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22a49-190">-Confirm</span></span>
<span data-ttu-id="22a49-191">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22a49-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22a49-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22a49-192">-WhatIf</span></span>
<span data-ttu-id="22a49-193">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22a49-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22a49-194">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22a49-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22a49-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a49-195">CommonParameters</span></span>
<span data-ttu-id="22a49-196">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a49-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a49-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22a49-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a49-198">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22a49-198">INPUTS</span></span>

### <span data-ttu-id="22a49-199">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="22a49-199">None</span></span>

## <span data-ttu-id="22a49-200">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22a49-200">OUTPUTS</span></span>

### <span data-ttu-id="22a49-201">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="22a49-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="22a49-202">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22a49-202">NOTES</span></span>

## <span data-ttu-id="22a49-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22a49-203">RELATED LINKS</span></span>
