---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348853"
---
# <span data-ttu-id="68802-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="68802-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="68802-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68802-102">SYNOPSIS</span></span>
<span data-ttu-id="68802-103">Aktualizowanie puli węzłów w zarządzanym klastrze.</span><span class="sxs-lookup"><span data-stu-id="68802-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="68802-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68802-104">SYNTAX</span></span>

### <span data-ttu-id="68802-105">defaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="68802-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68802-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68802-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68802-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68802-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68802-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68802-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68802-109">Opis</span><span class="sxs-lookup"><span data-stu-id="68802-109">DESCRIPTION</span></span>
<span data-ttu-id="68802-110">Aktualizowanie puli węzłów w zarządzanym klastrze.</span><span class="sxs-lookup"><span data-stu-id="68802-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="68802-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68802-111">EXAMPLES</span></span>

### <span data-ttu-id="68802-112">Zmień minimun liczbę na 5 dla określonej puli węzłów</span><span class="sxs-lookup"><span data-stu-id="68802-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="68802-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68802-113">PARAMETERS</span></span>

### <span data-ttu-id="68802-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68802-114">-AsJob</span></span>
<span data-ttu-id="68802-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="68802-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68802-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="68802-116">-ClusterName</span></span>
<span data-ttu-id="68802-117">Nazwa zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="68802-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="68802-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="68802-118">-ClusterObject</span></span>
<span data-ttu-id="68802-119">Obiekt klastra</span><span class="sxs-lookup"><span data-stu-id="68802-119">The cluster object</span></span>

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

### <span data-ttu-id="68802-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68802-120">-DefaultProfile</span></span>
<span data-ttu-id="68802-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68802-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68802-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="68802-122">-EnableAutoScaling</span></span>
<span data-ttu-id="68802-123">Czy włączyć funkcję automatycznej skalowania</span><span class="sxs-lookup"><span data-stu-id="68802-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="68802-124">-Force</span><span class="sxs-lookup"><span data-stu-id="68802-124">-Force</span></span>
<span data-ttu-id="68802-125">Aktualizowanie puli węzłów bez monitowania</span><span class="sxs-lookup"><span data-stu-id="68802-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="68802-126">-ID</span><span class="sxs-lookup"><span data-stu-id="68802-126">-Id</span></span>
<span data-ttu-id="68802-127">Identyfikator puli węzłów w klastrze zarządzanych Kubernetes</span><span class="sxs-lookup"><span data-stu-id="68802-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="68802-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68802-128">-InputObject</span></span>
<span data-ttu-id="68802-129">Obiekt PSAgentPool, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="68802-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="68802-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="68802-130">-KubernetesVersion</span></span>
<span data-ttu-id="68802-131">Wersja programu Kubernetes używana do tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="68802-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="68802-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="68802-132">-MaxCount</span></span>
<span data-ttu-id="68802-133">Maksymalna liczba węzłów do automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="68802-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="68802-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="68802-134">-MinCount</span></span>
<span data-ttu-id="68802-135">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="68802-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="68802-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68802-136">-Name</span></span>
<span data-ttu-id="68802-137">Nazwa puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="68802-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="68802-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68802-138">-ResourceGroupName</span></span>
<span data-ttu-id="68802-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68802-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="68802-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68802-140">-Confirm</span></span>
<span data-ttu-id="68802-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68802-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68802-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68802-142">-WhatIf</span></span>
<span data-ttu-id="68802-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68802-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68802-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68802-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68802-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68802-145">CommonParameters</span></span>
<span data-ttu-id="68802-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68802-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68802-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68802-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68802-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68802-148">INPUTS</span></span>

### <span data-ttu-id="68802-149">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="68802-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="68802-150">System. String</span><span class="sxs-lookup"><span data-stu-id="68802-150">System.String</span></span>

## <span data-ttu-id="68802-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68802-151">OUTPUTS</span></span>

### <span data-ttu-id="68802-152">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="68802-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="68802-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68802-153">NOTES</span></span>

## <span data-ttu-id="68802-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68802-154">RELATED LINKS</span></span>
