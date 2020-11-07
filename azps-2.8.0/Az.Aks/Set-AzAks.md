---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707166"
---
# <span data-ttu-id="aee5a-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="aee5a-101">Set-AzAks</span></span>

## <span data-ttu-id="aee5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aee5a-102">SYNOPSIS</span></span>
<span data-ttu-id="aee5a-103">Zaktualizuj lub Utwórz zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="aee5a-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="aee5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aee5a-104">SYNTAX</span></span>

### <span data-ttu-id="aee5a-105">defaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aee5a-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee5a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee5a-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee5a-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee5a-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aee5a-108">DESCRIPTION</span></span>
<span data-ttu-id="aee5a-109">Zaktualizuj lub Utwórz zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="aee5a-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="aee5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aee5a-110">EXAMPLES</span></span>

### <span data-ttu-id="aee5a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aee5a-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="aee5a-112">Ustaw liczbę węzłów w klastrze Kubernetes na 5.</span><span class="sxs-lookup"><span data-stu-id="aee5a-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="aee5a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aee5a-113">PARAMETERS</span></span>

### <span data-ttu-id="aee5a-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="aee5a-114">-AdminUserName</span></span>
<span data-ttu-id="aee5a-115">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="aee5a-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="aee5a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aee5a-116">-AsJob</span></span>
<span data-ttu-id="aee5a-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="aee5a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aee5a-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="aee5a-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="aee5a-119">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="aee5a-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="aee5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee5a-120">-DefaultProfile</span></span>
<span data-ttu-id="aee5a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aee5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee5a-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="aee5a-122">-DnsNamePrefix</span></span>
<span data-ttu-id="aee5a-123">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="aee5a-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="aee5a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="aee5a-124">-Id</span></span>
<span data-ttu-id="aee5a-125">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="aee5a-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="aee5a-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aee5a-126">-InputObject</span></span>
<span data-ttu-id="aee5a-127">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="aee5a-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="aee5a-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="aee5a-128">-KubernetesVersion</span></span>
<span data-ttu-id="aee5a-129">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="aee5a-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="aee5a-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aee5a-130">-Location</span></span>
<span data-ttu-id="aee5a-131">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="aee5a-131">Azure location for the cluster.</span></span>
<span data-ttu-id="aee5a-132">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aee5a-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="aee5a-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aee5a-133">-Name</span></span>
<span data-ttu-id="aee5a-134">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="aee5a-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="aee5a-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="aee5a-135">-NodeCount</span></span>
<span data-ttu-id="aee5a-136">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="aee5a-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="aee5a-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="aee5a-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="aee5a-138">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="aee5a-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="aee5a-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="aee5a-139">-NodeVmSize</span></span>
<span data-ttu-id="aee5a-140">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aee5a-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="aee5a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee5a-141">-ResourceGroupName</span></span>
<span data-ttu-id="aee5a-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aee5a-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="aee5a-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="aee5a-143">-SshKeyValue</span></span>
<span data-ttu-id="aee5a-144">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="aee5a-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="aee5a-145">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="aee5a-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="aee5a-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="aee5a-146">-Tag</span></span>
<span data-ttu-id="aee5a-147">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="aee5a-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="aee5a-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aee5a-148">-Confirm</span></span>
<span data-ttu-id="aee5a-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aee5a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee5a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee5a-150">-WhatIf</span></span>
<span data-ttu-id="aee5a-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aee5a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aee5a-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aee5a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee5a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee5a-153">CommonParameters</span></span>
<span data-ttu-id="aee5a-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee5a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee5a-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aee5a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee5a-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aee5a-156">INPUTS</span></span>

### <span data-ttu-id="aee5a-157">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="aee5a-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="aee5a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="aee5a-158">System.String</span></span>

## <span data-ttu-id="aee5a-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aee5a-159">OUTPUTS</span></span>

### <span data-ttu-id="aee5a-160">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="aee5a-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="aee5a-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aee5a-161">NOTES</span></span>

## <span data-ttu-id="aee5a-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aee5a-162">RELATED LINKS</span></span>
