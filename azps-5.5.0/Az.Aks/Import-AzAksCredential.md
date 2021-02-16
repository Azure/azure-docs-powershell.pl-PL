---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199858"
---
# <span data-ttu-id="f00f9-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="f00f9-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="f00f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f00f9-103">Importowanie i scalanie konfiguracji Kubectl dla zarządzanego klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f00f9-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="f00f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f00f9-104">SYNTAX</span></span>

### <span data-ttu-id="f00f9-105">GroupNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f00f9-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00f9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f00f9-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00f9-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f00f9-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00f9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f00f9-108">DESCRIPTION</span></span>
<span data-ttu-id="f00f9-109">Importowanie i scalanie konfiguracji Kubectl dla zarządzanego klastra Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f00f9-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="f00f9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f00f9-110">EXAMPLES</span></span>

### <span data-ttu-id="f00f9-111">Importowanie i scalanie konfiguracji Kubectl</span><span class="sxs-lookup"><span data-stu-id="f00f9-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f00f9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f00f9-112">PARAMETERS</span></span>

### <span data-ttu-id="f00f9-113">— Administrator</span><span class="sxs-lookup"><span data-stu-id="f00f9-113">-Admin</span></span>
<span data-ttu-id="f00f9-114">Pobierz konfigurację kubectl "clusterAdmin" zamiast domyślnego "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="f00f9-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="f00f9-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="f00f9-115">-ConfigPath</span></span>
<span data-ttu-id="f00f9-116">Plik konfiguracji programu Kubectl do utworzenia lub zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f00f9-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="f00f9-117">Zamiast tego należy użyć "-", aby wydrukować yaml jako stdout.</span><span class="sxs-lookup"><span data-stu-id="f00f9-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="f00f9-118">Domyślne: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="f00f9-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="f00f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00f9-119">-DefaultProfile</span></span>
<span data-ttu-id="f00f9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f00f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00f9-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f00f9-121">-Force</span></span>
<span data-ttu-id="f00f9-122">Importowanie konfiguracji Kubernetesa, nawet jeśli jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="f00f9-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="f00f9-123">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="f00f9-123">-Id</span></span>
<span data-ttu-id="f00f9-124">Identyfikator zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f00f9-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00f9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f00f9-125">-InputObject</span></span>
<span data-ttu-id="f00f9-126">Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="f00f9-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f00f9-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f00f9-127">-Name</span></span>
<span data-ttu-id="f00f9-128">Nazwa zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f00f9-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00f9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f00f9-129">-PassThru</span></span>
<span data-ttu-id="f00f9-130">Jeśli importowanie się powiedzie, zwraca wartość prawda.</span><span class="sxs-lookup"><span data-stu-id="f00f9-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="f00f9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00f9-131">-ResourceGroupName</span></span>
<span data-ttu-id="f00f9-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f00f9-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00f9-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f00f9-133">-Confirm</span></span>
<span data-ttu-id="f00f9-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f00f9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f00f9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00f9-135">-WhatIf</span></span>
<span data-ttu-id="f00f9-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f00f9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f00f9-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f00f9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f00f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00f9-138">CommonParameters</span></span>
<span data-ttu-id="f00f9-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00f9-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f00f9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00f9-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f00f9-141">INPUTS</span></span>

### <span data-ttu-id="f00f9-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f00f9-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="f00f9-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f00f9-143">System.String</span></span>

## <span data-ttu-id="f00f9-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f00f9-144">OUTPUTS</span></span>

### <span data-ttu-id="f00f9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f00f9-145">System.String</span></span>

## <span data-ttu-id="f00f9-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f00f9-146">NOTES</span></span>

## <span data-ttu-id="f00f9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f00f9-147">RELATED LINKS</span></span>
