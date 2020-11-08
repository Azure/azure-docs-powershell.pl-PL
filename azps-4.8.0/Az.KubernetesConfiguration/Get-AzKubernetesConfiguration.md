---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220834"
---
# <span data-ttu-id="78bfa-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="78bfa-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="78bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="78bfa-103">Pobiera szczegóły konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="78bfa-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="78bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78bfa-104">SYNTAX</span></span>

### <span data-ttu-id="78bfa-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="78bfa-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="78bfa-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="78bfa-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="78bfa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="78bfa-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="78bfa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="78bfa-108">DESCRIPTION</span></span>
<span data-ttu-id="78bfa-109">Pobiera szczegóły konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="78bfa-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="78bfa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78bfa-110">EXAMPLES</span></span>

### <span data-ttu-id="78bfa-111">Przykład 1: pobieranie wszystkich konfiguracji klastra usługi Kubernetes</span><span class="sxs-lookup"><span data-stu-id="78bfa-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="78bfa-112">To polecenie pobiera wszystkie konfiguracje klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="78bfa-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="78bfa-113">Przykład 2: Uzyskiwanie konfiguracji klastra usługi Kubernetes według nazwy</span><span class="sxs-lookup"><span data-stu-id="78bfa-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="78bfa-114">To polecenie pobiera konfigurację klastra usługi Kubernetes według nazwy.</span><span class="sxs-lookup"><span data-stu-id="78bfa-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="78bfa-115">Przykład 3: Uzyskiwanie konfiguracji Kubernetes klastra według obiektu</span><span class="sxs-lookup"><span data-stu-id="78bfa-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="78bfa-116">To polecenie pobiera konfigurację klastra Kubernetes przez obiekt.</span><span class="sxs-lookup"><span data-stu-id="78bfa-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="78bfa-117">Przykład 4: Uzyskiwanie konfiguracji klastra usługi Kubernetes według rurociągu</span><span class="sxs-lookup"><span data-stu-id="78bfa-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="78bfa-118">To polecenie pobiera konfigurację klastra Kubernetes według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="78bfa-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="78bfa-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78bfa-119">PARAMETERS</span></span>

### <span data-ttu-id="78bfa-120">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="78bfa-120">-ClusterName</span></span>
<span data-ttu-id="78bfa-121">Nazwa klastra usługi Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="78bfa-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="78bfa-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="78bfa-122">-ClusterRp</span></span>
<span data-ttu-id="78bfa-123">Kubernetes Cluster RP — Microsoft. ContainerService (dla AKS klastrów) lub Microsoft. Kubernetes (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="78bfa-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="78bfa-124">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="78bfa-124">-ClusterType</span></span>
<span data-ttu-id="78bfa-125">Nazwa zasobu klastra Kubernetes-managedClusters (dla klastrów AKS) lub connectedClusters (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="78bfa-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="78bfa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bfa-126">-DefaultProfile</span></span>
<span data-ttu-id="78bfa-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78bfa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78bfa-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78bfa-128">-InputObject</span></span>
<span data-ttu-id="78bfa-129">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="78bfa-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfa-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78bfa-130">-Name</span></span>
<span data-ttu-id="78bfa-131">Nazwa konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="78bfa-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bfa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78bfa-132">-ResourceGroupName</span></span>
<span data-ttu-id="78bfa-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78bfa-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="78bfa-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="78bfa-134">-SubscriptionId</span></span>
<span data-ttu-id="78bfa-135">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="78bfa-135">The Azure subscription ID.</span></span>
<span data-ttu-id="78bfa-136">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="78bfa-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bfa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bfa-137">CommonParameters</span></span>
<span data-ttu-id="78bfa-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78bfa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bfa-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78bfa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bfa-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78bfa-140">INPUTS</span></span>

### <span data-ttu-id="78bfa-141">Microsoft. Azure. PowerShell. polecenia. KubernetesConfiguration. models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="78bfa-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="78bfa-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78bfa-142">OUTPUTS</span></span>

### <span data-ttu-id="78bfa-143">Microsoft. Azure. PowerShell. polecenia. KubernetesConfiguration. models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="78bfa-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="78bfa-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78bfa-144">NOTES</span></span>

<span data-ttu-id="78bfa-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="78bfa-145">ALIASES</span></span>

<span data-ttu-id="78bfa-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78bfa-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78bfa-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="78bfa-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78bfa-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78bfa-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78bfa-149">INPUTobject <IKubernetesConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="78bfa-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78bfa-150">`[ClusterName <String>]`: Nazwa klastra usługi Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="78bfa-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="78bfa-151">`[ClusterResourceName <String>]`: Nazwa zasobu klastra usługi Kubernetes — albo managedClusters (dla klastrów AKS) lub connectedClusters (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="78bfa-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="78bfa-152">`[ClusterRp <String>]`: Kubernetes Cluster RP-albo Microsoft. ContainerService (dla AKS klastrów) lub Microsoft. Kubernetes (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="78bfa-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="78bfa-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="78bfa-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78bfa-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78bfa-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="78bfa-155">`[SourceControlConfigurationName <String>]`: Nazwa konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="78bfa-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="78bfa-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="78bfa-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="78bfa-157">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="78bfa-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="78bfa-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78bfa-158">RELATED LINKS</span></span>

