---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012529"
---
# <span data-ttu-id="16332-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="16332-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="16332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16332-102">SYNOPSIS</span></span>
<span data-ttu-id="16332-103">Zwraca właściwości określonego połączonego klastra, takie jak nazwa, tożsamość, właściwości i dodatkowe szczegóły klastrów.</span><span class="sxs-lookup"><span data-stu-id="16332-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="16332-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16332-104">SYNTAX</span></span>

### <span data-ttu-id="16332-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="16332-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16332-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="16332-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16332-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="16332-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="16332-108">Lista</span><span class="sxs-lookup"><span data-stu-id="16332-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="16332-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="16332-109">DESCRIPTION</span></span>
<span data-ttu-id="16332-110">Zwraca właściwości określonego połączonego klastra, takie jak nazwa, tożsamość, właściwości i dodatkowe szczegóły klastrów.</span><span class="sxs-lookup"><span data-stu-id="16332-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="16332-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16332-111">EXAMPLES</span></span>

### <span data-ttu-id="16332-112">Przykład 1. Uzyskiwanie wszystkich połączonych kubernetes w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="16332-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="16332-113">To polecenie pobiera wszystkie połączone sieci kubernetes w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="16332-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="16332-114">Przykład 2. Uzyskiwanie wszystkich połączonych kubernetes w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="16332-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="16332-115">To polecenie pobiera wszystkie połączone sieci kubernetes w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="16332-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="16332-116">Przykład 3. Uzyskiwanie połączonej sieci kubernetes</span><span class="sxs-lookup"><span data-stu-id="16332-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="16332-117">To polecenie pobiera połączone sieci kubernetes.</span><span class="sxs-lookup"><span data-stu-id="16332-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="16332-118">Przykład 4. Uzyskiwanie połączonych kubernetes według obiektów</span><span class="sxs-lookup"><span data-stu-id="16332-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="16332-119">To polecenie pobiera połączone kubernety według obiektów.</span><span class="sxs-lookup"><span data-stu-id="16332-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="16332-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16332-120">PARAMETERS</span></span>

### <span data-ttu-id="16332-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="16332-121">-ClusterName</span></span>
<span data-ttu-id="16332-122">Nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="16332-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16332-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16332-123">-DefaultProfile</span></span>
<span data-ttu-id="16332-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16332-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16332-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16332-125">-InputObject</span></span>
<span data-ttu-id="16332-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="16332-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16332-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16332-127">-ResourceGroupName</span></span>
<span data-ttu-id="16332-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16332-128">The name of the resource group.</span></span>
<span data-ttu-id="16332-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="16332-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16332-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16332-130">-SubscriptionId</span></span>
<span data-ttu-id="16332-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="16332-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16332-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16332-132">CommonParameters</span></span>
<span data-ttu-id="16332-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16332-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16332-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16332-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16332-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16332-135">INPUTS</span></span>

### <span data-ttu-id="16332-136">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="16332-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="16332-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16332-137">OUTPUTS</span></span>

### <span data-ttu-id="16332-138">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="16332-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="16332-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16332-139">NOTES</span></span>

<span data-ttu-id="16332-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="16332-140">ALIASES</span></span>

<span data-ttu-id="16332-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16332-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16332-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="16332-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16332-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16332-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16332-144">INPUTOBJECT: <IConnectedKubernetesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="16332-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16332-145">`[ClusterName <String>]`: nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="16332-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="16332-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="16332-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16332-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16332-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="16332-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="16332-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="16332-149">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="16332-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="16332-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16332-150">RELATED LINKS</span></span>

