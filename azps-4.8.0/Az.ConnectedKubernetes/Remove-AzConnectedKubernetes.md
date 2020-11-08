---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220127"
---
# <span data-ttu-id="ad0d6-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="ad0d6-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="ad0d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0d6-103">Usuń podłączony klaster, usuwając prześledzony zasób w Menedżerze zasobów Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="ad0d6-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="ad0d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad0d6-104">SYNTAX</span></span>

### <span data-ttu-id="ad0d6-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ad0d6-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ad0d6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad0d6-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ad0d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad0d6-107">DESCRIPTION</span></span>
<span data-ttu-id="ad0d6-108">Usuń podłączony klaster, usuwając prześledzony zasób w Menedżerze zasobów Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="ad0d6-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="ad0d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad0d6-109">EXAMPLES</span></span>

### <span data-ttu-id="ad0d6-110">Przykład 1: usuwanie połączonego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ad0d6-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="ad0d6-111">To polecenie usuwa podłączony Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ad0d6-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="ad0d6-112">Przykład 2: usuwanie połączonego Kubernetes przez obiekt</span><span class="sxs-lookup"><span data-stu-id="ad0d6-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="ad0d6-113">To polecenie usuwa połączony Kubernetes przez obiekt</span><span class="sxs-lookup"><span data-stu-id="ad0d6-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="ad0d6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad0d6-114">PARAMETERS</span></span>

### <span data-ttu-id="ad0d6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad0d6-115">-AsJob</span></span>
<span data-ttu-id="ad0d6-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ad0d6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ad0d6-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ad0d6-117">-ClusterName</span></span>
<span data-ttu-id="ad0d6-118">Nazwa klastra usługi Kubernetes, na którym jest wywoływana pozycja get.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="ad0d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0d6-119">-DefaultProfile</span></span>
<span data-ttu-id="ad0d6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0d6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad0d6-121">-InputObject</span></span>
<span data-ttu-id="ad0d6-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad0d6-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="ad0d6-123">-KubeConfig</span></span>
<span data-ttu-id="ad0d6-124">Ścieżka do pliku konfiguracji Kube</span><span class="sxs-lookup"><span data-stu-id="ad0d6-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="ad0d6-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="ad0d6-125">-KubeContext</span></span>
<span data-ttu-id="ad0d6-126">Kubconfig kontekst na bieżącym komputerze</span><span class="sxs-lookup"><span data-stu-id="ad0d6-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="ad0d6-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ad0d6-127">-NoWait</span></span>
<span data-ttu-id="ad0d6-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ad0d6-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad0d6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad0d6-129">-PassThru</span></span>
<span data-ttu-id="ad0d6-130">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad0d6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0d6-131">-ResourceGroupName</span></span>
<span data-ttu-id="ad0d6-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-132">The name of the resource group.</span></span>
<span data-ttu-id="ad0d6-133">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ad0d6-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ad0d6-134">-SubscriptionId</span></span>
<span data-ttu-id="ad0d6-135">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ad0d6-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad0d6-136">-Confirm</span></span>
<span data-ttu-id="ad0d6-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0d6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0d6-138">-WhatIf</span></span>
<span data-ttu-id="ad0d6-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad0d6-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0d6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0d6-141">CommonParameters</span></span>
<span data-ttu-id="ad0d6-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0d6-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad0d6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0d6-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad0d6-144">INPUTS</span></span>

### <span data-ttu-id="ad0d6-145">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="ad0d6-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="ad0d6-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad0d6-146">OUTPUTS</span></span>

### <span data-ttu-id="ad0d6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad0d6-147">System.Boolean</span></span>

## <span data-ttu-id="ad0d6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad0d6-148">NOTES</span></span>

<span data-ttu-id="ad0d6-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ad0d6-149">ALIASES</span></span>

<span data-ttu-id="ad0d6-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad0d6-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad0d6-151">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad0d6-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad0d6-153">INPUTobject <IConnectedKubernetesIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ad0d6-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad0d6-154">`[ClusterName <String>]`: Nazwa klastra usługi Kubernetes, na którym jest wywoływana metoda get.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="ad0d6-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ad0d6-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad0d6-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ad0d6-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="ad0d6-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ad0d6-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad0d6-159">RELATED LINKS</span></span>

