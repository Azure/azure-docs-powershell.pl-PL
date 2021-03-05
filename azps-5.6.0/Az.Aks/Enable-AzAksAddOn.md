---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 1280f65659f986d0fd8402da0d3db5b1c5a92b58
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966954"
---
# <span data-ttu-id="8c335-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="8c335-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="8c335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c335-102">SYNOPSIS</span></span>
<span data-ttu-id="8c335-103">Włącz dodatki dla dodatków.</span><span class="sxs-lookup"><span data-stu-id="8c335-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="8c335-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c335-104">SYNTAX</span></span>

### <span data-ttu-id="8c335-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8c335-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c335-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c335-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c335-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c335-107">DESCRIPTION</span></span>
<span data-ttu-id="8c335-108">Włącz dodatki dla dodatków.</span><span class="sxs-lookup"><span data-stu-id="8c335-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="8c335-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c335-109">EXAMPLES</span></span>

### <span data-ttu-id="8c335-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c335-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="8c335-111">Włącz dodatki `HttpApplicationRouting` `Monitoring` , `AzurePolicy` i `VirtualNode` dla `KubeDashboard` dodatków.</span><span class="sxs-lookup"><span data-stu-id="8c335-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="8c335-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c335-112">PARAMETERS</span></span>

### <span data-ttu-id="8c335-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8c335-113">-ClusterName</span></span>
<span data-ttu-id="8c335-114">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8c335-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="8c335-115">- ClusterObject</span><span class="sxs-lookup"><span data-stu-id="8c335-115">-ClusterObject</span></span>
<span data-ttu-id="8c335-116">Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="8c335-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="8c335-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c335-117">-DefaultProfile</span></span>
<span data-ttu-id="8c335-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c335-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c335-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c335-119">-Name</span></span>
<span data-ttu-id="8c335-120">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8c335-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c335-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c335-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c335-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c335-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c335-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8c335-123">-SubnetName</span></span>
<span data-ttu-id="8c335-124">Nazwa podsieci VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="8c335-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c335-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8c335-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="8c335-126">Identyfikator zasobu obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="8c335-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c335-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c335-127">-Confirm</span></span>
<span data-ttu-id="8c335-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c335-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c335-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c335-129">-WhatIf</span></span>
<span data-ttu-id="8c335-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c335-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c335-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c335-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c335-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c335-132">CommonParameters</span></span>
<span data-ttu-id="8c335-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c335-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c335-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c335-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c335-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c335-135">INPUTS</span></span>

### <span data-ttu-id="8c335-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8c335-136">System.String</span></span>

### <span data-ttu-id="8c335-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8c335-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="8c335-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c335-138">OUTPUTS</span></span>

### <span data-ttu-id="8c335-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8c335-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="8c335-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c335-140">NOTES</span></span>

## <span data-ttu-id="8c335-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c335-141">RELATED LINKS</span></span>
