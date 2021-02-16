---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194939"
---
# <span data-ttu-id="fe78d-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="fe78d-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="fe78d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe78d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe78d-103">Interfejs API do rejestrowania nowego klastru K8s, a tym samym tworzenia śledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="fe78d-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="fe78d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe78d-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe78d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe78d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe78d-106">Interfejs API do rejestrowania nowego klastru K8s, a tym samym tworzenia śledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="fe78d-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="fe78d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe78d-107">EXAMPLES</span></span>

### <span data-ttu-id="fe78d-108">Przykład 1. Tworzenie połączonych sieci kubernetes</span><span class="sxs-lookup"><span data-stu-id="fe78d-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="fe78d-109">To polecenie tworzy połączone kubernety.</span><span class="sxs-lookup"><span data-stu-id="fe78d-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="fe78d-110">Przykład 1. Tworzenie połączonych kubernetes z parametrami kubeConfig i kubeContext</span><span class="sxs-lookup"><span data-stu-id="fe78d-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="fe78d-111">To polecenie tworzy połączone witryny kubernetes z parametrami kubeConfig i kubeContext.</span><span class="sxs-lookup"><span data-stu-id="fe78d-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="fe78d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe78d-112">PARAMETERS</span></span>

### <span data-ttu-id="fe78d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fe78d-113">-ClusterName</span></span>
<span data-ttu-id="fe78d-114">Nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="fe78d-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe78d-115">-DefaultProfile</span></span>
<span data-ttu-id="fe78d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe78d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78d-117">- KubeConfig</span><span class="sxs-lookup"><span data-stu-id="fe78d-117">-KubeConfig</span></span>
<span data-ttu-id="fe78d-118">Ścieżka do pliku konfiguracji kube</span><span class="sxs-lookup"><span data-stu-id="fe78d-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="fe78d-119">- KubeContext</span><span class="sxs-lookup"><span data-stu-id="fe78d-119">-KubeContext</span></span>
<span data-ttu-id="fe78d-120">Kontekst konfiguracji z bieżącego komputera</span><span class="sxs-lookup"><span data-stu-id="fe78d-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="fe78d-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fe78d-121">-Location</span></span>
<span data-ttu-id="fe78d-122">Lokalizacja klastra</span><span class="sxs-lookup"><span data-stu-id="fe78d-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe78d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe78d-124">Nazwa grupy zasobów, do której jest zarejestrowany klaster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fe78d-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78d-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe78d-125">-SubscriptionId</span></span>
<span data-ttu-id="fe78d-126">Identyfikator subskrypcji, do której jest zarejestrowany klaster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fe78d-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe78d-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe78d-127">-Confirm</span></span>
<span data-ttu-id="fe78d-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe78d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe78d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe78d-129">-WhatIf</span></span>
<span data-ttu-id="fe78d-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe78d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe78d-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fe78d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe78d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe78d-132">CommonParameters</span></span>
<span data-ttu-id="fe78d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe78d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe78d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe78d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe78d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe78d-135">INPUTS</span></span>

## <span data-ttu-id="fe78d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe78d-136">OUTPUTS</span></span>

### <span data-ttu-id="fe78d-137">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="fe78d-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="fe78d-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe78d-138">NOTES</span></span>

<span data-ttu-id="fe78d-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fe78d-139">ALIASES</span></span>

## <span data-ttu-id="fe78d-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe78d-140">RELATED LINKS</span></span>

