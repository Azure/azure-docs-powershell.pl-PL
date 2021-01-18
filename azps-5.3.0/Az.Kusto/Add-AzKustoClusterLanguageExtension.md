---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: e1b5a123d00e097e7e6315ac2231b145de645149
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500854"
---
# <span data-ttu-id="da986-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="da986-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="da986-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da986-102">SYNOPSIS</span></span>
<span data-ttu-id="da986-103">Dodaj listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="da986-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="da986-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da986-104">SYNTAX</span></span>

### <span data-ttu-id="da986-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="da986-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da986-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="da986-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da986-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da986-107">DESCRIPTION</span></span>
<span data-ttu-id="da986-108">Dodaj listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="da986-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="da986-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da986-109">EXAMPLES</span></span>

### <span data-ttu-id="da986-110">Przykład 1: Dodawanie listy rozszerzeń języków</span><span class="sxs-lookup"><span data-stu-id="da986-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="da986-111">Powyższe polecenie dodaje listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword</span><span class="sxs-lookup"><span data-stu-id="da986-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="da986-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da986-112">PARAMETERS</span></span>

### <span data-ttu-id="da986-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da986-113">-AsJob</span></span>
<span data-ttu-id="da986-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="da986-114">Run the command as a job</span></span>

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

### <span data-ttu-id="da986-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="da986-115">-ClusterName</span></span>
<span data-ttu-id="da986-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="da986-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="da986-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da986-117">-DefaultProfile</span></span>
<span data-ttu-id="da986-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da986-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da986-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da986-119">-InputObject</span></span>
<span data-ttu-id="da986-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="da986-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da986-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="da986-121">-NoWait</span></span>
<span data-ttu-id="da986-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="da986-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da986-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da986-123">-PassThru</span></span>
<span data-ttu-id="da986-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="da986-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da986-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da986-125">-ResourceGroupName</span></span>
<span data-ttu-id="da986-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="da986-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="da986-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da986-127">-SubscriptionId</span></span>
<span data-ttu-id="da986-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="da986-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="da986-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="da986-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da986-130">-Value</span><span class="sxs-lookup"><span data-stu-id="da986-130">-Value</span></span>
<span data-ttu-id="da986-131">Lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="da986-131">The list of language extensions.</span></span>
<span data-ttu-id="da986-132">Aby skonstruować, zobacz sekcję notatki dla właściwości wartości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="da986-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="da986-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da986-133">-Confirm</span></span>
<span data-ttu-id="da986-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da986-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da986-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da986-135">-WhatIf</span></span>
<span data-ttu-id="da986-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da986-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da986-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da986-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da986-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da986-138">CommonParameters</span></span>
<span data-ttu-id="da986-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da986-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da986-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da986-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da986-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da986-141">INPUTS</span></span>

### <span data-ttu-id="da986-142">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="da986-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="da986-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da986-143">OUTPUTS</span></span>

### <span data-ttu-id="da986-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da986-144">System.Boolean</span></span>

## <span data-ttu-id="da986-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da986-145">NOTES</span></span>

<span data-ttu-id="da986-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="da986-146">ALIASES</span></span>

<span data-ttu-id="da986-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da986-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da986-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="da986-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da986-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da986-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da986-150">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="da986-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da986-151">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="da986-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="da986-152">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="da986-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="da986-153">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="da986-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="da986-154">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="da986-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="da986-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="da986-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da986-156">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da986-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="da986-157">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="da986-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="da986-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="da986-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="da986-159">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="da986-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="da986-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="da986-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="da986-161">WARTOŚĆ <ILanguageExtension [] >: lista rozszerzeń języków.</span><span class="sxs-lookup"><span data-stu-id="da986-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="da986-162">`[Name <LanguageExtensionName?>]`: Nazwa rozszerzenia języka.</span><span class="sxs-lookup"><span data-stu-id="da986-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="da986-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da986-163">RELATED LINKS</span></span>

