---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012481"
---
# <span data-ttu-id="5fbba-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="5fbba-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="5fbba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbba-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbba-103">Usuń połączony klaster, usuwając śledzony zasób w usłudze Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="5fbba-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="5fbba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5fbba-104">SYNTAX</span></span>

### <span data-ttu-id="5fbba-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="5fbba-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5fbba-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5fbba-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbba-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5fbba-107">DESCRIPTION</span></span>
<span data-ttu-id="5fbba-108">Usuń połączony klaster, usuwając śledzony zasób w usłudze Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="5fbba-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="5fbba-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5fbba-109">EXAMPLES</span></span>

### <span data-ttu-id="5fbba-110">Przykład 1. Usuwanie połączonych kubernetes</span><span class="sxs-lookup"><span data-stu-id="5fbba-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="5fbba-111">To polecenie usuwa połączone kubernety</span><span class="sxs-lookup"><span data-stu-id="5fbba-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="5fbba-112">Przykład 2. Usuwanie połączonych kubernetesów według obiektu</span><span class="sxs-lookup"><span data-stu-id="5fbba-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="5fbba-113">To polecenie usuwa połączone kubernety według obiektów</span><span class="sxs-lookup"><span data-stu-id="5fbba-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="5fbba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fbba-114">PARAMETERS</span></span>

### <span data-ttu-id="5fbba-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5fbba-115">-AsJob</span></span>
<span data-ttu-id="5fbba-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5fbba-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5fbba-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5fbba-117">-ClusterName</span></span>
<span data-ttu-id="5fbba-118">Nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="5fbba-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbba-119">-DefaultProfile</span></span>
<span data-ttu-id="5fbba-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fbba-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fbba-121">-InputObject</span></span>
<span data-ttu-id="5fbba-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5fbba-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbba-123">- KubeConfig</span><span class="sxs-lookup"><span data-stu-id="5fbba-123">-KubeConfig</span></span>
<span data-ttu-id="5fbba-124">Ścieżka do pliku konfiguracji kube</span><span class="sxs-lookup"><span data-stu-id="5fbba-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="5fbba-125">- KubeContext</span><span class="sxs-lookup"><span data-stu-id="5fbba-125">-KubeContext</span></span>
<span data-ttu-id="5fbba-126">Kontekst konfiguracji z bieżącego komputera</span><span class="sxs-lookup"><span data-stu-id="5fbba-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="5fbba-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5fbba-127">-NoWait</span></span>
<span data-ttu-id="5fbba-128">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5fbba-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5fbba-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fbba-129">-PassThru</span></span>
<span data-ttu-id="5fbba-130">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="5fbba-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5fbba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbba-131">-ResourceGroupName</span></span>
<span data-ttu-id="5fbba-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fbba-132">The name of the resource group.</span></span>
<span data-ttu-id="5fbba-133">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="5fbba-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5fbba-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fbba-134">-SubscriptionId</span></span>
<span data-ttu-id="5fbba-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5fbba-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5fbba-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fbba-136">-Confirm</span></span>
<span data-ttu-id="5fbba-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5fbba-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fbba-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbba-138">-WhatIf</span></span>
<span data-ttu-id="5fbba-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fbba-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fbba-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5fbba-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fbba-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbba-141">CommonParameters</span></span>
<span data-ttu-id="5fbba-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbba-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbba-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fbba-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbba-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fbba-144">INPUTS</span></span>

### <span data-ttu-id="5fbba-145">Microsoft.Azure.PowerShell.cmdlet.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="5fbba-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="5fbba-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fbba-146">OUTPUTS</span></span>

### <span data-ttu-id="5fbba-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5fbba-147">System.Boolean</span></span>

## <span data-ttu-id="5fbba-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5fbba-148">NOTES</span></span>

<span data-ttu-id="5fbba-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5fbba-149">ALIASES</span></span>

<span data-ttu-id="5fbba-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fbba-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fbba-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5fbba-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fbba-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fbba-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fbba-153">INPUTOBJECT: <IConnectedKubernetesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="5fbba-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5fbba-154">`[ClusterName <String>]`: nazwa klastru Kubernetes, do którego jest dzwonić.</span><span class="sxs-lookup"><span data-stu-id="5fbba-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="5fbba-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5fbba-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5fbba-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fbba-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5fbba-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="5fbba-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="5fbba-158">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5fbba-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5fbba-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fbba-159">RELATED LINKS</span></span>

