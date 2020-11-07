---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707170"
---
# <span data-ttu-id="0bb7d-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="0bb7d-101">New-AzAks</span></span>

## <span data-ttu-id="0bb7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb7d-103">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0bb7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bb7d-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0bb7d-105">DESCRIPTION</span></span>

<span data-ttu-id="0bb7d-106">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0bb7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bb7d-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb7d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0bb7d-108">Example 1</span></span>

<span data-ttu-id="0bb7d-109">Utwórz nowy klaster zarządzany Kubernetes z domyślną wartością parametry.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="0bb7d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bb7d-110">PARAMETERS</span></span>

### <span data-ttu-id="0bb7d-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="0bb7d-111">-AdminUserName</span></span>
<span data-ttu-id="0bb7d-112">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="0bb7d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bb7d-113">-AsJob</span></span>
<span data-ttu-id="0bb7d-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0bb7d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bb7d-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="0bb7d-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="0bb7d-116">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="0bb7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb7d-117">-DefaultProfile</span></span>
<span data-ttu-id="0bb7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bb7d-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0bb7d-119">-DnsNamePrefix</span></span>
<span data-ttu-id="0bb7d-120">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="0bb7d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0bb7d-121">-Force</span></span>
<span data-ttu-id="0bb7d-122">Utwórz klaster, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="0bb7d-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="0bb7d-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="0bb7d-123">-KubernetesVersion</span></span>
<span data-ttu-id="0bb7d-124">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="0bb7d-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0bb7d-125">-Location</span></span>
<span data-ttu-id="0bb7d-126">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-126">Azure location for the cluster.</span></span>
<span data-ttu-id="0bb7d-127">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="0bb7d-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bb7d-128">-Name</span></span>
<span data-ttu-id="0bb7d-129">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="0bb7d-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="0bb7d-130">-NodeCount</span></span>
<span data-ttu-id="0bb7d-131">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="0bb7d-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="0bb7d-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="0bb7d-133">Rozmiar dysku systemu operacyjnego w GB dla każdego węzła w puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="0bb7d-134">Minimum 30 GB.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="0bb7d-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="0bb7d-135">-NodeVmSize</span></span>
<span data-ttu-id="0bb7d-136">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="0bb7d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb7d-137">-ResourceGroupName</span></span>
<span data-ttu-id="0bb7d-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="0bb7d-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="0bb7d-139">-SshKeyValue</span></span>
<span data-ttu-id="0bb7d-140">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="0bb7d-141">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="0bb7d-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="0bb7d-142">-Tag</span></span>
<span data-ttu-id="0bb7d-143">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="0bb7d-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="0bb7d-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bb7d-144">-Confirm</span></span>
<span data-ttu-id="0bb7d-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb7d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb7d-146">-WhatIf</span></span>
<span data-ttu-id="0bb7d-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bb7d-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb7d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb7d-149">CommonParameters</span></span>
<span data-ttu-id="0bb7d-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb7d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb7d-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb7d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb7d-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bb7d-152">INPUTS</span></span>

### <span data-ttu-id="0bb7d-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0bb7d-153">None</span></span>

## <span data-ttu-id="0bb7d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bb7d-154">OUTPUTS</span></span>

### <span data-ttu-id="0bb7d-155">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0bb7d-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="0bb7d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bb7d-156">NOTES</span></span>

## <span data-ttu-id="0bb7d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bb7d-157">RELATED LINKS</span></span>
