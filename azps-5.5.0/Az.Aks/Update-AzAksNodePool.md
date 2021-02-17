---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192635"
---
# <span data-ttu-id="25d10-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="25d10-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="25d10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d10-102">SYNOPSIS</span></span>
<span data-ttu-id="25d10-103">Zaktualizuj pulę węzła w klastrze zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="25d10-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="25d10-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25d10-104">SYNTAX</span></span>

### <span data-ttu-id="25d10-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="25d10-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d10-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d10-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d10-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d10-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d10-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d10-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25d10-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="25d10-109">DESCRIPTION</span></span>
<span data-ttu-id="25d10-110">Zaktualizuj pulę węzła w klastrze zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="25d10-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="25d10-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25d10-111">EXAMPLES</span></span>

### <span data-ttu-id="25d10-112">Zmienianie liczby minimunów na 5 dla określonej puli węzła</span><span class="sxs-lookup"><span data-stu-id="25d10-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="25d10-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25d10-113">PARAMETERS</span></span>

### <span data-ttu-id="25d10-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="25d10-114">-AsJob</span></span>
<span data-ttu-id="25d10-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="25d10-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25d10-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="25d10-116">-ClusterName</span></span>
<span data-ttu-id="25d10-117">Nazwa zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="25d10-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="25d10-118">- ClusterObject</span><span class="sxs-lookup"><span data-stu-id="25d10-118">-ClusterObject</span></span>
<span data-ttu-id="25d10-119">Obiekt klasterowy</span><span class="sxs-lookup"><span data-stu-id="25d10-119">The cluster object</span></span>

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

### <span data-ttu-id="25d10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d10-120">-DefaultProfile</span></span>
<span data-ttu-id="25d10-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25d10-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d10-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="25d10-122">-EnableAutoScaling</span></span>
<span data-ttu-id="25d10-123">Czy włączyć automatyczny skaler</span><span class="sxs-lookup"><span data-stu-id="25d10-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="25d10-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="25d10-124">-Force</span></span>
<span data-ttu-id="25d10-125">Aktualizowanie puli węzła bez monitu</span><span class="sxs-lookup"><span data-stu-id="25d10-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="25d10-126">— Id</span><span class="sxs-lookup"><span data-stu-id="25d10-126">-Id</span></span>
<span data-ttu-id="25d10-127">Identyfikator puli węzła w zarządzanym klastrze Kubernetes</span><span class="sxs-lookup"><span data-stu-id="25d10-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="25d10-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25d10-128">-InputObject</span></span>
<span data-ttu-id="25d10-129">Obiekt PSAgentPool, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="25d10-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="25d10-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="25d10-130">-KubernetesVersion</span></span>
<span data-ttu-id="25d10-131">Wersja programu Kubernetes do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="25d10-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="25d10-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="25d10-132">-MaxCount</span></span>
<span data-ttu-id="25d10-133">Maksymalna liczba węzłów na skalowanie automatyczne</span><span class="sxs-lookup"><span data-stu-id="25d10-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="25d10-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="25d10-134">-MinCount</span></span>
<span data-ttu-id="25d10-135">Minimalna liczba węzłów do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="25d10-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="25d10-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25d10-136">-Name</span></span>
<span data-ttu-id="25d10-137">Nazwa puli węzła.</span><span class="sxs-lookup"><span data-stu-id="25d10-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="25d10-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d10-138">-ResourceGroupName</span></span>
<span data-ttu-id="25d10-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25d10-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="25d10-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25d10-140">-Confirm</span></span>
<span data-ttu-id="25d10-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25d10-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d10-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d10-142">-WhatIf</span></span>
<span data-ttu-id="25d10-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d10-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d10-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="25d10-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d10-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d10-145">CommonParameters</span></span>
<span data-ttu-id="25d10-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d10-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d10-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25d10-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d10-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25d10-148">INPUTS</span></span>

### <span data-ttu-id="25d10-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="25d10-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="25d10-150">System.String</span><span class="sxs-lookup"><span data-stu-id="25d10-150">System.String</span></span>

## <span data-ttu-id="25d10-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25d10-151">OUTPUTS</span></span>

### <span data-ttu-id="25d10-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="25d10-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="25d10-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25d10-153">NOTES</span></span>

## <span data-ttu-id="25d10-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25d10-154">RELATED LINKS</span></span>
