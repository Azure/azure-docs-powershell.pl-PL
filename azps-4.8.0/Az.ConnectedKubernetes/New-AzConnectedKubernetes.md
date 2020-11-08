---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064247"
---
# <span data-ttu-id="2e996-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="2e996-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="2e996-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e996-102">SYNOPSIS</span></span>
<span data-ttu-id="2e996-103">Interfejs API umożliwiający zarejestrowanie nowego klastra K8s i w związku z tym utworzenie prześledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="2e996-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="2e996-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e996-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e996-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e996-105">DESCRIPTION</span></span>
<span data-ttu-id="2e996-106">Interfejs API umożliwiający zarejestrowanie nowego klastra K8s i w związku z tym utworzenie prześledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="2e996-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="2e996-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e996-107">EXAMPLES</span></span>

### <span data-ttu-id="2e996-108">Przykład 1. Tworzenie połączonego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="2e996-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="2e996-109">To polecenie tworzy połączony Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2e996-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="2e996-110">Przykład 1. Utwórz połączony Kubernetes z parametrami kubeConfig i kubeContext</span><span class="sxs-lookup"><span data-stu-id="2e996-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="2e996-111">To polecenie tworzy połączony Kubernetes z parametrami kubeConfig i kubeContext.</span><span class="sxs-lookup"><span data-stu-id="2e996-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="2e996-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e996-112">PARAMETERS</span></span>

### <span data-ttu-id="2e996-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2e996-113">-ClusterName</span></span>
<span data-ttu-id="2e996-114">Nazwa klastra usługi Kubernetes, na którym jest wywoływana pozycja get.</span><span class="sxs-lookup"><span data-stu-id="2e996-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="2e996-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e996-115">-DefaultProfile</span></span>
<span data-ttu-id="2e996-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e996-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e996-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="2e996-117">-KubeConfig</span></span>
<span data-ttu-id="2e996-118">Ścieżka do pliku konfiguracji Kube</span><span class="sxs-lookup"><span data-stu-id="2e996-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="2e996-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="2e996-119">-KubeContext</span></span>
<span data-ttu-id="2e996-120">Kubconfig kontekst na bieżącym komputerze</span><span class="sxs-lookup"><span data-stu-id="2e996-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="2e996-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e996-121">-Location</span></span>
<span data-ttu-id="2e996-122">Lokalizacja klastra</span><span class="sxs-lookup"><span data-stu-id="2e996-122">Location of the cluster</span></span>

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

### <span data-ttu-id="2e996-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e996-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e996-124">Nazwa grupy zasobów, do której jest zarejestrowany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2e996-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="2e996-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e996-125">-SubscriptionId</span></span>
<span data-ttu-id="2e996-126">Identyfikator subskrypcji, do której jest zarejestrowany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2e996-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="2e996-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e996-127">-Confirm</span></span>
<span data-ttu-id="2e996-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e996-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e996-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e996-129">-WhatIf</span></span>
<span data-ttu-id="2e996-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e996-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e996-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e996-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e996-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e996-132">CommonParameters</span></span>
<span data-ttu-id="2e996-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e996-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e996-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e996-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e996-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e996-135">INPUTS</span></span>

## <span data-ttu-id="2e996-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e996-136">OUTPUTS</span></span>

### <span data-ttu-id="2e996-137">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="2e996-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="2e996-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e996-138">NOTES</span></span>

<span data-ttu-id="2e996-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2e996-139">ALIASES</span></span>

## <span data-ttu-id="2e996-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e996-140">RELATED LINKS</span></span>

