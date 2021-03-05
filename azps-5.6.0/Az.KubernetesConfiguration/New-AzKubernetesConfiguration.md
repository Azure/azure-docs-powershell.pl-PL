---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 0040ab3bc037527400ea1f3eabf3c887189fc73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976826"
---
# <span data-ttu-id="8c011-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c011-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="8c011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c011-102">SYNOPSIS</span></span>
<span data-ttu-id="8c011-103">Utwórz nową konfigurację kontrolki źródła Kubernetesa.</span><span class="sxs-lookup"><span data-stu-id="8c011-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="8c011-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c011-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c011-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c011-105">DESCRIPTION</span></span>
<span data-ttu-id="8c011-106">Utwórz nową konfigurację kontrolki źródła Kubernetesa.</span><span class="sxs-lookup"><span data-stu-id="8c011-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="8c011-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c011-107">EXAMPLES</span></span>

### <span data-ttu-id="8c011-108">Przykład 1. Tworzenie konfiguracji dla klastrów kubernetes</span><span class="sxs-lookup"><span data-stu-id="8c011-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="8c011-109">To polecenie tworzy konfigurację klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8c011-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="8c011-110">Przykład 1. Tworzenie konfiguracji dla klastrów kubernetes z określeniem operatorNamespace parametru</span><span class="sxs-lookup"><span data-stu-id="8c011-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="8c011-111">To polecenie tworzy konfigurację w przestrzeni nazw nowego operatora dla klastrów kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8c011-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="8c011-112">Uwaga: Nie można utworzyć konfiguracji w istniejącej przestrzeni nazw operatora.</span><span class="sxs-lookup"><span data-stu-id="8c011-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="8c011-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c011-113">PARAMETERS</span></span>

### <span data-ttu-id="8c011-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8c011-114">-ClusterName</span></span>
<span data-ttu-id="8c011-115">Nazwa klastru kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8c011-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="8c011-116">- ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="8c011-116">-ClusterScoped</span></span>
<span data-ttu-id="8c011-117">Jeśli zakres konfiguracji został ustawiony na klaster (wartością domyślną jest nameSpace).</span><span class="sxs-lookup"><span data-stu-id="8c011-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="8c011-118">- ClusterType</span><span class="sxs-lookup"><span data-stu-id="8c011-118">-ClusterType</span></span>
<span data-ttu-id="8c011-119">Nazwa zasobu klastrów Kubernetes — zarządzaneClusters (dla klastrów AKS) lub połączone klastry (dla klastrów OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="8c011-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="8c011-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c011-120">-DefaultProfile</span></span>
<span data-ttu-id="8c011-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c011-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c011-122">-EnableOpermOperator</span><span class="sxs-lookup"><span data-stu-id="8c011-122">-EnableHelmOperator</span></span>
<span data-ttu-id="8c011-123">Opcja włączenia operatora Helm dla tej konfiguracji git.</span><span class="sxs-lookup"><span data-stu-id="8c011-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="8c011-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="8c011-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="8c011-125">Wartości są zastępują operator wykresu Helm.</span><span class="sxs-lookup"><span data-stu-id="8c011-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="8c011-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="8c011-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="8c011-127">Wersja wykresu operatorowego Helm.</span><span class="sxs-lookup"><span data-stu-id="8c011-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="8c011-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c011-128">-Name</span></span>
<span data-ttu-id="8c011-129">Nazwa konfiguracji kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="8c011-129">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="8c011-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="8c011-130">-OperatorInstanceName</span></span>
<span data-ttu-id="8c011-131">Nazwa wystąpienia operatora — identyfikująca konkretną konfigurację.</span><span class="sxs-lookup"><span data-stu-id="8c011-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="8c011-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="8c011-132">-OperatorNamespace</span></span>
<span data-ttu-id="8c011-133">Przestrzeń nazw, do której jest instalowany ten operator.</span><span class="sxs-lookup"><span data-stu-id="8c011-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="8c011-134">Maksymalnie 253 małe litery alfanumeryczne, łącznik i przec.</span><span class="sxs-lookup"><span data-stu-id="8c011-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="8c011-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="8c011-135">-OperatorParameters</span></span>
<span data-ttu-id="8c011-136">Wszystkie parametry wystąpienia operatora w formacie ciągu.</span><span class="sxs-lookup"><span data-stu-id="8c011-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="8c011-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="8c011-137">-RepositoryUrl</span></span>
<span data-ttu-id="8c011-138">Adres URL repozytorium sourcecontrol.</span><span class="sxs-lookup"><span data-stu-id="8c011-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="8c011-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c011-139">-ResourceGroupName</span></span>
<span data-ttu-id="8c011-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c011-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c011-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c011-141">-SubscriptionId</span></span>
<span data-ttu-id="8c011-142">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8c011-142">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="8c011-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c011-143">-Confirm</span></span>
<span data-ttu-id="8c011-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c011-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c011-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c011-145">-WhatIf</span></span>
<span data-ttu-id="8c011-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c011-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c011-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c011-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c011-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c011-148">CommonParameters</span></span>
<span data-ttu-id="8c011-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c011-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c011-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c011-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c011-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c011-151">INPUTS</span></span>

## <span data-ttu-id="8c011-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c011-152">OUTPUTS</span></span>

### <span data-ttu-id="8c011-153">Microsoft.Azure.PowerShell.Cmdlet.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c011-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="8c011-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c011-154">NOTES</span></span>

<span data-ttu-id="8c011-155">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8c011-155">ALIASES</span></span>

## <span data-ttu-id="8c011-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c011-156">RELATED LINKS</span></span>

