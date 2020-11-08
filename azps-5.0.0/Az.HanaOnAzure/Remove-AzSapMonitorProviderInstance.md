---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231860"
---
# <span data-ttu-id="f7c8d-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f7c8d-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="f7c8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c8d-103">Usuwa wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f7c8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7c8d-104">SYNTAX</span></span>

### <span data-ttu-id="f7c8d-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f7c8d-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7c8d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7c8d-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7c8d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7c8d-107">DESCRIPTION</span></span>
<span data-ttu-id="f7c8d-108">Usuwa wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f7c8d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7c8d-109">EXAMPLES</span></span>

### <span data-ttu-id="f7c8d-110">Przykład 1: usuwanie wystąpienia monitora protokołu SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="f7c8d-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="f7c8d-111">To polecenie powoduje usunięcie wystąpienia monitora protokołu SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="f7c8d-112">Przykład 2: usuwanie wystąpienia monitora protokołu SAP według obiektów</span><span class="sxs-lookup"><span data-stu-id="f7c8d-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="f7c8d-113">To polecenie powoduje usunięcie wystąpienia monitora protokołu SAP według obiektu.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="f7c8d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7c8d-114">PARAMETERS</span></span>

### <span data-ttu-id="f7c8d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7c8d-115">-AsJob</span></span>
<span data-ttu-id="f7c8d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f7c8d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f7c8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c8d-117">-DefaultProfile</span></span>
<span data-ttu-id="f7c8d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7c8d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7c8d-119">-InputObject</span></span>
<span data-ttu-id="f7c8d-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c8d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7c8d-121">-Name</span></span>
<span data-ttu-id="f7c8d-122">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c8d-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f7c8d-123">-NoWait</span></span>
<span data-ttu-id="f7c8d-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f7c8d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7c8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7c8d-125">-PassThru</span></span>
<span data-ttu-id="f7c8d-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f7c8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7c8d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="f7c8d-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="f7c8d-129">-SapMonitorName</span></span>
<span data-ttu-id="f7c8d-130">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f7c8d-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f7c8d-131">-SubscriptionId</span></span>
<span data-ttu-id="f7c8d-132">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f7c8d-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f7c8d-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7c8d-134">-Confirm</span></span>
<span data-ttu-id="f7c8d-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7c8d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7c8d-136">-WhatIf</span></span>
<span data-ttu-id="f7c8d-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7c8d-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7c8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c8d-139">CommonParameters</span></span>
<span data-ttu-id="f7c8d-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c8d-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7c8d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c8d-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7c8d-142">INPUTS</span></span>

### <span data-ttu-id="f7c8d-143">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="f7c8d-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f7c8d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7c8d-144">OUTPUTS</span></span>

### <span data-ttu-id="f7c8d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7c8d-145">System.Boolean</span></span>

## <span data-ttu-id="f7c8d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7c8d-146">NOTES</span></span>

<span data-ttu-id="f7c8d-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f7c8d-147">ALIASES</span></span>

<span data-ttu-id="f7c8d-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7c8d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7c8d-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7c8d-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7c8d-151">INPUTobject <IHanaOnAzureIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f7c8d-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7c8d-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f7c8d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7c8d-153">`[Location <String>]`: Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f7c8d-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="f7c8d-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f7c8d-155">`[ProviderInstanceName <String>]`: Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f7c8d-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f7c8d-157">`[ResourceName <String>]`: Nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f7c8d-158">`[SapMonitorName <String>]`: Nazwa zasobu monitora SAP.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f7c8d-159">`[Scope <String>]`: Zakres zasobu dostawca zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f7c8d-160">Zasób nadrzędny jest rozszerzany przez zarządzane tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f7c8d-161">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f7c8d-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f7c8d-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f7c8d-163">`[VaultName <String>]`: Nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="f7c8d-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f7c8d-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7c8d-164">RELATED LINKS</span></span>

