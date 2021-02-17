---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 425a2f2fcc145b360ea981a4d78113d6053c90e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185339"
---
# <span data-ttu-id="4706a-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="4706a-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="4706a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4706a-102">SYNOPSIS</span></span>
<span data-ttu-id="4706a-103">Utwórz nową konfigurację sterowania źródłem w programie Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4706a-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="4706a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4706a-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4706a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4706a-105">DESCRIPTION</span></span>
<span data-ttu-id="4706a-106">Utwórz nową konfigurację sterowania źródłem w programie Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4706a-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="4706a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4706a-107">EXAMPLES</span></span>

### <span data-ttu-id="4706a-108">Przykład 1. Tworzenie konfiguracji dla klastrów kubernetes</span><span class="sxs-lookup"><span data-stu-id="4706a-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="4706a-109">To polecenie tworzy konfigurację klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4706a-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="4706a-110">Przykład 1. Tworzenie konfiguracji dla klastrów kubernetes z określeniem operatorNamespace parametru</span><span class="sxs-lookup"><span data-stu-id="4706a-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="4706a-111">To polecenie tworzy konfigurację w przestrzeni nazw nowego operatora dla klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4706a-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="4706a-112">Uwaga: Nie można utworzyć konfiguracji w istniejącej przestrzeni nazw operatora.</span><span class="sxs-lookup"><span data-stu-id="4706a-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="4706a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4706a-113">PARAMETERS</span></span>

### <span data-ttu-id="4706a-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4706a-114">-ClusterName</span></span>
<span data-ttu-id="4706a-115">Nazwa klastru kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4706a-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="4706a-116">- ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="4706a-116">-ClusterScoped</span></span>
<span data-ttu-id="4706a-117">Jeśli zakres konfiguracji został ustawiony na klaster (wartością domyślną jest nameSpace).</span><span class="sxs-lookup"><span data-stu-id="4706a-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="4706a-118">- ClusterType</span><span class="sxs-lookup"><span data-stu-id="4706a-118">-ClusterType</span></span>
<span data-ttu-id="4706a-119">Nazwa zasobu klastrów Kubernetes — zarządzaneClusters (dla klastrów AKS) lub połączone klastry (dla klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="4706a-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="4706a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4706a-120">-DefaultProfile</span></span>
<span data-ttu-id="4706a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4706a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4706a-122">-EnableOpermOperator</span><span class="sxs-lookup"><span data-stu-id="4706a-122">-EnableHelmOperator</span></span>
<span data-ttu-id="4706a-123">Opcja włączenia operatora Helm dla tej konfiguracji git.</span><span class="sxs-lookup"><span data-stu-id="4706a-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="4706a-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="4706a-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="4706a-125">Wartości zastępują operator wykresu Helm.</span><span class="sxs-lookup"><span data-stu-id="4706a-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="4706a-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="4706a-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="4706a-127">Wersja wykresu operatorowego Helm.</span><span class="sxs-lookup"><span data-stu-id="4706a-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="4706a-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4706a-128">-Name</span></span>
<span data-ttu-id="4706a-129">Nazwa konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="4706a-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4706a-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="4706a-130">-OperatorInstanceName</span></span>
<span data-ttu-id="4706a-131">Nazwa wystąpienia operatora — identyfikująca konkretną konfigurację.</span><span class="sxs-lookup"><span data-stu-id="4706a-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="4706a-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="4706a-132">-OperatorNamespace</span></span>
<span data-ttu-id="4706a-133">Przestrzeń nazw, do której jest instalowany ten operator.</span><span class="sxs-lookup"><span data-stu-id="4706a-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="4706a-134">Maksymalnie 253 małe litery alfanumeryczne, łącznik i przekłoń.</span><span class="sxs-lookup"><span data-stu-id="4706a-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="4706a-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="4706a-135">-OperatorParameters</span></span>
<span data-ttu-id="4706a-136">Wszystkie parametry wystąpienia operatora w formacie ciągu.</span><span class="sxs-lookup"><span data-stu-id="4706a-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="4706a-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="4706a-137">-RepositoryUrl</span></span>
<span data-ttu-id="4706a-138">Adres URL repozytorium sourcecontrol.</span><span class="sxs-lookup"><span data-stu-id="4706a-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="4706a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4706a-139">-ResourceGroupName</span></span>
<span data-ttu-id="4706a-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4706a-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="4706a-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4706a-141">-SubscriptionId</span></span>
<span data-ttu-id="4706a-142">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4706a-142">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="4706a-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4706a-143">-Confirm</span></span>
<span data-ttu-id="4706a-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4706a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4706a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4706a-145">-WhatIf</span></span>
<span data-ttu-id="4706a-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4706a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4706a-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4706a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4706a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4706a-148">CommonParameters</span></span>
<span data-ttu-id="4706a-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4706a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4706a-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4706a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4706a-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4706a-151">INPUTS</span></span>

## <span data-ttu-id="4706a-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4706a-152">OUTPUTS</span></span>

### <span data-ttu-id="4706a-153">Microsoft.Azure.PowerShell.Cmdlet.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4706a-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="4706a-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4706a-154">NOTES</span></span>

<span data-ttu-id="4706a-155">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4706a-155">ALIASES</span></span>

## <span data-ttu-id="4706a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4706a-156">RELATED LINKS</span></span>

