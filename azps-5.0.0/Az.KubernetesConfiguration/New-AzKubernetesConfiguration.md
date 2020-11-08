---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234655"
---
# <span data-ttu-id="7dc15-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="7dc15-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="7dc15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dc15-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc15-103">Tworzenie nowej konfiguracji kontroli źródła Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7dc15-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="7dc15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dc15-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7dc15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7dc15-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc15-106">Tworzenie nowej konfiguracji kontroli źródła Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7dc15-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="7dc15-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dc15-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc15-108">Przykład 1: Tworzenie configuation dla Kubernetes klastra</span><span class="sxs-lookup"><span data-stu-id="7dc15-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="7dc15-109">To polecenie tworzy configuation dla Kubernetes klastra.</span><span class="sxs-lookup"><span data-stu-id="7dc15-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="7dc15-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dc15-110">PARAMETERS</span></span>

### <span data-ttu-id="7dc15-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="7dc15-111">-ClusterName</span></span>
<span data-ttu-id="7dc15-112">Nazwa klastra usługi Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7dc15-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="7dc15-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="7dc15-113">-ClusterScoped</span></span>
<span data-ttu-id="7dc15-114">Jeśli przekazano, Ustaw zakres konfiguracji na klaster (domyślnie jest to obszar nazw).</span><span class="sxs-lookup"><span data-stu-id="7dc15-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="7dc15-115">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="7dc15-115">-ClusterType</span></span>
<span data-ttu-id="7dc15-116">Nazwa zasobu klastra Kubernetes-managedClusters (dla klastrów AKS) lub connectedClusters (dla niektórymi K8S).</span><span class="sxs-lookup"><span data-stu-id="7dc15-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="7dc15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc15-117">-DefaultProfile</span></span>
<span data-ttu-id="7dc15-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dc15-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="7dc15-119">-EnableHelmOperator</span></span>
<span data-ttu-id="7dc15-120">Opcja umożliwiająca włączenie operatora Helm dla tej konfiguracji git.</span><span class="sxs-lookup"><span data-stu-id="7dc15-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="7dc15-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="7dc15-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="7dc15-122">Przesłonięcie wartości dla wykresu Helm dla operatorów.</span><span class="sxs-lookup"><span data-stu-id="7dc15-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="7dc15-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="7dc15-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="7dc15-124">Wersja wykresu Helm.</span><span class="sxs-lookup"><span data-stu-id="7dc15-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="7dc15-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7dc15-125">-Name</span></span>
<span data-ttu-id="7dc15-126">Nazwa konfiguracji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="7dc15-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="7dc15-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="7dc15-127">-OperatorInstanceName</span></span>
<span data-ttu-id="7dc15-128">Nazwa wystąpienia operatora — identyfikująca określoną konfigurację.</span><span class="sxs-lookup"><span data-stu-id="7dc15-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="7dc15-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="7dc15-129">-OperatorNamespace</span></span>
<span data-ttu-id="7dc15-130">Obszar nazw, do którego jest zainstalowany ten operator.</span><span class="sxs-lookup"><span data-stu-id="7dc15-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="7dc15-131">Maksymalnie 253 małych znaków alfanumerycznych, łączników i tylko okresów.</span><span class="sxs-lookup"><span data-stu-id="7dc15-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="7dc15-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="7dc15-132">-OperatorParameters</span></span>
<span data-ttu-id="7dc15-133">Wszystkie parametry wystąpienia operatora w formacie String.</span><span class="sxs-lookup"><span data-stu-id="7dc15-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="7dc15-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="7dc15-134">-RepositoryUrl</span></span>
<span data-ttu-id="7dc15-135">Adres URL repozytorium SourceControl.</span><span class="sxs-lookup"><span data-stu-id="7dc15-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="7dc15-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dc15-136">-ResourceGroupName</span></span>
<span data-ttu-id="7dc15-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7dc15-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="7dc15-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7dc15-138">-SubscriptionId</span></span>
<span data-ttu-id="7dc15-139">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc15-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="7dc15-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7dc15-140">-Confirm</span></span>
<span data-ttu-id="7dc15-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dc15-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dc15-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dc15-142">-WhatIf</span></span>
<span data-ttu-id="7dc15-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dc15-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dc15-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7dc15-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dc15-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc15-145">CommonParameters</span></span>
<span data-ttu-id="7dc15-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc15-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc15-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dc15-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc15-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dc15-148">INPUTS</span></span>

## <span data-ttu-id="7dc15-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dc15-149">OUTPUTS</span></span>

### <span data-ttu-id="7dc15-150">Microsoft. Azure. PowerShell. polecenia. KubernetesConfiguration. models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7dc15-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="7dc15-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dc15-151">NOTES</span></span>

<span data-ttu-id="7dc15-152">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7dc15-152">ALIASES</span></span>

## <span data-ttu-id="7dc15-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dc15-153">RELATED LINKS</span></span>

