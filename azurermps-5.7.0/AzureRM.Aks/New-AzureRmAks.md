---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718970"
---
# <span data-ttu-id="5a4f8-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="5a4f8-101">New-AzureRmAks</span></span>

## <span data-ttu-id="5a4f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4f8-103">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a4f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a4f8-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4f8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a4f8-105">DESCRIPTION</span></span>
<span data-ttu-id="5a4f8-106">Utwórz nowy klaster zarządzany Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5a4f8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a4f8-107">EXAMPLES</span></span>

### <span data-ttu-id="5a4f8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a4f8-108">Example 1</span></span>
<span data-ttu-id="5a4f8-109">Tworzenie nowego klastra zarządzanego Kubernetes z wartością domyślną parametry</span><span class="sxs-lookup"><span data-stu-id="5a4f8-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="5a4f8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a4f8-110">PARAMETERS</span></span>

### <span data-ttu-id="5a4f8-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="5a4f8-111">-AdminUserName</span></span>
<span data-ttu-id="5a4f8-112">Nazwa użytkownika dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a4f8-113">-AsJob</span></span>
<span data-ttu-id="5a4f8-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5a4f8-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="5a4f8-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="5a4f8-116">Identyfikator klienta i klucz tajny klienta skojarzone z podmiotem zabezpieczeń aplikacji/usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4f8-117">-DefaultProfile</span></span>
<span data-ttu-id="5a4f8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5a4f8-119">-DnsNamePrefix</span></span>
<span data-ttu-id="5a4f8-120">Prefiks nazwy DNS dla klastra.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5a4f8-121">-Force</span></span>
<span data-ttu-id="5a4f8-122">Utwórz klaster, nawet jeśli już istnieje</span><span class="sxs-lookup"><span data-stu-id="5a4f8-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="5a4f8-123">-KubernetesVersion</span></span>
<span data-ttu-id="5a4f8-124">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5a4f8-125">-Location</span></span>
<span data-ttu-id="5a4f8-126">Lokalizacja platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-126">Azure location for the cluster.</span></span>
<span data-ttu-id="5a4f8-127">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a4f8-128">-Name</span></span>
<span data-ttu-id="5a4f8-129">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5a4f8-130">-NodeCount</span></span>
<span data-ttu-id="5a4f8-131">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="5a4f8-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="5a4f8-133">Domyślna liczba węzłów puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="5a4f8-134">-NodeVmSize</span></span>
<span data-ttu-id="5a4f8-135">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4f8-136">-ResourceGroupName</span></span>
<span data-ttu-id="5a4f8-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="5a4f8-138">-SshKeyValue</span></span>
<span data-ttu-id="5a4f8-139">Wartość pliku klucza SSH lub ścieżka pliku klucza.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="5a4f8-140">Domyślnie jest to {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a4f8-141">-Tag</span></span>
<span data-ttu-id="5a4f8-142">Znaczniki, które mają zostać zastosowane do zasobu</span><span class="sxs-lookup"><span data-stu-id="5a4f8-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a4f8-143">-Confirm</span></span>
<span data-ttu-id="5a4f8-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4f8-145">-WhatIf</span></span>
<span data-ttu-id="5a4f8-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4f8-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4f8-148">CommonParameters</span></span>
<span data-ttu-id="5a4f8-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4f8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4f8-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4f8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4f8-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a4f8-151">INPUTS</span></span>

### <span data-ttu-id="5a4f8-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5a4f8-152">None</span></span>

## <span data-ttu-id="5a4f8-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a4f8-153">OUTPUTS</span></span>

### <span data-ttu-id="5a4f8-154">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5a4f8-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="5a4f8-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a4f8-155">NOTES</span></span>

## <span data-ttu-id="5a4f8-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a4f8-156">RELATED LINKS</span></span>
