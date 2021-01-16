---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368818"
---
# <span data-ttu-id="219fd-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="219fd-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="219fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="219fd-102">SYNOPSIS</span></span>
<span data-ttu-id="219fd-103">Interfejs API umożliwiający aktualizowanie określonych właściwości połączonego zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="219fd-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="219fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="219fd-104">SYNTAX</span></span>

### <span data-ttu-id="219fd-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="219fd-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="219fd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="219fd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="219fd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="219fd-107">DESCRIPTION</span></span>
<span data-ttu-id="219fd-108">Interfejs API umożliwiający aktualizowanie określonych właściwości połączonego zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="219fd-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="219fd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="219fd-109">EXAMPLES</span></span>

### <span data-ttu-id="219fd-110">Przykład 1: aktualizowanie połączonego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="219fd-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="219fd-111">To polecenie aktualizuje podłączony Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="219fd-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="219fd-112">Przykład 2: aktualizowanie połączonego Kubernetes przez obiekt</span><span class="sxs-lookup"><span data-stu-id="219fd-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="219fd-113">To polecenie aktualizuje połączony Kubernetes przez obiekt.</span><span class="sxs-lookup"><span data-stu-id="219fd-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="219fd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="219fd-114">PARAMETERS</span></span>

### <span data-ttu-id="219fd-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="219fd-115">-ClusterName</span></span>
<span data-ttu-id="219fd-116">Nazwa klastra usługi Kubernetes, na którym jest wywoływana pozycja get.</span><span class="sxs-lookup"><span data-stu-id="219fd-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="219fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219fd-117">-DefaultProfile</span></span>
<span data-ttu-id="219fd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="219fd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219fd-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="219fd-119">-InputObject</span></span>
<span data-ttu-id="219fd-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="219fd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="219fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="219fd-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="219fd-122">The name of the resource group.</span></span>
<span data-ttu-id="219fd-123">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="219fd-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="219fd-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="219fd-124">-SubscriptionId</span></span>
<span data-ttu-id="219fd-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="219fd-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="219fd-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="219fd-126">-Tag</span></span>
<span data-ttu-id="219fd-127">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="219fd-127">Resource tags.</span></span>

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

### <span data-ttu-id="219fd-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="219fd-128">-Confirm</span></span>
<span data-ttu-id="219fd-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219fd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219fd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219fd-130">-WhatIf</span></span>
<span data-ttu-id="219fd-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219fd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219fd-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="219fd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219fd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219fd-133">CommonParameters</span></span>
<span data-ttu-id="219fd-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219fd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219fd-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="219fd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219fd-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="219fd-136">INPUTS</span></span>

### <span data-ttu-id="219fd-137">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="219fd-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="219fd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="219fd-138">OUTPUTS</span></span>

### <span data-ttu-id="219fd-139">Microsoft. Azure. PowerShell. polecenia. ConnectedKubernetes. models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="219fd-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="219fd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="219fd-140">NOTES</span></span>

<span data-ttu-id="219fd-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="219fd-141">ALIASES</span></span>

<span data-ttu-id="219fd-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="219fd-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="219fd-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="219fd-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="219fd-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="219fd-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="219fd-145">INPUTobject <IConnectedKubernetesIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="219fd-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="219fd-146">`[ClusterName <String>]`: Nazwa klastra usługi Kubernetes, na którym jest wywoływana metoda get.</span><span class="sxs-lookup"><span data-stu-id="219fd-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="219fd-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="219fd-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="219fd-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="219fd-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="219fd-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="219fd-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="219fd-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="219fd-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="219fd-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="219fd-151">RELATED LINKS</span></span>

