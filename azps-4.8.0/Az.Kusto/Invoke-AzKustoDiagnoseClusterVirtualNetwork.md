---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222518"
---
# <span data-ttu-id="84c9d-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="84c9d-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="84c9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="84c9d-103">Diagnozuje stan łączności sieciowej dla zasobów zewnętrznych, od których zależy usługa.</span><span class="sxs-lookup"><span data-stu-id="84c9d-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="84c9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84c9d-104">SYNTAX</span></span>

### <span data-ttu-id="84c9d-105">Diagnozuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="84c9d-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="84c9d-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="84c9d-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84c9d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="84c9d-107">DESCRIPTION</span></span>
<span data-ttu-id="84c9d-108">Diagnozuje stan łączności sieciowej dla zasobów zewnętrznych, od których zależy usługa.</span><span class="sxs-lookup"><span data-stu-id="84c9d-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="84c9d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84c9d-109">EXAMPLES</span></span>

### <span data-ttu-id="84c9d-110">Przykład 1: pokazywanie diagnostyki łączności sieciowej dla zasobów zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="84c9d-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="84c9d-111">Powyższe polecenie diagnozuje stan łączności sieciowej dla zasobów zewnętrznych, na których jest zależny klaster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="84c9d-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="84c9d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84c9d-112">PARAMETERS</span></span>

### <span data-ttu-id="84c9d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84c9d-113">-AsJob</span></span>
<span data-ttu-id="84c9d-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="84c9d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="84c9d-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="84c9d-115">-ClusterName</span></span>
<span data-ttu-id="84c9d-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="84c9d-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c9d-117">-DefaultProfile</span></span>
<span data-ttu-id="84c9d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84c9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c9d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84c9d-119">-InputObject</span></span>
<span data-ttu-id="84c9d-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="84c9d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84c9d-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="84c9d-121">-NoWait</span></span>
<span data-ttu-id="84c9d-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="84c9d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84c9d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c9d-123">-ResourceGroupName</span></span>
<span data-ttu-id="84c9d-124">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="84c9d-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c9d-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="84c9d-125">-SubscriptionId</span></span>
<span data-ttu-id="84c9d-126">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84c9d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84c9d-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="84c9d-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c9d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84c9d-128">-Confirm</span></span>
<span data-ttu-id="84c9d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c9d-130">-WhatIf</span></span>
<span data-ttu-id="84c9d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c9d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84c9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c9d-133">CommonParameters</span></span>
<span data-ttu-id="84c9d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c9d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84c9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c9d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84c9d-136">INPUTS</span></span>

### <span data-ttu-id="84c9d-137">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="84c9d-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="84c9d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84c9d-138">OUTPUTS</span></span>

### <span data-ttu-id="84c9d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84c9d-139">System.String</span></span>

## <span data-ttu-id="84c9d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84c9d-140">NOTES</span></span>

<span data-ttu-id="84c9d-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="84c9d-141">ALIASES</span></span>

<span data-ttu-id="84c9d-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84c9d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84c9d-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="84c9d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84c9d-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84c9d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84c9d-145">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="84c9d-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84c9d-146">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="84c9d-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="84c9d-147">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="84c9d-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="84c9d-148">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="84c9d-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="84c9d-149">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="84c9d-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="84c9d-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="84c9d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84c9d-151">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="84c9d-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="84c9d-152">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="84c9d-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="84c9d-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="84c9d-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="84c9d-154">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84c9d-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="84c9d-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="84c9d-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="84c9d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84c9d-156">RELATED LINKS</span></span>

