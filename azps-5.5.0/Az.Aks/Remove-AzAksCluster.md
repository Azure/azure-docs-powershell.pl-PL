---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199835"
---
# <span data-ttu-id="3dee7-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="3dee7-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="3dee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dee7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dee7-103">Usuwanie zarządzanego klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="3dee7-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3dee7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3dee7-104">SYNTAX</span></span>

### <span data-ttu-id="3dee7-105">GroupNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3dee7-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dee7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dee7-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dee7-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dee7-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dee7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3dee7-108">DESCRIPTION</span></span>
<span data-ttu-id="3dee7-109">Usuwanie zarządzanego klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="3dee7-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3dee7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3dee7-110">EXAMPLES</span></span>

### <span data-ttu-id="3dee7-111">Usuwanie istniejącego zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="3dee7-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="3dee7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dee7-112">PARAMETERS</span></span>

### <span data-ttu-id="3dee7-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3dee7-113">-AsJob</span></span>
<span data-ttu-id="3dee7-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3dee7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dee7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dee7-115">-DefaultProfile</span></span>
<span data-ttu-id="3dee7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dee7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dee7-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3dee7-117">-Force</span></span>
<span data-ttu-id="3dee7-118">Usuwanie zarządzanego klastru Kubernetes bez monitu</span><span class="sxs-lookup"><span data-stu-id="3dee7-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="3dee7-119">— Id</span><span class="sxs-lookup"><span data-stu-id="3dee7-119">-Id</span></span>
<span data-ttu-id="3dee7-120">Identyfikator zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="3dee7-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="3dee7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dee7-121">-InputObject</span></span>
<span data-ttu-id="3dee7-122">Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="3dee7-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3dee7-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3dee7-123">-Name</span></span>
<span data-ttu-id="3dee7-124">Nazwa zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="3dee7-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="3dee7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dee7-125">-PassThru</span></span>
<span data-ttu-id="3dee7-126">Zwraca wartość True (Prawda), jeśli usunięcie się powiedzie</span><span class="sxs-lookup"><span data-stu-id="3dee7-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="3dee7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dee7-127">-ResourceGroupName</span></span>
<span data-ttu-id="3dee7-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3dee7-128">Resource group name</span></span>

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

### <span data-ttu-id="3dee7-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dee7-129">-Confirm</span></span>
<span data-ttu-id="3dee7-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3dee7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dee7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dee7-131">-WhatIf</span></span>
<span data-ttu-id="3dee7-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dee7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dee7-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3dee7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dee7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dee7-134">CommonParameters</span></span>
<span data-ttu-id="3dee7-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dee7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dee7-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dee7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dee7-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dee7-137">INPUTS</span></span>

### <span data-ttu-id="3dee7-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="3dee7-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="3dee7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3dee7-139">System.String</span></span>

## <span data-ttu-id="3dee7-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dee7-140">OUTPUTS</span></span>

### <span data-ttu-id="3dee7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3dee7-141">System.Boolean</span></span>

## <span data-ttu-id="3dee7-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3dee7-142">NOTES</span></span>

## <span data-ttu-id="3dee7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dee7-143">RELATED LINKS</span></span>
