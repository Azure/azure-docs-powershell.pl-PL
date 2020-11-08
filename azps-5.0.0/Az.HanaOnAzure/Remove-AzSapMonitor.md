---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224307"
---
# <span data-ttu-id="40f18-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="40f18-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="40f18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40f18-102">SYNOPSIS</span></span>
<span data-ttu-id="40f18-103">Usuwa Monitor protokołu SAP z określoną subskrypcją, grupą zasobów i nazwą monitora.</span><span class="sxs-lookup"><span data-stu-id="40f18-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="40f18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40f18-104">SYNTAX</span></span>

### <span data-ttu-id="40f18-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="40f18-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40f18-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40f18-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40f18-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40f18-107">DESCRIPTION</span></span>
<span data-ttu-id="40f18-108">Usuwa Monitor protokołu SAP z określoną subskrypcją, grupą zasobów i nazwą monitora.</span><span class="sxs-lookup"><span data-stu-id="40f18-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="40f18-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40f18-109">EXAMPLES</span></span>

### <span data-ttu-id="40f18-110">Przykład 1: usuwanie monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="40f18-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="40f18-111">To polecenie usuwa Monitor protokołu SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="40f18-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="40f18-112">Przykład 2: usuwanie monitora SAP według obiektów</span><span class="sxs-lookup"><span data-stu-id="40f18-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="40f18-113">To polecenie usuwa Monitor protokołu SAP według obiektu.</span><span class="sxs-lookup"><span data-stu-id="40f18-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="40f18-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40f18-114">PARAMETERS</span></span>

### <span data-ttu-id="40f18-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40f18-115">-AsJob</span></span>
<span data-ttu-id="40f18-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="40f18-116">Run the command as a job</span></span>

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

### <span data-ttu-id="40f18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f18-117">-DefaultProfile</span></span>
<span data-ttu-id="40f18-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40f18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f18-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="40f18-119">-InputObject</span></span>
<span data-ttu-id="40f18-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="40f18-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="40f18-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40f18-121">-Name</span></span>
<span data-ttu-id="40f18-122">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="40f18-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f18-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="40f18-123">-NoWait</span></span>
<span data-ttu-id="40f18-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="40f18-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="40f18-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40f18-125">-PassThru</span></span>
<span data-ttu-id="40f18-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="40f18-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="40f18-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f18-127">-ResourceGroupName</span></span>
<span data-ttu-id="40f18-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40f18-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="40f18-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="40f18-129">-SubscriptionId</span></span>
<span data-ttu-id="40f18-130">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40f18-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="40f18-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="40f18-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40f18-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40f18-132">-Confirm</span></span>
<span data-ttu-id="40f18-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40f18-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f18-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f18-134">-WhatIf</span></span>
<span data-ttu-id="40f18-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40f18-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f18-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40f18-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f18-137">CommonParameters</span></span>
<span data-ttu-id="40f18-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40f18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f18-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40f18-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f18-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40f18-140">INPUTS</span></span>

### <span data-ttu-id="40f18-141">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="40f18-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="40f18-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40f18-142">OUTPUTS</span></span>

### <span data-ttu-id="40f18-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40f18-143">System.Boolean</span></span>

## <span data-ttu-id="40f18-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40f18-144">NOTES</span></span>

<span data-ttu-id="40f18-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="40f18-145">ALIASES</span></span>

<span data-ttu-id="40f18-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40f18-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40f18-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="40f18-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40f18-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40f18-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40f18-149">INPUTobject <IHanaOnAzureIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="40f18-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40f18-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="40f18-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40f18-151">`[Location <String>]`: Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="40f18-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="40f18-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="40f18-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="40f18-153">`[ProviderInstanceName <String>]`: Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="40f18-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="40f18-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40f18-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="40f18-155">`[ResourceName <String>]`: Nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="40f18-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="40f18-156">`[SapMonitorName <String>]`: Nazwa zasobu monitora SAP.</span><span class="sxs-lookup"><span data-stu-id="40f18-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="40f18-157">`[Scope <String>]`: Zakres zasobu dostawca zasobów.</span><span class="sxs-lookup"><span data-stu-id="40f18-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="40f18-158">Zasób nadrzędny jest rozszerzany przez zarządzane tożsamości.</span><span class="sxs-lookup"><span data-stu-id="40f18-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="40f18-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40f18-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="40f18-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="40f18-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="40f18-161">`[VaultName <String>]`: Nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="40f18-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="40f18-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40f18-162">RELATED LINKS</span></span>

