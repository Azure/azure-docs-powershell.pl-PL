---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: a5a376fea0dc40bbfd02ea1cb430c725c2bc14e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052851"
---
# <span data-ttu-id="a3fc6-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="a3fc6-101">New-AzAks</span></span>

## <span data-ttu-id="a3fc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fc6-103">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a3fc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3fc6-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3fc6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3fc6-105">DESCRIPTION</span></span>

<span data-ttu-id="a3fc6-106">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a3fc6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="a3fc6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3fc6-108">Example 1</span></span>

<span data-ttu-id="a3fc6-109">Utwórz nowy klaster zarządzany Kubernetes z domyślną wartością parametry.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a3fc6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3fc6-110">PARAMETERS</span></span>

### <span data-ttu-id="a3fc6-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="a3fc6-111">-AdminUserName</span></span>
<span data-ttu-id="a3fc6-112">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="a3fc6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3fc6-113">-AsJob</span></span>
<span data-ttu-id="a3fc6-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a3fc6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3fc6-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="a3fc6-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="a3fc6-116">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="a3fc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fc6-117">-DefaultProfile</span></span>
<span data-ttu-id="a3fc6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3fc6-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a3fc6-119">-DnsNamePrefix</span></span>
<span data-ttu-id="a3fc6-120">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="a3fc6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a3fc6-121">-Force</span></span>
<span data-ttu-id="a3fc6-122">Utwórz klaster, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="a3fc6-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="a3fc6-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="a3fc6-123">-KubernetesVersion</span></span>
<span data-ttu-id="a3fc6-124">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="a3fc6-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a3fc6-125">-Location</span></span>
<span data-ttu-id="a3fc6-126">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-126">Azure location for the cluster.</span></span>
<span data-ttu-id="a3fc6-127">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="a3fc6-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3fc6-128">-Name</span></span>
<span data-ttu-id="a3fc6-129">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="a3fc6-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="a3fc6-130">-NodeCount</span></span>
<span data-ttu-id="a3fc6-131">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="a3fc6-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="a3fc6-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="a3fc6-133">Rozmiar dysku systemu operacyjnego w GB dla każdego węzła w puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="a3fc6-134">Minimum 30 GB.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="a3fc6-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="a3fc6-135">-NodeVmSize</span></span>
<span data-ttu-id="a3fc6-136">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="a3fc6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fc6-137">-ResourceGroupName</span></span>
<span data-ttu-id="a3fc6-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3fc6-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="a3fc6-139">-SshKeyValue</span></span>
<span data-ttu-id="a3fc6-140">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="a3fc6-141">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="a3fc6-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3fc6-142">-Tag</span></span>
<span data-ttu-id="a3fc6-143">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="a3fc6-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="a3fc6-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3fc6-144">-Confirm</span></span>
<span data-ttu-id="a3fc6-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3fc6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3fc6-146">-WhatIf</span></span>
<span data-ttu-id="a3fc6-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3fc6-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3fc6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fc6-149">CommonParameters</span></span>
<span data-ttu-id="a3fc6-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fc6-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3fc6-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fc6-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3fc6-152">INPUTS</span></span>

### <span data-ttu-id="a3fc6-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3fc6-153">None</span></span>

## <span data-ttu-id="a3fc6-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3fc6-154">OUTPUTS</span></span>

### <span data-ttu-id="a3fc6-155">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a3fc6-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="a3fc6-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3fc6-156">NOTES</span></span>

## <span data-ttu-id="a3fc6-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3fc6-157">RELATED LINKS</span></span>
