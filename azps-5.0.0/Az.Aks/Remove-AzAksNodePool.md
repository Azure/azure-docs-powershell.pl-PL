---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231576"
---
# <span data-ttu-id="344cd-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="344cd-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="344cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="344cd-102">SYNOPSIS</span></span>
<span data-ttu-id="344cd-103">Usuwanie puli węzłów z zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="344cd-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="344cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="344cd-104">SYNTAX</span></span>

### <span data-ttu-id="344cd-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="344cd-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344cd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="344cd-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344cd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="344cd-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344cd-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="344cd-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="344cd-109">Opis</span><span class="sxs-lookup"><span data-stu-id="344cd-109">DESCRIPTION</span></span>
<span data-ttu-id="344cd-110">Usuwanie puli węzłów z zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="344cd-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="344cd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="344cd-111">EXAMPLES</span></span>

### <span data-ttu-id="344cd-112">Usuwanie określonej puli węzłów</span><span class="sxs-lookup"><span data-stu-id="344cd-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="344cd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="344cd-113">PARAMETERS</span></span>

### <span data-ttu-id="344cd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="344cd-114">-AsJob</span></span>
<span data-ttu-id="344cd-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="344cd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="344cd-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="344cd-116">-ClusterName</span></span>
<span data-ttu-id="344cd-117">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="344cd-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="344cd-118">-ClusterObject</span></span>
<span data-ttu-id="344cd-119">Obiekt klastra.</span><span class="sxs-lookup"><span data-stu-id="344cd-119">The cluster object.</span></span>

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

### <span data-ttu-id="344cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344cd-120">-DefaultProfile</span></span>
<span data-ttu-id="344cd-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="344cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="344cd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="344cd-122">-Force</span></span>
<span data-ttu-id="344cd-123">Usuwanie puli węzłów bez monitu</span><span class="sxs-lookup"><span data-stu-id="344cd-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="344cd-124">-ID</span><span class="sxs-lookup"><span data-stu-id="344cd-124">-Id</span></span>
<span data-ttu-id="344cd-125">Identyfikator puli węzłów w klastrze zarządzanych Kubernetes</span><span class="sxs-lookup"><span data-stu-id="344cd-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="344cd-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="344cd-126">-InputObject</span></span>
<span data-ttu-id="344cd-127">Obiekt PSAgentPool, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="344cd-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="344cd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="344cd-128">-Name</span></span>
<span data-ttu-id="344cd-129">Nazwa puli węzłów</span><span class="sxs-lookup"><span data-stu-id="344cd-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="344cd-130">-PassThru</span></span>
<span data-ttu-id="344cd-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="344cd-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="344cd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="344cd-132">-ResourceGroupName</span></span>
<span data-ttu-id="344cd-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="344cd-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344cd-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="344cd-134">-Confirm</span></span>
<span data-ttu-id="344cd-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="344cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="344cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344cd-136">-WhatIf</span></span>
<span data-ttu-id="344cd-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="344cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344cd-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="344cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="344cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344cd-139">CommonParameters</span></span>
<span data-ttu-id="344cd-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="344cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344cd-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="344cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344cd-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="344cd-142">INPUTS</span></span>

### <span data-ttu-id="344cd-143">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="344cd-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="344cd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="344cd-144">System.String</span></span>

## <span data-ttu-id="344cd-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="344cd-145">OUTPUTS</span></span>

### <span data-ttu-id="344cd-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="344cd-146">System.Boolean</span></span>

## <span data-ttu-id="344cd-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="344cd-147">NOTES</span></span>

## <span data-ttu-id="344cd-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="344cd-148">RELATED LINKS</span></span>
