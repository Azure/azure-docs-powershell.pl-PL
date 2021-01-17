---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342493"
---
# <span data-ttu-id="fa1ae-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="fa1ae-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="fa1ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fa1ae-103">Wyłącz Dodatki dla AKS.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="fa1ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa1ae-104">SYNTAX</span></span>

### <span data-ttu-id="fa1ae-105">defaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fa1ae-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa1ae-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa1ae-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa1ae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa1ae-107">DESCRIPTION</span></span>
<span data-ttu-id="fa1ae-108">Wyłącz Dodatki dla AKS.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="fa1ae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa1ae-109">EXAMPLES</span></span>

### <span data-ttu-id="fa1ae-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa1ae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="fa1ae-111">Wyłączanie dodatków,, `HttpApplicationRouting` `Monitoring` `AzurePolicy` `VirtualNode` i `KubeDashboard` dla AKS.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="fa1ae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa1ae-112">PARAMETERS</span></span>

### <span data-ttu-id="fa1ae-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="fa1ae-113">-ClusterName</span></span>
<span data-ttu-id="fa1ae-114">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="fa1ae-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="fa1ae-115">-ClusterObject</span></span>
<span data-ttu-id="fa1ae-116">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="fa1ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa1ae-117">-DefaultProfile</span></span>
<span data-ttu-id="fa1ae-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa1ae-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa1ae-119">-Name</span></span>
<span data-ttu-id="fa1ae-120">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="fa1ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa1ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="fa1ae-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa1ae-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa1ae-123">-Confirm</span></span>
<span data-ttu-id="fa1ae-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa1ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa1ae-125">-WhatIf</span></span>
<span data-ttu-id="fa1ae-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa1ae-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa1ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa1ae-128">CommonParameters</span></span>
<span data-ttu-id="fa1ae-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa1ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa1ae-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa1ae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa1ae-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa1ae-131">INPUTS</span></span>

### <span data-ttu-id="fa1ae-132">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fa1ae-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="fa1ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fa1ae-133">System.String</span></span>

## <span data-ttu-id="fa1ae-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa1ae-134">OUTPUTS</span></span>

### <span data-ttu-id="fa1ae-135">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fa1ae-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fa1ae-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa1ae-136">NOTES</span></span>

## <span data-ttu-id="fa1ae-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa1ae-137">RELATED LINKS</span></span>
