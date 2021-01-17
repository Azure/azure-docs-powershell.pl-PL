---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348013"
---
# <span data-ttu-id="03c7b-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="03c7b-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="03c7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="03c7b-103">Importowanie i scalanie konfiguracji Kubectl dla Kubernetes zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="03c7b-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="03c7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03c7b-104">SYNTAX</span></span>

### <span data-ttu-id="03c7b-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03c7b-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c7b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c7b-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c7b-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c7b-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c7b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03c7b-108">DESCRIPTION</span></span>
<span data-ttu-id="03c7b-109">Importowanie i scalanie konfiguracji Kubectl dla Kubernetes zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="03c7b-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="03c7b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03c7b-110">EXAMPLES</span></span>

### <span data-ttu-id="03c7b-111">Importowanie i scalanie konfiguracji Kubectl</span><span class="sxs-lookup"><span data-stu-id="03c7b-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="03c7b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03c7b-112">PARAMETERS</span></span>

### <span data-ttu-id="03c7b-113">-Administrator</span><span class="sxs-lookup"><span data-stu-id="03c7b-113">-Admin</span></span>
<span data-ttu-id="03c7b-114">Pobierz clusterAdmin' kubectl zamiast domyślnego "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="03c7b-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="03c7b-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="03c7b-115">-ConfigPath</span></span>
<span data-ttu-id="03c7b-116">Plik konfiguracji kubectl do utworzenia lub zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="03c7b-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="03c7b-117">Zamiast tego użyj polecenia "-", aby wydrukować YAML na stdout.</span><span class="sxs-lookup"><span data-stu-id="03c7b-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="03c7b-118">Wartość domyślna:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="03c7b-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="03c7b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c7b-119">-DefaultProfile</span></span>
<span data-ttu-id="03c7b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03c7b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c7b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="03c7b-121">-Force</span></span>
<span data-ttu-id="03c7b-122">Importowanie pliku Kubernetes, nawet jeśli jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="03c7b-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="03c7b-123">-ID</span><span class="sxs-lookup"><span data-stu-id="03c7b-123">-Id</span></span>
<span data-ttu-id="03c7b-124">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="03c7b-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="03c7b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03c7b-125">-InputObject</span></span>
<span data-ttu-id="03c7b-126">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="03c7b-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="03c7b-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03c7b-127">-Name</span></span>
<span data-ttu-id="03c7b-128">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="03c7b-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="03c7b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c7b-129">-PassThru</span></span>
<span data-ttu-id="03c7b-130">Zwraca wartość PRAWDA, jeśli Importowanie kończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="03c7b-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="03c7b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c7b-131">-ResourceGroupName</span></span>
<span data-ttu-id="03c7b-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="03c7b-132">Resource group name</span></span>

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

### <span data-ttu-id="03c7b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03c7b-133">-Confirm</span></span>
<span data-ttu-id="03c7b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c7b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c7b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c7b-135">-WhatIf</span></span>
<span data-ttu-id="03c7b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c7b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c7b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03c7b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c7b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c7b-138">CommonParameters</span></span>
<span data-ttu-id="03c7b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c7b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c7b-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03c7b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c7b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03c7b-141">INPUTS</span></span>

### <span data-ttu-id="03c7b-142">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="03c7b-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="03c7b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="03c7b-143">System.String</span></span>

## <span data-ttu-id="03c7b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03c7b-144">OUTPUTS</span></span>

### <span data-ttu-id="03c7b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="03c7b-145">System.String</span></span>

## <span data-ttu-id="03c7b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03c7b-146">NOTES</span></span>

## <span data-ttu-id="03c7b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03c7b-147">RELATED LINKS</span></span>
