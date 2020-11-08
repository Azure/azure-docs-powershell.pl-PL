---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233454"
---
# <span data-ttu-id="7648f-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="7648f-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="7648f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7648f-102">SYNOPSIS</span></span>
<span data-ttu-id="7648f-103">Usuwanie listy rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="7648f-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7648f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7648f-104">SYNTAX</span></span>

### <span data-ttu-id="7648f-105">RemoveExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7648f-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7648f-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7648f-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7648f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7648f-107">DESCRIPTION</span></span>
<span data-ttu-id="7648f-108">Usuwanie listy rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="7648f-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7648f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7648f-109">EXAMPLES</span></span>

### <span data-ttu-id="7648f-110">Przykład 1: Usuwanie listy rozszerzeń języków z klastra</span><span class="sxs-lookup"><span data-stu-id="7648f-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="7648f-111">Powyższe polecenie usuwa listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="7648f-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7648f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7648f-112">PARAMETERS</span></span>

### <span data-ttu-id="7648f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7648f-113">-AsJob</span></span>
<span data-ttu-id="7648f-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7648f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7648f-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="7648f-115">-ClusterName</span></span>
<span data-ttu-id="7648f-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7648f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7648f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7648f-117">-DefaultProfile</span></span>
<span data-ttu-id="7648f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7648f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7648f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7648f-119">-InputObject</span></span>
<span data-ttu-id="7648f-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7648f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7648f-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7648f-121">-NoWait</span></span>
<span data-ttu-id="7648f-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7648f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7648f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7648f-123">-PassThru</span></span>
<span data-ttu-id="7648f-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="7648f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7648f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7648f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7648f-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7648f-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7648f-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7648f-127">-SubscriptionId</span></span>
<span data-ttu-id="7648f-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7648f-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7648f-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7648f-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7648f-130">-Value</span><span class="sxs-lookup"><span data-stu-id="7648f-130">-Value</span></span>
<span data-ttu-id="7648f-131">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="7648f-131">The list of language extensions.</span></span>
<span data-ttu-id="7648f-132">Aby skonstruować, zobacz sekcję notatki dla właściwości wartości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="7648f-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7648f-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7648f-133">-Confirm</span></span>
<span data-ttu-id="7648f-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7648f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7648f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7648f-135">-WhatIf</span></span>
<span data-ttu-id="7648f-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7648f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7648f-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7648f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7648f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7648f-138">CommonParameters</span></span>
<span data-ttu-id="7648f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7648f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7648f-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7648f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7648f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7648f-141">INPUTS</span></span>

### <span data-ttu-id="7648f-142">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7648f-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7648f-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7648f-143">OUTPUTS</span></span>

### <span data-ttu-id="7648f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7648f-144">System.Boolean</span></span>

## <span data-ttu-id="7648f-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7648f-145">NOTES</span></span>

<span data-ttu-id="7648f-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7648f-146">ALIASES</span></span>

<span data-ttu-id="7648f-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7648f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7648f-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7648f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7648f-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7648f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7648f-150">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7648f-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7648f-151">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7648f-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7648f-152">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7648f-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7648f-153">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="7648f-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7648f-154">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7648f-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7648f-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7648f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7648f-156">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7648f-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7648f-157">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7648f-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7648f-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7648f-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7648f-159">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7648f-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7648f-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7648f-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="7648f-161">WARTOŚĆ <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="7648f-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="7648f-162">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="7648f-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="7648f-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7648f-163">RELATED LINKS</span></span>

