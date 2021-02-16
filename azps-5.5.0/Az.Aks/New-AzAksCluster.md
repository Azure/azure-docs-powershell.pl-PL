---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: c0eeaedfc98f8225b097345908638d52bb4ed297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199850"
---
# <span data-ttu-id="87580-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="87580-101">New-AzAksCluster</span></span>

## <span data-ttu-id="87580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87580-102">SYNOPSIS</span></span>
<span data-ttu-id="87580-103">Tworzenie nowego zarządzanego klastru Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="87580-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="87580-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87580-104">SYNTAX</span></span>

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

## <span data-ttu-id="87580-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87580-105">DESCRIPTION</span></span>

<span data-ttu-id="87580-106">Utwórz nowy klaster usługi Azure Kubernetes(AKS).</span><span class="sxs-lookup"><span data-stu-id="87580-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="87580-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87580-107">EXAMPLES</span></span>

### <span data-ttu-id="87580-108">Nowy element AKS z domyślnymi parami.</span><span class="sxs-lookup"><span data-stu-id="87580-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="87580-109">Utwórz kontener systemu Windows Server na serwerze AKS.</span><span class="sxs-lookup"><span data-stu-id="87580-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="87580-110">Aby utworzyć kontener systemu Windows Server w aKS, podczas tworzenia serwera AKS należy określić co najmniej cztery następujące parametry, a także wartość, odpowiednio i `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` dla.</span><span class="sxs-lookup"><span data-stu-id="87580-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="87580-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87580-111">PARAMETERS</span></span>

### <span data-ttu-id="87580-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="87580-112">-AcrNameToAttach</span></span>
<span data-ttu-id="87580-113">Udzielanie funkcji "acrpull" określonej funkcji ACR podmiotowi zabezpieczeń usługi AKS, na przykład funkcji myacr</span><span class="sxs-lookup"><span data-stu-id="87580-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="87580-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="87580-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="87580-115">Nazwy dodatków, które mają być włączone podczas tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="87580-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="87580-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="87580-116">-AsJob</span></span>
<span data-ttu-id="87580-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="87580-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87580-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87580-118">-DefaultProfile</span></span>
<span data-ttu-id="87580-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87580-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87580-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="87580-120">-DnsNamePrefix</span></span>
<span data-ttu-id="87580-121">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="87580-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="87580-122">Długość musi być <= 9, jeśli użytkownicy planują dodać kontener systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="87580-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="87580-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="87580-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="87580-124">Czy należy włączyć automatyczny skaler</span><span class="sxs-lookup"><span data-stu-id="87580-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="87580-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="87580-125">-EnableRbac</span></span>
<span data-ttu-id="87580-126">Czy włączyć opcję Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="87580-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="87580-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="87580-127">-Force</span></span>
<span data-ttu-id="87580-128">Tworzenie klastrów, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="87580-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="87580-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="87580-129">-GenerateSshKey</span></span>
<span data-ttu-id="87580-130">Wygeneruj plik klucza ssh do {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="87580-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="87580-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="87580-131">-KubernetesVersion</span></span>
<span data-ttu-id="87580-132">Wersja programu Kubernetes do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="87580-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="87580-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="87580-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="87580-134">Nazwa użytkownika dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="87580-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="87580-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="87580-135">-LoadBalancerSku</span></span>
<span data-ttu-id="87580-136">SKU równoważenia obciążenia dla klastra zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="87580-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="87580-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="87580-137">-Location</span></span>
<span data-ttu-id="87580-138">Lokalizacja na platformie Azure dla klastrów.</span><span class="sxs-lookup"><span data-stu-id="87580-138">Azure location for the cluster.</span></span>
<span data-ttu-id="87580-139">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87580-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="87580-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87580-140">-Name</span></span>
<span data-ttu-id="87580-141">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="87580-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="87580-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="87580-142">-NetworkPlugin</span></span>
<span data-ttu-id="87580-143">Wtyczka sieciowa używana do tworzenia sieci Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="87580-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="87580-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="87580-144">-NodeCount</span></span>
<span data-ttu-id="87580-145">Domyślna liczba węzłów dla pul węzłów.</span><span class="sxs-lookup"><span data-stu-id="87580-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="87580-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="87580-146">-NodeMaxCount</span></span>
<span data-ttu-id="87580-147">Maksymalna liczba węzłów na skalowanie automatyczne</span><span class="sxs-lookup"><span data-stu-id="87580-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="87580-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="87580-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="87580-149">Maksymalna liczba zasobników, które mogą być uruchamiane w węźle.</span><span class="sxs-lookup"><span data-stu-id="87580-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="87580-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="87580-150">-NodeMinCount</span></span>
<span data-ttu-id="87580-151">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="87580-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="87580-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="87580-152">-NodeName</span></span>
<span data-ttu-id="87580-153">Unikatowa nazwa profilu puli agenta w kontekście grupy subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="87580-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="87580-154">-NodeOsSizeSize</span><span class="sxs-lookup"><span data-stu-id="87580-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="87580-155">Rozmiar w GB dysku systemu operacyjnego dla każdego węzła w puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="87580-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="87580-156">Co najmniej 30 GB.</span><span class="sxs-lookup"><span data-stu-id="87580-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="87580-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="87580-157">-NodePoolMode</span></span>
<span data-ttu-id="87580-158">NodePoolMode reprezentuje tryb puli węzła.</span><span class="sxs-lookup"><span data-stu-id="87580-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="87580-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="87580-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="87580-160">ScaleSetEvictionPolicy, która ma być używana do określania zasad wywrócenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="87580-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="87580-161">Domyślnie usuń.</span><span class="sxs-lookup"><span data-stu-id="87580-161">Default to Delete.</span></span>

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

### <span data-ttu-id="87580-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="87580-162">-NodeSetPriority</span></span>
<span data-ttu-id="87580-163">ScaleSetPriority, która ma być używana do określania priorytetu zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87580-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="87580-164">Domyślnie jest to zwykły.</span><span class="sxs-lookup"><span data-stu-id="87580-164">Default to regular.</span></span>

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

### <span data-ttu-id="87580-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="87580-165">-NodeVmSetType</span></span>
<span data-ttu-id="87580-166">Typ AgentPoolType reprezentuje typy puli agenta.</span><span class="sxs-lookup"><span data-stu-id="87580-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="87580-167">Możliwe wartości: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="87580-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="87580-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="87580-168">-NodeVmSize</span></span>
<span data-ttu-id="87580-169">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87580-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="87580-170">Wartość domyślna Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="87580-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="87580-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="87580-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="87580-172">Identyfikator podsieci wirtualnej określa identyfikator podsieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87580-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="87580-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87580-173">-ResourceGroupName</span></span>
<span data-ttu-id="87580-174">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87580-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="87580-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="87580-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="87580-176">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="87580-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="87580-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="87580-177">-SshKeyValue</span></span>
<span data-ttu-id="87580-178">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="87580-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="87580-179">Domyślnie jest to plik {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="87580-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="87580-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="87580-180">-SubnetName</span></span>
<span data-ttu-id="87580-181">Nazwa podsieci dodatku VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="87580-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="87580-182">— Tag</span><span class="sxs-lookup"><span data-stu-id="87580-182">-Tag</span></span>
<span data-ttu-id="87580-183">Tagi do zastosowania do zasobu</span><span class="sxs-lookup"><span data-stu-id="87580-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="87580-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="87580-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="87580-185">Nazwa użytkownika administratora do użycia dla maszyn wirtualnych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="87580-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="87580-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="87580-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="87580-187">Hasło administratora do używania dla maszyn wirtualnych systemu Windows, jego długość musi mieć długość co najmniej 12, zawierającą co najmniej jeden znak mniejszy, czyli jeden i `[a-z]` `[A-Z]` jeden znak `[!@#$%^&*()]` specjalny.</span><span class="sxs-lookup"><span data-stu-id="87580-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="87580-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="87580-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="87580-189">Identyfikator zasobu obszaru roboczego dodatku Monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="87580-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="87580-190">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87580-190">-Confirm</span></span>
<span data-ttu-id="87580-191">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87580-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87580-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87580-192">-WhatIf</span></span>
<span data-ttu-id="87580-193">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87580-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87580-194">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87580-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87580-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87580-195">CommonParameters</span></span>
<span data-ttu-id="87580-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87580-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87580-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87580-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87580-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87580-198">INPUTS</span></span>

### <span data-ttu-id="87580-199">Brak</span><span class="sxs-lookup"><span data-stu-id="87580-199">None</span></span>

## <span data-ttu-id="87580-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87580-200">OUTPUTS</span></span>

### <span data-ttu-id="87580-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="87580-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="87580-202">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87580-202">NOTES</span></span>

## <span data-ttu-id="87580-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87580-203">RELATED LINKS</span></span>
