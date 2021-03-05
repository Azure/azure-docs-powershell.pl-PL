---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: 806c3a17dcfc470e01801548013d0d8c6ea58ae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008161"
---
# <span data-ttu-id="09aa3-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="09aa3-101">New-AzAksCluster</span></span>

## <span data-ttu-id="09aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="09aa3-103">Tworzenie nowego zarządzanego klastru Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="09aa3-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="09aa3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09aa3-104">SYNTAX</span></span>

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

## <span data-ttu-id="09aa3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="09aa3-105">DESCRIPTION</span></span>

<span data-ttu-id="09aa3-106">Utwórz nowy klaster usługi Azure Kubernetes(AKS).</span><span class="sxs-lookup"><span data-stu-id="09aa3-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="09aa3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="09aa3-108">Nowy element AKS z domyślnymi parami.</span><span class="sxs-lookup"><span data-stu-id="09aa3-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="09aa3-109">Utwórz kontener systemu Windows Server na serwerze AKS.</span><span class="sxs-lookup"><span data-stu-id="09aa3-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="09aa3-110">Aby utworzyć kontener systemu Windows Server w serwerze AKS, podczas tworzenia serwera AKS należy określić co najmniej cztery następujące parametry, a także wartość, odpowiednio i `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` dla.</span><span class="sxs-lookup"><span data-stu-id="09aa3-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="09aa3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09aa3-111">PARAMETERS</span></span>

### <span data-ttu-id="09aa3-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="09aa3-112">-AcrNameToAttach</span></span>
<span data-ttu-id="09aa3-113">Udzielanie funkcji "acrpull" określonej funkcji ACR podmiotowi zabezpieczeń usługi AKS, na przykład funkcji myacr</span><span class="sxs-lookup"><span data-stu-id="09aa3-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="09aa3-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="09aa3-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="09aa3-115">Nazwy dodatków, które mają być włączone podczas tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="09aa3-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="09aa3-116">-AsJob</span></span>
<span data-ttu-id="09aa3-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="09aa3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09aa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09aa3-118">-DefaultProfile</span></span>
<span data-ttu-id="09aa3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09aa3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09aa3-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="09aa3-120">-DnsNamePrefix</span></span>
<span data-ttu-id="09aa3-121">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="09aa3-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="09aa3-122">Długość musi być <= 9, jeśli użytkownicy planują dodać kontener systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="09aa3-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="09aa3-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="09aa3-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="09aa3-124">Czy włączyć automatyczny skaler</span><span class="sxs-lookup"><span data-stu-id="09aa3-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="09aa3-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="09aa3-125">-EnableRbac</span></span>
<span data-ttu-id="09aa3-126">Czy włączyć opcję Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="09aa3-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="09aa3-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="09aa3-127">-Force</span></span>
<span data-ttu-id="09aa3-128">Tworzenie klastrów, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="09aa3-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="09aa3-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="09aa3-129">-GenerateSshKey</span></span>
<span data-ttu-id="09aa3-130">Wygeneruj plik klucza ssh do {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="09aa3-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="09aa3-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="09aa3-131">-KubernetesVersion</span></span>
<span data-ttu-id="09aa3-132">Wersja programu Kubernetes do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="09aa3-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="09aa3-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="09aa3-134">Nazwa użytkownika dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="09aa3-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="09aa3-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="09aa3-135">-LoadBalancerSku</span></span>
<span data-ttu-id="09aa3-136">SKU równoważenia obciążenia dla klastra zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="09aa3-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="09aa3-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="09aa3-137">-Location</span></span>
<span data-ttu-id="09aa3-138">Lokalizacja na platformie Azure dla klastrów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-138">Azure location for the cluster.</span></span>
<span data-ttu-id="09aa3-139">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="09aa3-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09aa3-140">-Name</span></span>
<span data-ttu-id="09aa3-141">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="09aa3-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="09aa3-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="09aa3-142">-NetworkPlugin</span></span>
<span data-ttu-id="09aa3-143">Wtyczka sieciowa używana do tworzenia sieci Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="09aa3-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="09aa3-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="09aa3-144">-NodeCount</span></span>
<span data-ttu-id="09aa3-145">Domyślna liczba węzłów dla pul węzłów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="09aa3-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="09aa3-146">-NodeMaxCount</span></span>
<span data-ttu-id="09aa3-147">Maksymalna liczba węzłów na skalowanie automatyczne</span><span class="sxs-lookup"><span data-stu-id="09aa3-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="09aa3-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="09aa3-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="09aa3-149">Maksymalna liczba zasobników, które mogą być uruchamiane w węźle.</span><span class="sxs-lookup"><span data-stu-id="09aa3-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="09aa3-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="09aa3-150">-NodeMinCount</span></span>
<span data-ttu-id="09aa3-151">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="09aa3-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="09aa3-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="09aa3-152">-NodeName</span></span>
<span data-ttu-id="09aa3-153">Unikatowa nazwa profilu puli agenta w kontekście grupy subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="09aa3-154">-NodeOsSizeSize</span><span class="sxs-lookup"><span data-stu-id="09aa3-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="09aa3-155">Rozmiar w GB dysku systemu operacyjnego dla każdego węzła w puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="09aa3-156">Co najmniej 30 GB.</span><span class="sxs-lookup"><span data-stu-id="09aa3-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="09aa3-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="09aa3-157">-NodePoolMode</span></span>
<span data-ttu-id="09aa3-158">NodePoolMode reprezentuje tryb puli węzła.</span><span class="sxs-lookup"><span data-stu-id="09aa3-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="09aa3-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="09aa3-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="09aa3-160">ScaleSetEvictionPolicy, która ma być używana do określania zasad wywrócenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="09aa3-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="09aa3-161">Domyślnie usuń.</span><span class="sxs-lookup"><span data-stu-id="09aa3-161">Default to Delete.</span></span>

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

### <span data-ttu-id="09aa3-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="09aa3-162">-NodeSetPriority</span></span>
<span data-ttu-id="09aa3-163">ScaleSetPriority, która ma być używana do określania priorytetu zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="09aa3-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="09aa3-164">Domyślnie jest to zwykły.</span><span class="sxs-lookup"><span data-stu-id="09aa3-164">Default to regular.</span></span>

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

### <span data-ttu-id="09aa3-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="09aa3-165">-NodeVmSetType</span></span>
<span data-ttu-id="09aa3-166">Typ AgentPoolType reprezentuje typy puli agenta.</span><span class="sxs-lookup"><span data-stu-id="09aa3-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="09aa3-167">Możliwe wartości: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="09aa3-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="09aa3-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="09aa3-168">-NodeVmSize</span></span>
<span data-ttu-id="09aa3-169">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="09aa3-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="09aa3-170">Wartość domyślna to Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="09aa3-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="09aa3-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="09aa3-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="09aa3-172">Identyfikator podsieci wirtualnej określa identyfikator podsieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="09aa3-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="09aa3-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09aa3-173">-ResourceGroupName</span></span>
<span data-ttu-id="09aa3-174">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09aa3-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="09aa3-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="09aa3-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="09aa3-176">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="09aa3-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="09aa3-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="09aa3-177">-SshKeyValue</span></span>
<span data-ttu-id="09aa3-178">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="09aa3-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="09aa3-179">Domyślnie jest to plik {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="09aa3-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="09aa3-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="09aa3-180">-SubnetName</span></span>
<span data-ttu-id="09aa3-181">Nazwa podsieci dodatku VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="09aa3-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="09aa3-182">— Tag</span><span class="sxs-lookup"><span data-stu-id="09aa3-182">-Tag</span></span>
<span data-ttu-id="09aa3-183">Tagi do zastosowania do zasobu</span><span class="sxs-lookup"><span data-stu-id="09aa3-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="09aa3-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="09aa3-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="09aa3-185">Nazwa użytkownika administratora do użycia dla maszyn wirtualnych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="09aa3-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="09aa3-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="09aa3-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="09aa3-187">Hasło administratora do używania dla maszyn wirtualnych systemu Windows, jego długość musi mieć długość co najmniej 12, zawierającą co najmniej jeden znak mniejszy, czyli jeden i `[a-z]` `[A-Z]` jeden znak `[!@#$%^&*()]` specjalny.</span><span class="sxs-lookup"><span data-stu-id="09aa3-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="09aa3-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="09aa3-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="09aa3-189">Identyfikator zasobu obszaru roboczego dodatku Monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="09aa3-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="09aa3-190">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09aa3-190">-Confirm</span></span>
<span data-ttu-id="09aa3-191">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09aa3-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09aa3-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09aa3-192">-WhatIf</span></span>
<span data-ttu-id="09aa3-193">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09aa3-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09aa3-194">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09aa3-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09aa3-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09aa3-195">CommonParameters</span></span>
<span data-ttu-id="09aa3-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09aa3-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09aa3-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09aa3-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09aa3-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09aa3-198">INPUTS</span></span>

### <span data-ttu-id="09aa3-199">Brak</span><span class="sxs-lookup"><span data-stu-id="09aa3-199">None</span></span>

## <span data-ttu-id="09aa3-200">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09aa3-200">OUTPUTS</span></span>

### <span data-ttu-id="09aa3-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="09aa3-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="09aa3-202">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09aa3-202">NOTES</span></span>

## <span data-ttu-id="09aa3-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09aa3-203">RELATED LINKS</span></span>
