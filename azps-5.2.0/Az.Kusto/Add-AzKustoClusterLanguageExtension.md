---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361636"
---
# <span data-ttu-id="f9201-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="f9201-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="f9201-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9201-102">SYNOPSIS</span></span>
<span data-ttu-id="f9201-103">Dodaj listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="f9201-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f9201-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9201-104">SYNTAX</span></span>

### <span data-ttu-id="f9201-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f9201-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f9201-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f9201-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9201-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f9201-107">DESCRIPTION</span></span>
<span data-ttu-id="f9201-108">Dodaj listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="f9201-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f9201-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9201-109">EXAMPLES</span></span>

### <span data-ttu-id="f9201-110">Przykład 1: Dodawanie listy rozszerzeń języków</span><span class="sxs-lookup"><span data-stu-id="f9201-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="f9201-111">Powyższe polecenie dodaje listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword</span><span class="sxs-lookup"><span data-stu-id="f9201-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="f9201-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9201-112">PARAMETERS</span></span>

### <span data-ttu-id="f9201-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9201-113">-AsJob</span></span>
<span data-ttu-id="f9201-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f9201-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f9201-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="f9201-115">-ClusterName</span></span>
<span data-ttu-id="f9201-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9201-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9201-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9201-117">-DefaultProfile</span></span>
<span data-ttu-id="f9201-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9201-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9201-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9201-119">-InputObject</span></span>
<span data-ttu-id="f9201-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f9201-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9201-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f9201-121">-NoWait</span></span>
<span data-ttu-id="f9201-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f9201-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f9201-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9201-123">-PassThru</span></span>
<span data-ttu-id="f9201-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="f9201-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f9201-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9201-125">-ResourceGroupName</span></span>
<span data-ttu-id="f9201-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9201-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9201-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f9201-127">-SubscriptionId</span></span>
<span data-ttu-id="f9201-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9201-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9201-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f9201-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9201-130">-Value</span><span class="sxs-lookup"><span data-stu-id="f9201-130">-Value</span></span>
<span data-ttu-id="f9201-131">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="f9201-131">The list of language extensions.</span></span>
<span data-ttu-id="f9201-132">Aby skonstruować, zobacz sekcję notatki dla właściwości wartości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="f9201-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9201-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9201-133">-Confirm</span></span>
<span data-ttu-id="f9201-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9201-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9201-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9201-135">-WhatIf</span></span>
<span data-ttu-id="f9201-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9201-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9201-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9201-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9201-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9201-138">CommonParameters</span></span>
<span data-ttu-id="f9201-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9201-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9201-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9201-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9201-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9201-141">INPUTS</span></span>

### <span data-ttu-id="f9201-142">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f9201-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f9201-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9201-143">OUTPUTS</span></span>

### <span data-ttu-id="f9201-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9201-144">System.Boolean</span></span>

## <span data-ttu-id="f9201-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9201-145">NOTES</span></span>

<span data-ttu-id="f9201-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f9201-146">ALIASES</span></span>

<span data-ttu-id="f9201-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9201-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f9201-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f9201-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9201-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9201-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f9201-150">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f9201-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9201-151">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f9201-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f9201-152">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9201-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f9201-153">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="f9201-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f9201-154">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9201-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f9201-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f9201-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9201-156">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9201-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f9201-157">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f9201-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f9201-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9201-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f9201-159">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9201-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f9201-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f9201-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f9201-161">WARTOŚĆ <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="f9201-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="f9201-162">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="f9201-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="f9201-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9201-163">RELATED LINKS</span></span>

