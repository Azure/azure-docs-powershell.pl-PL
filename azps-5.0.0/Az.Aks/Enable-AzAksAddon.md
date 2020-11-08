---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232368"
---
# <span data-ttu-id="ae280-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="ae280-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="ae280-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae280-102">SYNOPSIS</span></span>
<span data-ttu-id="ae280-103">Włącz Dodatki dla AKS.</span><span class="sxs-lookup"><span data-stu-id="ae280-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="ae280-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae280-104">SYNTAX</span></span>

### <span data-ttu-id="ae280-105">defaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae280-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae280-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae280-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae280-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae280-107">DESCRIPTION</span></span>
<span data-ttu-id="ae280-108">Włącz Dodatki dla AKS.</span><span class="sxs-lookup"><span data-stu-id="ae280-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="ae280-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae280-109">EXAMPLES</span></span>

### <span data-ttu-id="ae280-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae280-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="ae280-111">Włączanie dodatków,, `HttpApplicationRouting` `Monitoring` `AzurePolicy` `VirtualNode` i `KubeDashboard` dla AKS.</span><span class="sxs-lookup"><span data-stu-id="ae280-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="ae280-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae280-112">PARAMETERS</span></span>

### <span data-ttu-id="ae280-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ae280-113">-ClusterName</span></span>
<span data-ttu-id="ae280-114">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="ae280-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="ae280-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="ae280-115">-ClusterObject</span></span>
<span data-ttu-id="ae280-116">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="ae280-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ae280-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae280-117">-DefaultProfile</span></span>
<span data-ttu-id="ae280-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae280-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae280-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae280-119">-Name</span></span>
<span data-ttu-id="ae280-120">Kubernetes zarządzana Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="ae280-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="ae280-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae280-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae280-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae280-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae280-123">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="ae280-123">-SubnetName</span></span>
<span data-ttu-id="ae280-124">Nazwa podsieci VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="ae280-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="ae280-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ae280-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="ae280-126">Identyfikator zasobu obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="ae280-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="ae280-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae280-127">-Confirm</span></span>
<span data-ttu-id="ae280-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae280-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae280-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae280-129">-WhatIf</span></span>
<span data-ttu-id="ae280-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae280-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae280-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae280-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae280-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae280-132">CommonParameters</span></span>
<span data-ttu-id="ae280-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae280-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae280-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae280-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae280-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae280-135">INPUTS</span></span>

### <span data-ttu-id="ae280-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ae280-136">System.String</span></span>

### <span data-ttu-id="ae280-137">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ae280-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ae280-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae280-138">OUTPUTS</span></span>

### <span data-ttu-id="ae280-139">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ae280-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ae280-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae280-140">NOTES</span></span>

## <span data-ttu-id="ae280-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae280-141">RELATED LINKS</span></span>
