---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 6a687139f7dec156e539c09b864a88c4e8876fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972826"
---
# <span data-ttu-id="bb829-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="bb829-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="bb829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb829-102">SYNOPSIS</span></span>
<span data-ttu-id="bb829-103">Usuń listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="bb829-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="bb829-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb829-104">SYNTAX</span></span>

### <span data-ttu-id="bb829-105">RemoveExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="bb829-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb829-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bb829-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb829-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb829-107">DESCRIPTION</span></span>
<span data-ttu-id="bb829-108">Usuń listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="bb829-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="bb829-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb829-109">EXAMPLES</span></span>

### <span data-ttu-id="bb829-110">Przykład 1. Usuwanie listy rozszerzeń językowych z klastrów</span><span class="sxs-lookup"><span data-stu-id="bb829-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="bb829-111">Powyższe polecenie usuwa listę rozszerzeń językowych, które można uruchamiać w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="bb829-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="bb829-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb829-112">PARAMETERS</span></span>

### <span data-ttu-id="bb829-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bb829-113">-AsJob</span></span>
<span data-ttu-id="bb829-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bb829-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bb829-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bb829-115">-ClusterName</span></span>
<span data-ttu-id="bb829-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb829-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="bb829-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb829-117">-DefaultProfile</span></span>
<span data-ttu-id="bb829-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb829-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb829-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb829-119">-InputObject</span></span>
<span data-ttu-id="bb829-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bb829-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb829-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bb829-121">-NoWait</span></span>
<span data-ttu-id="bb829-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bb829-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb829-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb829-123">-PassThru</span></span>
<span data-ttu-id="bb829-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bb829-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bb829-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb829-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb829-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb829-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="bb829-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb829-127">-SubscriptionId</span></span>
<span data-ttu-id="bb829-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bb829-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bb829-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="bb829-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bb829-130">— Wartość</span><span class="sxs-lookup"><span data-stu-id="bb829-130">-Value</span></span>
<span data-ttu-id="bb829-131">Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="bb829-131">The list of language extensions.</span></span>
<span data-ttu-id="bb829-132">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WARTOŚCI i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="bb829-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb829-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb829-133">-Confirm</span></span>
<span data-ttu-id="bb829-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb829-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb829-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb829-135">-WhatIf</span></span>
<span data-ttu-id="bb829-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb829-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb829-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb829-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb829-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb829-138">CommonParameters</span></span>
<span data-ttu-id="bb829-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb829-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb829-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb829-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb829-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb829-141">INPUTS</span></span>

### <span data-ttu-id="bb829-142">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bb829-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bb829-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb829-143">OUTPUTS</span></span>

### <span data-ttu-id="bb829-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb829-144">System.Boolean</span></span>

## <span data-ttu-id="bb829-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb829-145">NOTES</span></span>

<span data-ttu-id="bb829-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bb829-146">ALIASES</span></span>

<span data-ttu-id="bb829-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb829-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb829-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bb829-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb829-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb829-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb829-150">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bb829-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb829-151">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bb829-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bb829-152">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb829-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bb829-153">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="bb829-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bb829-154">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb829-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bb829-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bb829-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb829-156">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bb829-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bb829-157">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="bb829-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bb829-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb829-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bb829-159">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bb829-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bb829-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="bb829-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="bb829-161">VALUE <ILanguageExtension[]>: Lista rozszerzeń językowych.</span><span class="sxs-lookup"><span data-stu-id="bb829-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="bb829-162">`[Name <LanguageExtensionName?>]`: nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="bb829-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="bb829-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb829-163">RELATED LINKS</span></span>

