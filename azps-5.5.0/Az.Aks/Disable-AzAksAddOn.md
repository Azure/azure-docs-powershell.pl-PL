---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 616695e60d945e545cfbb8c1b2fb7ba81ae9caa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190402"
---
# <span data-ttu-id="43efe-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="43efe-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="43efe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43efe-102">SYNOPSIS</span></span>
<span data-ttu-id="43efe-103">Wyłącz dodatki dla dodatków.</span><span class="sxs-lookup"><span data-stu-id="43efe-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="43efe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43efe-104">SYNTAX</span></span>

### <span data-ttu-id="43efe-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="43efe-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43efe-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43efe-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43efe-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="43efe-107">DESCRIPTION</span></span>
<span data-ttu-id="43efe-108">Wyłącz dodatki dla dodatków.</span><span class="sxs-lookup"><span data-stu-id="43efe-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="43efe-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43efe-109">EXAMPLES</span></span>

### <span data-ttu-id="43efe-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43efe-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="43efe-111">Wyłącz dodatki `HttpApplicationRouting` `Monitoring` oraz `AzurePolicy` `VirtualNode` `KubeDashboard` dodatki.</span><span class="sxs-lookup"><span data-stu-id="43efe-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="43efe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43efe-112">PARAMETERS</span></span>

### <span data-ttu-id="43efe-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="43efe-113">-ClusterName</span></span>
<span data-ttu-id="43efe-114">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="43efe-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="43efe-115">- ClusterObject</span><span class="sxs-lookup"><span data-stu-id="43efe-115">-ClusterObject</span></span>
<span data-ttu-id="43efe-116">Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="43efe-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="43efe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43efe-117">-DefaultProfile</span></span>
<span data-ttu-id="43efe-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43efe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43efe-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43efe-119">-Name</span></span>
<span data-ttu-id="43efe-120">Nazwa zarządzanego klastra przez użytkownika Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="43efe-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="43efe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43efe-121">-ResourceGroupName</span></span>
<span data-ttu-id="43efe-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43efe-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="43efe-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43efe-123">-Confirm</span></span>
<span data-ttu-id="43efe-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="43efe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43efe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43efe-125">-WhatIf</span></span>
<span data-ttu-id="43efe-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43efe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43efe-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="43efe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43efe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43efe-128">CommonParameters</span></span>
<span data-ttu-id="43efe-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43efe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43efe-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43efe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43efe-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43efe-131">INPUTS</span></span>

### <span data-ttu-id="43efe-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="43efe-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="43efe-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43efe-133">System.String</span></span>

## <span data-ttu-id="43efe-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43efe-134">OUTPUTS</span></span>

### <span data-ttu-id="43efe-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="43efe-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="43efe-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43efe-136">NOTES</span></span>

## <span data-ttu-id="43efe-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43efe-137">RELATED LINKS</span></span>
