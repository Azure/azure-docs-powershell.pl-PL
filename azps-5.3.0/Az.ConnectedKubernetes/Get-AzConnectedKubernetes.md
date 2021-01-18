---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503915"
---
# <span data-ttu-id="12434-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="12434-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="12434-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12434-102">SYNOPSIS</span></span>
<span data-ttu-id="12434-103">Zwraca właściwości określonego klastra połączonego, w tym nazwę, tożsamość, właściwości i dodatkowe szczegóły klastra.</span><span class="sxs-lookup"><span data-stu-id="12434-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="12434-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12434-104">SYNTAX</span></span>

### <span data-ttu-id="12434-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12434-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12434-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="12434-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12434-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12434-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="12434-108">Lista</span><span class="sxs-lookup"><span data-stu-id="12434-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="12434-109">Opis</span><span class="sxs-lookup"><span data-stu-id="12434-109">DESCRIPTION</span></span>
<span data-ttu-id="12434-110">Zwraca właściwości określonego klastra połączonego, w tym nazwę, tożsamość, właściwości i dodatkowe szczegóły klastra.</span><span class="sxs-lookup"><span data-stu-id="12434-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="12434-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12434-111">EXAMPLES</span></span>

### <span data-ttu-id="12434-112">Przykład 1: uzyskiwanie wszystkich połączonych Kubernetes w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="12434-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="12434-113">To polecenie uzyskuje wszystkie połączone Kubernetes w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12434-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="12434-114">Przykład 2: uzyskiwanie wszystkich połączonych Kubernetes w grupie zasób</span><span class="sxs-lookup"><span data-stu-id="12434-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="12434-115">To polecenie pobiera wszystkie połączone Kubernetes w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="12434-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="12434-116">Przykład 3: uzyskiwanie połączonego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="12434-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="12434-117">To polecenie uzyskuje połączony Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="12434-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="12434-118">Przykład 4: uzyskiwanie połączonego Kubernetes przez obiekt</span><span class="sxs-lookup"><span data-stu-id="12434-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="12434-119">To polecenie uzyskuje połączony Kubernetes przez obiekt.</span><span class="sxs-lookup"><span data-stu-id="12434-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="12434-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12434-120">PARAMETERS</span></span>

### <span data-ttu-id="12434-121">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="12434-121">-ClusterName</span></span>
<span data-ttu-id="12434-122">Nazwa klastra usługi Kubernetes, na którym jest wywoływana pozycja get.</span><span class="sxs-lookup"><span data-stu-id="12434-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="12434-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12434-123">-DefaultProfile</span></span>
<span data-ttu-id="12434-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12434-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12434-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12434-125">-InputObject</span></span>
<span data-ttu-id="12434-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="12434-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12434-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12434-127">-ResourceGroupName</span></span>
<span data-ttu-id="12434-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12434-128">The name of the resource group.</span></span>
<span data-ttu-id="12434-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="12434-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="12434-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12434-130">-SubscriptionId</span></span>
<span data-ttu-id="12434-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="12434-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="12434-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12434-132">CommonParameters</span></span>
<span data-ttu-id="12434-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12434-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12434-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12434-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12434-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12434-135">INPUTS</span></span>

### <span data-ttu-id="12434-136">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="12434-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="12434-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12434-137">OUTPUTS</span></span>

### <span data-ttu-id="12434-138">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="12434-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="12434-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12434-139">NOTES</span></span>

<span data-ttu-id="12434-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="12434-140">ALIASES</span></span>

<span data-ttu-id="12434-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12434-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12434-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="12434-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12434-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12434-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12434-144">INPUTobject <IConnectedKubernetesIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="12434-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12434-145">`[ClusterName <String>]`: Nazwa klastra usługi Kubernetes, na którym jest wywoływana metoda get.</span><span class="sxs-lookup"><span data-stu-id="12434-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="12434-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="12434-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12434-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12434-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="12434-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="12434-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="12434-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="12434-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="12434-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12434-150">RELATED LINKS</span></span>

