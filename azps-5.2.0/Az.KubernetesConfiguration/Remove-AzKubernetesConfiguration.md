---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361650"
---
# <span data-ttu-id="e25ef-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="e25ef-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="e25ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e25ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e25ef-103">Spowoduje to usunięcie pliku YAML użytego do skonfigurowania konfiguracji kontroli źródła, co powoduje zatrzymanie przyszłej synchronizacji z repozytorium źródłowego.</span><span class="sxs-lookup"><span data-stu-id="e25ef-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="e25ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e25ef-104">SYNTAX</span></span>

### <span data-ttu-id="e25ef-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e25ef-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e25ef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e25ef-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e25ef-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e25ef-107">DESCRIPTION</span></span>
<span data-ttu-id="e25ef-108">Spowoduje to usunięcie pliku YAML użytego do skonfigurowania konfiguracji kontroli źródła, co powoduje zatrzymanie przyszłej synchronizacji z repozytorium źródłowego.</span><span class="sxs-lookup"><span data-stu-id="e25ef-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="e25ef-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e25ef-109">EXAMPLES</span></span>

### <span data-ttu-id="e25ef-110">Przykład 1: usuwanie configuation Kubernetes klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="e25ef-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="e25ef-111">To polecenie usuwa configuation klastra Kubernetes według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e25ef-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="e25ef-112">Przykład 2: usuwanie configuation Kubernetes klastra według obiektu</span><span class="sxs-lookup"><span data-stu-id="e25ef-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="e25ef-113">To polecenie usuwa configuation klastra Kubernetes według obiektu.</span><span class="sxs-lookup"><span data-stu-id="e25ef-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="e25ef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e25ef-114">PARAMETERS</span></span>

### <span data-ttu-id="e25ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e25ef-115">-AsJob</span></span>
<span data-ttu-id="e25ef-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e25ef-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e25ef-117">-ClusterName</span></span>
<span data-ttu-id="e25ef-118">Nazwa klastra usługi Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e25ef-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-119">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="e25ef-119">-ClusterType</span></span>
<span data-ttu-id="e25ef-120">Nazwa zasobu klastra Kubernetes-managedClusters (dla klastrów AKS) lub connectedClusters (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="e25ef-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25ef-121">-DefaultProfile</span></span>
<span data-ttu-id="e25ef-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e25ef-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e25ef-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e25ef-123">-InputObject</span></span>
<span data-ttu-id="e25ef-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e25ef-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e25ef-125">-Name</span></span>
<span data-ttu-id="e25ef-126">Nazwa konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="e25ef-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e25ef-127">-NoWait</span></span>
<span data-ttu-id="e25ef-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e25ef-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e25ef-129">-PassThru</span></span>
<span data-ttu-id="e25ef-130">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e25ef-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25ef-131">-ResourceGroupName</span></span>
<span data-ttu-id="e25ef-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e25ef-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e25ef-133">-SubscriptionId</span></span>
<span data-ttu-id="e25ef-134">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e25ef-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25ef-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e25ef-135">-Confirm</span></span>
<span data-ttu-id="e25ef-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25ef-137">-WhatIf</span></span>
<span data-ttu-id="e25ef-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25ef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25ef-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e25ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25ef-140">CommonParameters</span></span>
<span data-ttu-id="e25ef-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25ef-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e25ef-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25ef-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e25ef-143">INPUTS</span></span>

### <span data-ttu-id="e25ef-144">Microsoft. Azure. PowerShell. polecenia. KubernetesConfiguration. models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="e25ef-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="e25ef-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e25ef-145">OUTPUTS</span></span>

### <span data-ttu-id="e25ef-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e25ef-146">System.Boolean</span></span>

## <span data-ttu-id="e25ef-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e25ef-147">NOTES</span></span>

<span data-ttu-id="e25ef-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e25ef-148">ALIASES</span></span>

<span data-ttu-id="e25ef-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e25ef-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e25ef-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e25ef-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e25ef-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e25ef-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e25ef-152">INPUTobject <IKubernetesConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e25ef-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e25ef-153">`[ClusterName <String>]`: Nazwa klastra usługi Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e25ef-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="e25ef-154">`[ClusterResourceName <String>]`: Nazwa zasobu klastra usługi Kubernetes — albo managedClusters (dla klastrów AKS) lub connectedClusters (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="e25ef-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="e25ef-155">`[ClusterRp <String>]`: Kubernetes Cluster RP-albo Microsoft. ContainerService (dla AKS klastrów) lub Microsoft. Kubernetes (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="e25ef-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="e25ef-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e25ef-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e25ef-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e25ef-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e25ef-158">`[SourceControlConfigurationName <String>]`: Nazwa konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="e25ef-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="e25ef-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e25ef-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="e25ef-160">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="e25ef-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="e25ef-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e25ef-161">RELATED LINKS</span></span>

