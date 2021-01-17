---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332818"
---
# <span data-ttu-id="5dab2-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="5dab2-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="5dab2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5dab2-102">SYNOPSIS</span></span>
<span data-ttu-id="5dab2-103">Zaktualizuj lub Utwórz zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5dab2-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5dab2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5dab2-104">SYNTAX</span></span>

### <span data-ttu-id="5dab2-105">defaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5dab2-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dab2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dab2-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dab2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dab2-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dab2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5dab2-108">DESCRIPTION</span></span>
<span data-ttu-id="5dab2-109">Zaktualizuj lub Utwórz zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5dab2-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5dab2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5dab2-110">EXAMPLES</span></span>

### <span data-ttu-id="5dab2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5dab2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="5dab2-112">Ustaw liczbę węzłów w klastrze Kubernetes na 5.</span><span class="sxs-lookup"><span data-stu-id="5dab2-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="5dab2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5dab2-113">PARAMETERS</span></span>

### <span data-ttu-id="5dab2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dab2-114">-AsJob</span></span>
<span data-ttu-id="5dab2-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5dab2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5dab2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dab2-116">-DefaultProfile</span></span>
<span data-ttu-id="5dab2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5dab2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dab2-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5dab2-118">-DnsNamePrefix</span></span>
<span data-ttu-id="5dab2-119">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="5dab2-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="5dab2-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="5dab2-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="5dab2-121">Czy włączyć funkcję automatycznej skalowania</span><span class="sxs-lookup"><span data-stu-id="5dab2-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="5dab2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5dab2-122">-Id</span></span>
<span data-ttu-id="5dab2-123">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="5dab2-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5dab2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5dab2-124">-InputObject</span></span>
<span data-ttu-id="5dab2-125">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5dab2-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5dab2-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="5dab2-126">-KubernetesVersion</span></span>
<span data-ttu-id="5dab2-127">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="5dab2-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="5dab2-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="5dab2-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="5dab2-129">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="5dab2-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="5dab2-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5dab2-130">-Location</span></span>
<span data-ttu-id="5dab2-131">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="5dab2-131">Azure location for the cluster.</span></span>
<span data-ttu-id="5dab2-132">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5dab2-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="5dab2-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5dab2-133">-Name</span></span>
<span data-ttu-id="5dab2-134">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="5dab2-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="5dab2-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5dab2-135">-NodeCount</span></span>
<span data-ttu-id="5dab2-136">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="5dab2-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="5dab2-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="5dab2-137">-NodeMaxCount</span></span>
<span data-ttu-id="5dab2-138">Maksymalna liczba węzłów do automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="5dab2-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="5dab2-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="5dab2-139">-NodeMinCount</span></span>
<span data-ttu-id="5dab2-140">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="5dab2-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="5dab2-141">-Nodename</span><span class="sxs-lookup"><span data-stu-id="5dab2-141">-NodeName</span></span>
<span data-ttu-id="5dab2-142">Unikatowa nazwa profilu puli agentów w kontekście subskrypcji i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5dab2-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="5dab2-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="5dab2-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="5dab2-144">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="5dab2-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="5dab2-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="5dab2-145">-NodePoolMode</span></span>
<span data-ttu-id="5dab2-146">NodePoolMode reprezentuje tryb puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="5dab2-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="5dab2-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="5dab2-147">-NodeVmSize</span></span>
<span data-ttu-id="5dab2-148">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5dab2-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="5dab2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dab2-149">-ResourceGroupName</span></span>
<span data-ttu-id="5dab2-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5dab2-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="5dab2-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="5dab2-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="5dab2-152">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="5dab2-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="5dab2-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="5dab2-153">-SshKeyValue</span></span>
<span data-ttu-id="5dab2-154">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="5dab2-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="5dab2-155">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="5dab2-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="5dab2-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="5dab2-156">-Tag</span></span>
<span data-ttu-id="5dab2-157">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="5dab2-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="5dab2-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5dab2-158">-Confirm</span></span>
<span data-ttu-id="5dab2-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dab2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dab2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dab2-160">-WhatIf</span></span>
<span data-ttu-id="5dab2-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dab2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dab2-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5dab2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dab2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dab2-163">CommonParameters</span></span>
<span data-ttu-id="5dab2-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dab2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dab2-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dab2-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dab2-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5dab2-166">INPUTS</span></span>

### <span data-ttu-id="5dab2-167">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5dab2-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="5dab2-168">System. String</span><span class="sxs-lookup"><span data-stu-id="5dab2-168">System.String</span></span>

## <span data-ttu-id="5dab2-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5dab2-169">OUTPUTS</span></span>

### <span data-ttu-id="5dab2-170">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5dab2-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="5dab2-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5dab2-171">NOTES</span></span>

## <span data-ttu-id="5dab2-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5dab2-172">RELATED LINKS</span></span>
