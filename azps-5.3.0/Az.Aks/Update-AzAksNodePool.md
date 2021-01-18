---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500478"
---
# <span data-ttu-id="3e29b-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="3e29b-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="3e29b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e29b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e29b-103">Aktualizowanie puli węzłów w zarządzanym klastrze.</span><span class="sxs-lookup"><span data-stu-id="3e29b-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="3e29b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e29b-104">SYNTAX</span></span>

### <span data-ttu-id="3e29b-105">defaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e29b-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e29b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e29b-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e29b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e29b-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e29b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e29b-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e29b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3e29b-109">DESCRIPTION</span></span>
<span data-ttu-id="3e29b-110">Aktualizowanie puli węzłów w zarządzanym klastrze.</span><span class="sxs-lookup"><span data-stu-id="3e29b-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="3e29b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e29b-111">EXAMPLES</span></span>

### <span data-ttu-id="3e29b-112">Zmień minimun liczbę na 5 dla określonej puli węzłów</span><span class="sxs-lookup"><span data-stu-id="3e29b-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="3e29b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e29b-113">PARAMETERS</span></span>

### <span data-ttu-id="3e29b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e29b-114">-AsJob</span></span>
<span data-ttu-id="3e29b-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3e29b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e29b-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="3e29b-116">-ClusterName</span></span>
<span data-ttu-id="3e29b-117">Nazwa zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="3e29b-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e29b-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="3e29b-118">-ClusterObject</span></span>
<span data-ttu-id="3e29b-119">Obiekt klastra</span><span class="sxs-lookup"><span data-stu-id="3e29b-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e29b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e29b-120">-DefaultProfile</span></span>
<span data-ttu-id="3e29b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e29b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e29b-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="3e29b-122">-EnableAutoScaling</span></span>
<span data-ttu-id="3e29b-123">Czy włączyć funkcję automatycznej skalowania</span><span class="sxs-lookup"><span data-stu-id="3e29b-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="3e29b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3e29b-124">-Force</span></span>
<span data-ttu-id="3e29b-125">Aktualizowanie puli węzłów bez monitowania</span><span class="sxs-lookup"><span data-stu-id="3e29b-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="3e29b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3e29b-126">-Id</span></span>
<span data-ttu-id="3e29b-127">Identyfikator puli węzłów w klastrze zarządzanych Kubernetes</span><span class="sxs-lookup"><span data-stu-id="3e29b-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e29b-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e29b-128">-InputObject</span></span>
<span data-ttu-id="3e29b-129">Obiekt PSAgentPool, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3e29b-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e29b-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="3e29b-130">-KubernetesVersion</span></span>
<span data-ttu-id="3e29b-131">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="3e29b-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="3e29b-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3e29b-132">-MaxCount</span></span>
<span data-ttu-id="3e29b-133">Maksymalna liczba węzłów do automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="3e29b-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="3e29b-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="3e29b-134">-MinCount</span></span>
<span data-ttu-id="3e29b-135">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="3e29b-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="3e29b-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e29b-136">-Name</span></span>
<span data-ttu-id="3e29b-137">Nazwa puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="3e29b-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e29b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e29b-138">-ResourceGroupName</span></span>
<span data-ttu-id="3e29b-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e29b-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e29b-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e29b-140">-Confirm</span></span>
<span data-ttu-id="3e29b-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e29b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e29b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e29b-142">-WhatIf</span></span>
<span data-ttu-id="3e29b-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e29b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e29b-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e29b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e29b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e29b-145">CommonParameters</span></span>
<span data-ttu-id="3e29b-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e29b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e29b-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e29b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e29b-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e29b-148">INPUTS</span></span>

### <span data-ttu-id="3e29b-149">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="3e29b-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="3e29b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3e29b-150">System.String</span></span>

## <span data-ttu-id="3e29b-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e29b-151">OUTPUTS</span></span>

### <span data-ttu-id="3e29b-152">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="3e29b-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="3e29b-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e29b-153">NOTES</span></span>

## <span data-ttu-id="3e29b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e29b-154">RELATED LINKS</span></span>
