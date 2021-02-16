---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 9cac9f92e61ac17ed825dd3e39991fc85c661d9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194307"
---
# <span data-ttu-id="84a57-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="84a57-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="84a57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a57-102">SYNOPSIS</span></span>
<span data-ttu-id="84a57-103">Usuń listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="84a57-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="84a57-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84a57-104">SYNTAX</span></span>

### <span data-ttu-id="84a57-105">RemoveExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="84a57-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="84a57-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="84a57-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84a57-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="84a57-107">DESCRIPTION</span></span>
<span data-ttu-id="84a57-108">Usuń listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="84a57-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="84a57-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84a57-109">EXAMPLES</span></span>

### <span data-ttu-id="84a57-110">Przykład 1. Usuwanie listy rozszerzeń językowych z klastrów</span><span class="sxs-lookup"><span data-stu-id="84a57-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="84a57-111">Powyższe polecenie usuwa listę rozszerzeń językowych, które można uruchamiać w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="84a57-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="84a57-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84a57-112">PARAMETERS</span></span>

### <span data-ttu-id="84a57-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="84a57-113">-AsJob</span></span>
<span data-ttu-id="84a57-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="84a57-114">Run the command as a job</span></span>

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

### <span data-ttu-id="84a57-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="84a57-115">-ClusterName</span></span>
<span data-ttu-id="84a57-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="84a57-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a57-117">-DefaultProfile</span></span>
<span data-ttu-id="84a57-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84a57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a57-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84a57-119">-InputObject</span></span>
<span data-ttu-id="84a57-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="84a57-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84a57-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84a57-121">-NoWait</span></span>
<span data-ttu-id="84a57-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="84a57-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84a57-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84a57-123">-PassThru</span></span>
<span data-ttu-id="84a57-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="84a57-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="84a57-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a57-125">-ResourceGroupName</span></span>
<span data-ttu-id="84a57-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="84a57-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a57-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84a57-127">-SubscriptionId</span></span>
<span data-ttu-id="84a57-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84a57-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84a57-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="84a57-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a57-130">— Wartość</span><span class="sxs-lookup"><span data-stu-id="84a57-130">-Value</span></span>
<span data-ttu-id="84a57-131">Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="84a57-131">The list of language extensions.</span></span>
<span data-ttu-id="84a57-132">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WARTOŚCI i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="84a57-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a57-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84a57-133">-Confirm</span></span>
<span data-ttu-id="84a57-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84a57-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a57-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a57-135">-WhatIf</span></span>
<span data-ttu-id="84a57-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a57-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a57-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84a57-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a57-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a57-138">CommonParameters</span></span>
<span data-ttu-id="84a57-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a57-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a57-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84a57-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a57-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84a57-141">INPUTS</span></span>

### <span data-ttu-id="84a57-142">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="84a57-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="84a57-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84a57-143">OUTPUTS</span></span>

### <span data-ttu-id="84a57-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84a57-144">System.Boolean</span></span>

## <span data-ttu-id="84a57-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84a57-145">NOTES</span></span>

<span data-ttu-id="84a57-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="84a57-146">ALIASES</span></span>

<span data-ttu-id="84a57-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84a57-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84a57-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="84a57-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84a57-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84a57-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84a57-150">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="84a57-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84a57-151">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="84a57-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="84a57-152">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="84a57-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="84a57-153">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="84a57-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="84a57-154">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="84a57-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="84a57-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="84a57-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84a57-156">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="84a57-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="84a57-157">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="84a57-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="84a57-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="84a57-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="84a57-159">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84a57-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="84a57-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="84a57-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="84a57-161">VALUE <ILanguageExtension[]>: Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="84a57-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="84a57-162">`[Name <LanguageExtensionName?>]`: nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="84a57-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="84a57-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84a57-163">RELATED LINKS</span></span>

