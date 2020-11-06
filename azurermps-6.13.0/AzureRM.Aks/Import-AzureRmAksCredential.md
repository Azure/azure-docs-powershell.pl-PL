---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: b65ac736be5ee5f2f0592bcb2fdc84c873361f9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549471"
---
# <span data-ttu-id="6aba8-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="6aba8-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="6aba8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aba8-102">SYNOPSIS</span></span>
<span data-ttu-id="6aba8-103">Importowanie i scalanie konfiguracji Kubectl dla Kubernetes zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="6aba8-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aba8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aba8-104">SYNTAX</span></span>

### <span data-ttu-id="6aba8-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6aba8-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aba8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aba8-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aba8-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aba8-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aba8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6aba8-108">DESCRIPTION</span></span>
<span data-ttu-id="6aba8-109">Importowanie i scalanie konfiguracji Kubectl dla Kubernetes zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="6aba8-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="6aba8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aba8-110">EXAMPLES</span></span>

### <span data-ttu-id="6aba8-111">Importowanie i scalanie konfiguracji Kubectl</span><span class="sxs-lookup"><span data-stu-id="6aba8-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="6aba8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aba8-112">PARAMETERS</span></span>

### <span data-ttu-id="6aba8-113">-Administrator</span><span class="sxs-lookup"><span data-stu-id="6aba8-113">-Admin</span></span>
<span data-ttu-id="6aba8-114">Pobierz clusterAdmin' kubectl zamiast domyślnego "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="6aba8-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="6aba8-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="6aba8-115">-ConfigPath</span></span>
<span data-ttu-id="6aba8-116">Plik konfiguracji kubectl do utworzenia lub zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="6aba8-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="6aba8-117">Zamiast tego użyj polecenia "-", aby wydrukować YAML na stdout.</span><span class="sxs-lookup"><span data-stu-id="6aba8-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="6aba8-118">Wartość domyślna:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="6aba8-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="6aba8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aba8-119">-DefaultProfile</span></span>
<span data-ttu-id="6aba8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aba8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aba8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6aba8-121">-Force</span></span>
<span data-ttu-id="6aba8-122">Importowanie pliku Kubernetes, nawet jeśli jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="6aba8-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="6aba8-123">-ID</span><span class="sxs-lookup"><span data-stu-id="6aba8-123">-Id</span></span>
<span data-ttu-id="6aba8-124">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6aba8-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6aba8-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6aba8-125">-InputObject</span></span>
<span data-ttu-id="6aba8-126">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6aba8-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6aba8-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6aba8-127">-Name</span></span>
<span data-ttu-id="6aba8-128">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="6aba8-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6aba8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aba8-129">-PassThru</span></span>
<span data-ttu-id="6aba8-130">Zwraca wartość PRAWDA, jeśli Importowanie kończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6aba8-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="6aba8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aba8-131">-ResourceGroupName</span></span>
<span data-ttu-id="6aba8-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6aba8-132">Resource group name</span></span>

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

### <span data-ttu-id="6aba8-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aba8-133">-Confirm</span></span>
<span data-ttu-id="6aba8-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aba8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aba8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aba8-135">-WhatIf</span></span>
<span data-ttu-id="6aba8-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aba8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aba8-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6aba8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aba8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aba8-138">CommonParameters</span></span>
<span data-ttu-id="6aba8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aba8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aba8-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aba8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aba8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aba8-141">INPUTS</span></span>

### <span data-ttu-id="6aba8-142">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6aba8-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="6aba8-143">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6aba8-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6aba8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6aba8-144">System.String</span></span>

## <span data-ttu-id="6aba8-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aba8-145">OUTPUTS</span></span>

### <span data-ttu-id="6aba8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6aba8-146">System.String</span></span>

## <span data-ttu-id="6aba8-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aba8-147">NOTES</span></span>

## <span data-ttu-id="6aba8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aba8-148">RELATED LINKS</span></span>
