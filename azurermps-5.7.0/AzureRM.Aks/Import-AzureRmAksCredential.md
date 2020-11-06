---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: 9a95f6a6b299114c52e011c3a1abdc6fa8651c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525421"
---
# <span data-ttu-id="65ced-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="65ced-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="65ced-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65ced-102">SYNOPSIS</span></span>
<span data-ttu-id="65ced-103">Importowanie i scalanie konfiguracji Kubectl dla Kubernetes zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="65ced-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ced-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65ced-104">SYNTAX</span></span>

### <span data-ttu-id="65ced-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65ced-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ced-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65ced-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ced-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65ced-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ced-108">Opis</span><span class="sxs-lookup"><span data-stu-id="65ced-108">DESCRIPTION</span></span>
<span data-ttu-id="65ced-109">Importowanie i scalanie konfiguracji Kubectl dla Kubernetes zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="65ced-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="65ced-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65ced-110">EXAMPLES</span></span>

### <span data-ttu-id="65ced-111">Importowanie i scalanie konfiguracji Kubectl</span><span class="sxs-lookup"><span data-stu-id="65ced-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="65ced-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65ced-112">PARAMETERS</span></span>

### <span data-ttu-id="65ced-113">-Administrator</span><span class="sxs-lookup"><span data-stu-id="65ced-113">-Admin</span></span>
<span data-ttu-id="65ced-114">Pobierz clusterAdmin' kubectl zamiast domyślnego "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="65ced-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="65ced-115">-ConfigPath</span></span>
<span data-ttu-id="65ced-116">Plik konfiguracji kubectl do utworzenia lub zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="65ced-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="65ced-117">Zamiast tego użyj polecenia "-", aby wydrukować YAML na stdout.</span><span class="sxs-lookup"><span data-stu-id="65ced-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="65ced-118">Wartość domyślna:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="65ced-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ced-119">-DefaultProfile</span></span>
<span data-ttu-id="65ced-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65ced-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-121">-Force</span><span class="sxs-lookup"><span data-stu-id="65ced-121">-Force</span></span>
<span data-ttu-id="65ced-122">Importowanie pliku Kubernetes, nawet jeśli jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="65ced-122">Import Kubernetes config even if it is the default</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-123">-ID</span><span class="sxs-lookup"><span data-stu-id="65ced-123">-Id</span></span>
<span data-ttu-id="65ced-124">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="65ced-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65ced-125">-InputObject</span></span>
<span data-ttu-id="65ced-126">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="65ced-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65ced-127">-Name</span></span>
<span data-ttu-id="65ced-128">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="65ced-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65ced-129">-PassThru</span></span>
<span data-ttu-id="65ced-130">Zwraca wartość PRAWDA, jeśli Importowanie kończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="65ced-130">Returns true if import is successful</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ced-131">-ResourceGroupName</span></span>
<span data-ttu-id="65ced-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="65ced-132">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65ced-133">-Confirm</span></span>
<span data-ttu-id="65ced-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ced-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ced-135">-WhatIf</span></span>
<span data-ttu-id="65ced-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ced-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ced-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65ced-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ced-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ced-138">CommonParameters</span></span>
<span data-ttu-id="65ced-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ced-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ced-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ced-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ced-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65ced-141">INPUTS</span></span>

### <span data-ttu-id="65ced-142">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="65ced-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="65ced-143">System. String</span><span class="sxs-lookup"><span data-stu-id="65ced-143">System.String</span></span>

## <span data-ttu-id="65ced-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65ced-144">OUTPUTS</span></span>

### <span data-ttu-id="65ced-145">System. String</span><span class="sxs-lookup"><span data-stu-id="65ced-145">System.String</span></span>

## <span data-ttu-id="65ced-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65ced-146">NOTES</span></span>

## <span data-ttu-id="65ced-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65ced-147">RELATED LINKS</span></span>
