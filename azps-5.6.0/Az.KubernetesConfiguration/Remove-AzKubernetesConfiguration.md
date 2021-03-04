---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: a63a28d301b5b565a01bf1e3c22acba413ee779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964602"
---
# <span data-ttu-id="d6c29-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6c29-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="d6c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6c29-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c29-103">Spowoduje to usunięcie pliku YAML użytego do skonfigurowania konfiguracji kontrolki źródła, co spowoduje zatrzymanie przyszłej synchronizacji ze źródłowym obiektem ponownie.</span><span class="sxs-lookup"><span data-stu-id="d6c29-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="d6c29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6c29-104">SYNTAX</span></span>

### <span data-ttu-id="d6c29-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="d6c29-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6c29-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6c29-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6c29-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6c29-107">DESCRIPTION</span></span>
<span data-ttu-id="d6c29-108">Spowoduje to usunięcie pliku YAML użytego do skonfigurowania konfiguracji kontrolki źródła, co spowoduje zatrzymanie przyszłej synchronizacji ze źródłowym obiektem ponownie.</span><span class="sxs-lookup"><span data-stu-id="d6c29-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="d6c29-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6c29-109">EXAMPLES</span></span>

### <span data-ttu-id="d6c29-110">Przykład 1. Usuwanie konfiguracji klastrów kubernetes według nazw</span><span class="sxs-lookup"><span data-stu-id="d6c29-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="d6c29-111">To polecenie usuwa konfigurację klastrów kubernetes według nazw.</span><span class="sxs-lookup"><span data-stu-id="d6c29-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="d6c29-112">Przykład 2. Usuwanie konfiguracji klastrów kubernetes według obiektów</span><span class="sxs-lookup"><span data-stu-id="d6c29-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="d6c29-113">To polecenie usuwa konfigurację klastrów kubernetes według obiektów.</span><span class="sxs-lookup"><span data-stu-id="d6c29-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="d6c29-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6c29-114">PARAMETERS</span></span>

### <span data-ttu-id="d6c29-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d6c29-115">-AsJob</span></span>
<span data-ttu-id="d6c29-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d6c29-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d6c29-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d6c29-117">-ClusterName</span></span>
<span data-ttu-id="d6c29-118">Nazwa klastru kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d6c29-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="d6c29-119">- ClusterType</span><span class="sxs-lookup"><span data-stu-id="d6c29-119">-ClusterType</span></span>
<span data-ttu-id="d6c29-120">Nazwa zasobu klastrów Kubernetes — zarządzaneClusters (dla klastrów AKS) lub połączone klastry (dla klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="d6c29-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="d6c29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c29-121">-DefaultProfile</span></span>
<span data-ttu-id="d6c29-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c29-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6c29-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6c29-123">-InputObject</span></span>
<span data-ttu-id="d6c29-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d6c29-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6c29-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6c29-125">-Name</span></span>
<span data-ttu-id="d6c29-126">Nazwa konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="d6c29-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="d6c29-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d6c29-127">-NoWait</span></span>
<span data-ttu-id="d6c29-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d6c29-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d6c29-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6c29-129">-PassThru</span></span>
<span data-ttu-id="d6c29-130">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d6c29-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d6c29-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c29-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6c29-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6c29-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6c29-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6c29-133">-SubscriptionId</span></span>
<span data-ttu-id="d6c29-134">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c29-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d6c29-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6c29-135">-Confirm</span></span>
<span data-ttu-id="d6c29-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6c29-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c29-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c29-137">-WhatIf</span></span>
<span data-ttu-id="d6c29-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6c29-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6c29-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6c29-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c29-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c29-140">CommonParameters</span></span>
<span data-ttu-id="d6c29-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c29-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c29-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6c29-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c29-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6c29-143">INPUTS</span></span>

### <span data-ttu-id="d6c29-144">Microsoft.Azure.PowerShell.Cmdlet.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="d6c29-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="d6c29-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6c29-145">OUTPUTS</span></span>

### <span data-ttu-id="d6c29-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6c29-146">System.Boolean</span></span>

## <span data-ttu-id="d6c29-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6c29-147">NOTES</span></span>

<span data-ttu-id="d6c29-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d6c29-148">ALIASES</span></span>

<span data-ttu-id="d6c29-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6c29-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6c29-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d6c29-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6c29-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6c29-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6c29-152">INPUTOBJECT: <IKubernetesConfigurationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d6c29-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6c29-153">`[ClusterName <String>]`: nazwa klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d6c29-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="d6c29-154">`[ClusterResourceName <String>]`: Nazwa zasobu klastrów Kubernetes — zarządzaneClusters (dla klastrów AKS) lub połączone klastry (dla klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="d6c29-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="d6c29-155">`[ClusterRp <String>]`: Klaster Kubernetes , WIERSZ — microsoft.ContainerService (dla klastrów AKS) lub Microsoft.Kubernetes (w przypadku klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="d6c29-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="d6c29-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d6c29-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6c29-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6c29-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d6c29-158">`[SourceControlConfigurationName <String>]`: nazwa konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="d6c29-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="d6c29-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c29-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d6c29-160">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="d6c29-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d6c29-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6c29-161">RELATED LINKS</span></span>

