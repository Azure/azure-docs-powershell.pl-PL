---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194922"
---
# <span data-ttu-id="295f7-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="295f7-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="295f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="295f7-102">SYNOPSIS</span></span>
<span data-ttu-id="295f7-103">Interfejs API do aktualizowania niektórych właściwości połączonego zasobu klastrów</span><span class="sxs-lookup"><span data-stu-id="295f7-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="295f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="295f7-104">SYNTAX</span></span>

### <span data-ttu-id="295f7-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="295f7-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="295f7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="295f7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="295f7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="295f7-107">DESCRIPTION</span></span>
<span data-ttu-id="295f7-108">Interfejs API do aktualizowania niektórych właściwości połączonego zasobu klastrów</span><span class="sxs-lookup"><span data-stu-id="295f7-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="295f7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="295f7-109">EXAMPLES</span></span>

### <span data-ttu-id="295f7-110">Przykład 1. Aktualizowanie podłączonych kubernetes</span><span class="sxs-lookup"><span data-stu-id="295f7-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="295f7-111">To polecenie aktualizuje połączone sieci kubernetes.</span><span class="sxs-lookup"><span data-stu-id="295f7-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="295f7-112">Przykład 2. Aktualizowanie połączonych kubernetów według obiektów</span><span class="sxs-lookup"><span data-stu-id="295f7-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="295f7-113">To polecenie aktualizuje połączone kubernety według obiektów.</span><span class="sxs-lookup"><span data-stu-id="295f7-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="295f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="295f7-114">PARAMETERS</span></span>

### <span data-ttu-id="295f7-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="295f7-115">-ClusterName</span></span>
<span data-ttu-id="295f7-116">Nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="295f7-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="295f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295f7-117">-DefaultProfile</span></span>
<span data-ttu-id="295f7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="295f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="295f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="295f7-119">-InputObject</span></span>
<span data-ttu-id="295f7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="295f7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="295f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="295f7-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="295f7-122">The name of the resource group.</span></span>
<span data-ttu-id="295f7-123">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="295f7-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="295f7-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="295f7-124">-SubscriptionId</span></span>
<span data-ttu-id="295f7-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="295f7-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="295f7-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="295f7-126">-Tag</span></span>
<span data-ttu-id="295f7-127">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="295f7-127">Resource tags.</span></span>

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

### <span data-ttu-id="295f7-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="295f7-128">-Confirm</span></span>
<span data-ttu-id="295f7-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="295f7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="295f7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295f7-130">-WhatIf</span></span>
<span data-ttu-id="295f7-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="295f7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295f7-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="295f7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="295f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295f7-133">CommonParameters</span></span>
<span data-ttu-id="295f7-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="295f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295f7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="295f7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295f7-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="295f7-136">INPUTS</span></span>

### <span data-ttu-id="295f7-137">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="295f7-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="295f7-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="295f7-138">OUTPUTS</span></span>

### <span data-ttu-id="295f7-139">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="295f7-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="295f7-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="295f7-140">NOTES</span></span>

<span data-ttu-id="295f7-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="295f7-141">ALIASES</span></span>

<span data-ttu-id="295f7-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="295f7-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="295f7-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="295f7-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="295f7-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="295f7-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="295f7-145">INPUTOBJECT: <IConnectedKubernetesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="295f7-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="295f7-146">`[ClusterName <String>]`: nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="295f7-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="295f7-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="295f7-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="295f7-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="295f7-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="295f7-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="295f7-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="295f7-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="295f7-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="295f7-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="295f7-151">RELATED LINKS</span></span>

