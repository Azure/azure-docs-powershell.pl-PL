---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192651"
---
# <span data-ttu-id="2f4bf-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="2f4bf-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="2f4bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4bf-103">Usuń pulę węzła z zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="2f4bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f4bf-104">SYNTAX</span></span>

### <span data-ttu-id="2f4bf-105">GroupNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2f4bf-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f4bf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4bf-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f4bf-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4bf-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f4bf-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4bf-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4bf-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f4bf-109">DESCRIPTION</span></span>
<span data-ttu-id="2f4bf-110">Usuń pulę węzła z zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="2f4bf-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f4bf-111">EXAMPLES</span></span>

### <span data-ttu-id="2f4bf-112">Usuwanie określonej puli węzła</span><span class="sxs-lookup"><span data-stu-id="2f4bf-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="2f4bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f4bf-113">PARAMETERS</span></span>

### <span data-ttu-id="2f4bf-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2f4bf-114">-AsJob</span></span>
<span data-ttu-id="2f4bf-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2f4bf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f4bf-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2f4bf-116">-ClusterName</span></span>
<span data-ttu-id="2f4bf-117">Nazwa zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="2f4bf-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2f4bf-118">- ClusterObject</span><span class="sxs-lookup"><span data-stu-id="2f4bf-118">-ClusterObject</span></span>
<span data-ttu-id="2f4bf-119">Obiekt klasterowy.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-119">The cluster object.</span></span>

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

### <span data-ttu-id="2f4bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4bf-120">-DefaultProfile</span></span>
<span data-ttu-id="2f4bf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f4bf-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2f4bf-122">-Force</span></span>
<span data-ttu-id="2f4bf-123">Usuwanie puli węzła bez monitu</span><span class="sxs-lookup"><span data-stu-id="2f4bf-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="2f4bf-124">— Id</span><span class="sxs-lookup"><span data-stu-id="2f4bf-124">-Id</span></span>
<span data-ttu-id="2f4bf-125">Identyfikator puli węzła w zarządzanym klastrze Kubernetes</span><span class="sxs-lookup"><span data-stu-id="2f4bf-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2f4bf-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f4bf-126">-InputObject</span></span>
<span data-ttu-id="2f4bf-127">Obiekt PSAgentPool, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2f4bf-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2f4bf-128">-Name</span></span>
<span data-ttu-id="2f4bf-129">Nazwa puli węzła</span><span class="sxs-lookup"><span data-stu-id="2f4bf-129">Name of your node pool</span></span>

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

### <span data-ttu-id="2f4bf-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f4bf-130">-PassThru</span></span>
<span data-ttu-id="2f4bf-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2f4bf-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2f4bf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4bf-132">-ResourceGroupName</span></span>
<span data-ttu-id="2f4bf-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2f4bf-133">Resource group name</span></span>

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

### <span data-ttu-id="2f4bf-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f4bf-134">-Confirm</span></span>
<span data-ttu-id="2f4bf-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4bf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4bf-136">-WhatIf</span></span>
<span data-ttu-id="2f4bf-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4bf-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4bf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4bf-139">CommonParameters</span></span>
<span data-ttu-id="2f4bf-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4bf-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f4bf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4bf-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f4bf-142">INPUTS</span></span>

### <span data-ttu-id="2f4bf-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="2f4bf-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="2f4bf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2f4bf-144">System.String</span></span>

## <span data-ttu-id="2f4bf-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f4bf-145">OUTPUTS</span></span>

### <span data-ttu-id="2f4bf-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f4bf-146">System.Boolean</span></span>

## <span data-ttu-id="2f4bf-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f4bf-147">NOTES</span></span>

## <span data-ttu-id="2f4bf-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f4bf-148">RELATED LINKS</span></span>
