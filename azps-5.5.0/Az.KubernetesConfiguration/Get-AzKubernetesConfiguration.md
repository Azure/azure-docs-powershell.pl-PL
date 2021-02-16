---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: daa058d1f3cc13e073d8533403341dad3db7c319
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185347"
---
# <span data-ttu-id="784e2-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="784e2-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="784e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="784e2-102">SYNOPSIS</span></span>
<span data-ttu-id="784e2-103">Pobiera szczegółowe informacje o konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="784e2-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="784e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="784e2-104">SYNTAX</span></span>

### <span data-ttu-id="784e2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="784e2-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="784e2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="784e2-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="784e2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="784e2-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="784e2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="784e2-108">DESCRIPTION</span></span>
<span data-ttu-id="784e2-109">Pobiera szczegółowe informacje o konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="784e2-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="784e2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="784e2-110">EXAMPLES</span></span>

### <span data-ttu-id="784e2-111">Przykład 1. Uzyskiwanie wszystkich konfiguracji klastrów kubernetes</span><span class="sxs-lookup"><span data-stu-id="784e2-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="784e2-112">To polecenie pobiera wszystkie konfiguracje klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="784e2-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="784e2-113">Przykład 2. Uzyskiwanie konfiguracji klastrów kubernetes według nazw</span><span class="sxs-lookup"><span data-stu-id="784e2-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="784e2-114">To polecenie pobiera konfigurację klastrów kubernetes według nazw.</span><span class="sxs-lookup"><span data-stu-id="784e2-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="784e2-115">Przykład 3. Uzyskiwanie konfiguracji klastrów kubernetes według obiektów</span><span class="sxs-lookup"><span data-stu-id="784e2-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="784e2-116">To polecenie pobiera konfigurację klastrów kubernetes według obiektów.</span><span class="sxs-lookup"><span data-stu-id="784e2-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="784e2-117">Przykład 4. Uzyskiwanie konfiguracji klastrów kubernetes według potoków</span><span class="sxs-lookup"><span data-stu-id="784e2-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="784e2-118">To polecenie pobiera konfigurację klastrów kubernetes według potoków.</span><span class="sxs-lookup"><span data-stu-id="784e2-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="784e2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="784e2-119">PARAMETERS</span></span>

### <span data-ttu-id="784e2-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="784e2-120">-ClusterName</span></span>
<span data-ttu-id="784e2-121">Nazwa klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="784e2-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="784e2-122">- ClusterRp</span><span class="sxs-lookup"><span data-stu-id="784e2-122">-ClusterRp</span></span>
<span data-ttu-id="784e2-123">Klaster Kubernetes : USŁUGA MICROSOFT.ContainerService (dla klastrów AKS) lub Microsoft.Kubernetes (w przypadku klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="784e2-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="784e2-124">- ClusterType</span><span class="sxs-lookup"><span data-stu-id="784e2-124">-ClusterType</span></span>
<span data-ttu-id="784e2-125">Nazwa zasobu klastrów Kubernetes — zarządzaneClusters (dla klastrów AKS) lub połączone klastry (dla klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="784e2-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="784e2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784e2-126">-DefaultProfile</span></span>
<span data-ttu-id="784e2-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="784e2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784e2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784e2-128">-InputObject</span></span>
<span data-ttu-id="784e2-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="784e2-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="784e2-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="784e2-130">-Name</span></span>
<span data-ttu-id="784e2-131">Nazwa konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="784e2-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="784e2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784e2-132">-ResourceGroupName</span></span>
<span data-ttu-id="784e2-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="784e2-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="784e2-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="784e2-134">-SubscriptionId</span></span>
<span data-ttu-id="784e2-135">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="784e2-135">The Azure subscription ID.</span></span>
<span data-ttu-id="784e2-136">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="784e2-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="784e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784e2-137">CommonParameters</span></span>
<span data-ttu-id="784e2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="784e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784e2-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="784e2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784e2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="784e2-140">INPUTS</span></span>

### <span data-ttu-id="784e2-141">Microsoft.Azure.PowerShell.Cmdlet.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="784e2-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="784e2-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="784e2-142">OUTPUTS</span></span>

### <span data-ttu-id="784e2-143">Microsoft.Azure.PowerShell.Cmdlet.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="784e2-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="784e2-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="784e2-144">NOTES</span></span>

<span data-ttu-id="784e2-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="784e2-145">ALIASES</span></span>

<span data-ttu-id="784e2-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="784e2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="784e2-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="784e2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="784e2-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="784e2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="784e2-149">INPUTOBJECT: <IKubernetesConfigurationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="784e2-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="784e2-150">`[ClusterName <String>]`: nazwa klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="784e2-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="784e2-151">`[ClusterResourceName <String>]`: Nazwa zasobu klastrów Kubernetes — zarządzaneClusters (dla klastrów AKS) lub połączone klastry (dla klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="784e2-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="784e2-152">`[ClusterRp <String>]`: Klaster Kubernetes , WIERSZ — Microsoft.ContainerService (dla klastrów AKS) lub Microsoft.Kubernetes (w przypadku klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="784e2-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="784e2-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="784e2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="784e2-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="784e2-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="784e2-155">`[SourceControlConfigurationName <String>]`: nazwa konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="784e2-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="784e2-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="784e2-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="784e2-157">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="784e2-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="784e2-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="784e2-158">RELATED LINKS</span></span>

