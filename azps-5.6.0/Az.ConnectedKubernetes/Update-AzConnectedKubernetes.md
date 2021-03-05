---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2e0c7f11592238f11f49e82102c6d58c24f8b9fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012442"
---
# <span data-ttu-id="3dab4-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="3dab4-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="3dab4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dab4-102">SYNOPSIS</span></span>
<span data-ttu-id="3dab4-103">Interfejs API do aktualizowania niektórych właściwości połączonego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="3dab4-103">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="3dab4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3dab4-104">SYNTAX</span></span>

### <span data-ttu-id="3dab4-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3dab4-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3dab4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3dab4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3dab4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3dab4-107">DESCRIPTION</span></span>
<span data-ttu-id="3dab4-108">Interfejs API do aktualizowania niektórych właściwości połączonego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="3dab4-108">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="3dab4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3dab4-109">EXAMPLES</span></span>

### <span data-ttu-id="3dab4-110">Przykład 1. Aktualizowanie podłączonych kubernetes</span><span class="sxs-lookup"><span data-stu-id="3dab4-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="3dab4-111">To polecenie aktualizuje połączone sieci kubernetes.</span><span class="sxs-lookup"><span data-stu-id="3dab4-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="3dab4-112">Przykład 2. Aktualizowanie połączonych kubernetów według obiektów</span><span class="sxs-lookup"><span data-stu-id="3dab4-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="3dab4-113">To polecenie aktualizuje połączone kubernety według obiektów.</span><span class="sxs-lookup"><span data-stu-id="3dab4-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="3dab4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dab4-114">PARAMETERS</span></span>

### <span data-ttu-id="3dab4-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3dab4-115">-ClusterName</span></span>
<span data-ttu-id="3dab4-116">Nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="3dab4-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dab4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dab4-117">-DefaultProfile</span></span>
<span data-ttu-id="3dab4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dab4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dab4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dab4-119">-InputObject</span></span>
<span data-ttu-id="3dab4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3dab4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dab4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dab4-121">-ResourceGroupName</span></span>
<span data-ttu-id="3dab4-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3dab4-122">The name of the resource group.</span></span>
<span data-ttu-id="3dab4-123">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3dab4-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dab4-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3dab4-124">-SubscriptionId</span></span>
<span data-ttu-id="3dab4-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3dab4-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dab4-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="3dab4-126">-Tag</span></span>
<span data-ttu-id="3dab4-127">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3dab4-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dab4-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dab4-128">-Confirm</span></span>
<span data-ttu-id="3dab4-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3dab4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dab4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dab4-130">-WhatIf</span></span>
<span data-ttu-id="3dab4-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dab4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dab4-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3dab4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dab4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dab4-133">CommonParameters</span></span>
<span data-ttu-id="3dab4-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dab4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dab4-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dab4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dab4-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dab4-136">INPUTS</span></span>

### <span data-ttu-id="3dab4-137">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="3dab4-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="3dab4-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dab4-138">OUTPUTS</span></span>

### <span data-ttu-id="3dab4-139">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="3dab4-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="3dab4-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3dab4-140">NOTES</span></span>

<span data-ttu-id="3dab4-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3dab4-141">ALIASES</span></span>

<span data-ttu-id="3dab4-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dab4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3dab4-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3dab4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3dab4-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3dab4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3dab4-145">INPUTOBJECT: <IConnectedKubernetesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3dab4-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3dab4-146">`[ClusterName <String>]`: nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="3dab4-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="3dab4-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3dab4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3dab4-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3dab4-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3dab4-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3dab4-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3dab4-150">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3dab4-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="3dab4-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dab4-151">RELATED LINKS</span></span>

