---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222362"
---
# <span data-ttu-id="20e57-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="20e57-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="20e57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20e57-102">SYNOPSIS</span></span>
<span data-ttu-id="20e57-103">Zwraca właściwości określonego klastra połączonego, w tym nazwę, tożsamość, właściwości i dodatkowe szczegóły klastra.</span><span class="sxs-lookup"><span data-stu-id="20e57-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="20e57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20e57-104">SYNTAX</span></span>

### <span data-ttu-id="20e57-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20e57-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20e57-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="20e57-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20e57-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20e57-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="20e57-108">Lista</span><span class="sxs-lookup"><span data-stu-id="20e57-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="20e57-109">Opis</span><span class="sxs-lookup"><span data-stu-id="20e57-109">DESCRIPTION</span></span>
<span data-ttu-id="20e57-110">Zwraca właściwości określonego klastra połączonego, w tym nazwę, tożsamość, właściwości i dodatkowe szczegóły klastra.</span><span class="sxs-lookup"><span data-stu-id="20e57-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="20e57-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20e57-111">EXAMPLES</span></span>

### <span data-ttu-id="20e57-112">Przykład 1: uzyskiwanie wszystkich połączonych Kubernetes w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="20e57-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="20e57-113">To polecenie uzyskuje wszystkie połączone Kubernetes w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="20e57-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="20e57-114">Przykład 2: uzyskiwanie wszystkich połączonych Kubernetes w grupie zasób</span><span class="sxs-lookup"><span data-stu-id="20e57-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="20e57-115">To polecenie pobiera wszystkie połączone Kubernetes w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="20e57-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="20e57-116">Przykład 3: uzyskiwanie połączonego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="20e57-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="20e57-117">To polecenie uzyskuje połączony Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="20e57-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="20e57-118">Przykład 4: uzyskiwanie połączonego Kubernetes przez obiekt</span><span class="sxs-lookup"><span data-stu-id="20e57-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="20e57-119">To polecenie uzyskuje połączony Kubernetes przez obiekt.</span><span class="sxs-lookup"><span data-stu-id="20e57-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="20e57-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20e57-120">PARAMETERS</span></span>

### <span data-ttu-id="20e57-121">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="20e57-121">-ClusterName</span></span>
<span data-ttu-id="20e57-122">Nazwa klastra usługi Kubernetes, na którym jest wywoływana pozycja get.</span><span class="sxs-lookup"><span data-stu-id="20e57-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="20e57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e57-123">-DefaultProfile</span></span>
<span data-ttu-id="20e57-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20e57-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20e57-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20e57-125">-InputObject</span></span>
<span data-ttu-id="20e57-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="20e57-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20e57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e57-127">-ResourceGroupName</span></span>
<span data-ttu-id="20e57-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="20e57-128">The name of the resource group.</span></span>
<span data-ttu-id="20e57-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="20e57-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="20e57-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="20e57-130">-SubscriptionId</span></span>
<span data-ttu-id="20e57-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="20e57-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="20e57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e57-132">CommonParameters</span></span>
<span data-ttu-id="20e57-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e57-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20e57-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e57-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20e57-135">INPUTS</span></span>

### <span data-ttu-id="20e57-136">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="20e57-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="20e57-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20e57-137">OUTPUTS</span></span>

### <span data-ttu-id="20e57-138">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="20e57-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="20e57-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20e57-139">NOTES</span></span>

<span data-ttu-id="20e57-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="20e57-140">ALIASES</span></span>

<span data-ttu-id="20e57-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20e57-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20e57-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="20e57-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20e57-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20e57-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20e57-144">INPUTobject <IConnectedKubernetesIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="20e57-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20e57-145">`[ClusterName <String>]`: Nazwa klastra usługi Kubernetes, na którym jest wywoływana metoda get.</span><span class="sxs-lookup"><span data-stu-id="20e57-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="20e57-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="20e57-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20e57-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="20e57-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="20e57-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="20e57-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="20e57-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="20e57-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="20e57-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20e57-150">RELATED LINKS</span></span>

