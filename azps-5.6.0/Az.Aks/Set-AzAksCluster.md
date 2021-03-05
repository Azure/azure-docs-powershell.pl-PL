---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0cf25018ad9cb432b739f5beeb147d20272d7f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002026"
---
# <span data-ttu-id="1a832-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="1a832-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="1a832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a832-102">SYNOPSIS</span></span>
<span data-ttu-id="1a832-103">Aktualizowanie lub tworzenie zarządzanego klastru Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="1a832-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1a832-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a832-104">SYNTAX</span></span>

### <span data-ttu-id="1a832-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="1a832-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a832-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a832-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a832-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a832-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a832-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a832-108">DESCRIPTION</span></span>
<span data-ttu-id="1a832-109">Aktualizowanie lub tworzenie zarządzanego klastru Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="1a832-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1a832-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a832-110">EXAMPLES</span></span>

### <span data-ttu-id="1a832-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a832-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="1a832-112">Ustaw liczbę węzłów w klastrze Kubernetes na 5.</span><span class="sxs-lookup"><span data-stu-id="1a832-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="1a832-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a832-113">PARAMETERS</span></span>

### <span data-ttu-id="1a832-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1a832-114">-AsJob</span></span>
<span data-ttu-id="1a832-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1a832-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a832-116">-DefaultProfile</span></span>
<span data-ttu-id="1a832-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a832-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a832-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="1a832-118">-DnsNamePrefix</span></span>
<span data-ttu-id="1a832-119">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="1a832-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="1a832-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="1a832-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="1a832-121">Czy włączyć automatyczny skaler</span><span class="sxs-lookup"><span data-stu-id="1a832-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="1a832-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="1a832-122">-Id</span></span>
<span data-ttu-id="1a832-123">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="1a832-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a832-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a832-124">-InputObject</span></span>
<span data-ttu-id="1a832-125">Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="1a832-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a832-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="1a832-126">-KubernetesVersion</span></span>
<span data-ttu-id="1a832-127">Wersja programu Kubernetes do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="1a832-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="1a832-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="1a832-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="1a832-129">Nazwa użytkownika dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="1a832-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="1a832-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1a832-130">-Location</span></span>
<span data-ttu-id="1a832-131">Lokalizacja na platformie Azure dla klastrów.</span><span class="sxs-lookup"><span data-stu-id="1a832-131">Azure location for the cluster.</span></span>
<span data-ttu-id="1a832-132">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a832-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="1a832-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1a832-133">-Name</span></span>
<span data-ttu-id="1a832-134">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="1a832-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a832-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1a832-135">-NodeCount</span></span>
<span data-ttu-id="1a832-136">Domyślna liczba węzłów dla pul węzłów.</span><span class="sxs-lookup"><span data-stu-id="1a832-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1a832-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="1a832-137">-NodeMaxCount</span></span>
<span data-ttu-id="1a832-138">Maksymalna liczba węzłów na skalowanie automatyczne</span><span class="sxs-lookup"><span data-stu-id="1a832-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="1a832-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="1a832-139">-NodeMinCount</span></span>
<span data-ttu-id="1a832-140">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="1a832-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="1a832-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1a832-141">-NodeName</span></span>
<span data-ttu-id="1a832-142">Unikatowa nazwa profilu puli agenta w kontekście grupy subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a832-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="1a832-143">-NodeOsSizeSize</span><span class="sxs-lookup"><span data-stu-id="1a832-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="1a832-144">Domyślna liczba węzłów dla pul węzłów.</span><span class="sxs-lookup"><span data-stu-id="1a832-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1a832-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="1a832-145">-NodePoolMode</span></span>
<span data-ttu-id="1a832-146">NodePoolMode reprezentuje tryb puli węzła.</span><span class="sxs-lookup"><span data-stu-id="1a832-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="1a832-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="1a832-147">-NodeVmSize</span></span>
<span data-ttu-id="1a832-148">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1a832-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="1a832-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a832-149">-ResourceGroupName</span></span>
<span data-ttu-id="1a832-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a832-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a832-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="1a832-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="1a832-152">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="1a832-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a832-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="1a832-153">-SshKeyValue</span></span>
<span data-ttu-id="1a832-154">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="1a832-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="1a832-155">Domyślnie jest to plik {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="1a832-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="1a832-156">— Tag</span><span class="sxs-lookup"><span data-stu-id="1a832-156">-Tag</span></span>
<span data-ttu-id="1a832-157">Tagi do zastosowania do zasobu</span><span class="sxs-lookup"><span data-stu-id="1a832-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="1a832-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a832-158">-Confirm</span></span>
<span data-ttu-id="1a832-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a832-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a832-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a832-160">-WhatIf</span></span>
<span data-ttu-id="1a832-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a832-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a832-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a832-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a832-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a832-163">CommonParameters</span></span>
<span data-ttu-id="1a832-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a832-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a832-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a832-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a832-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a832-166">INPUTS</span></span>

### <span data-ttu-id="1a832-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1a832-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="1a832-168">System.String</span><span class="sxs-lookup"><span data-stu-id="1a832-168">System.String</span></span>

## <span data-ttu-id="1a832-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a832-169">OUTPUTS</span></span>

### <span data-ttu-id="1a832-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1a832-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1a832-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a832-171">NOTES</span></span>

## <span data-ttu-id="1a832-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a832-172">RELATED LINKS</span></span>
