---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: d7af2877d4823f1da85f08e61035b386d57a9c2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233501"
---
# <span data-ttu-id="91f33-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="91f33-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="91f33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91f33-102">SYNOPSIS</span></span>
<span data-ttu-id="91f33-103">Uprawnienia Dodaj podmioty zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="91f33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91f33-104">SYNTAX</span></span>

### <span data-ttu-id="91f33-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="91f33-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="91f33-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="91f33-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91f33-107">Opis</span><span class="sxs-lookup"><span data-stu-id="91f33-107">DESCRIPTION</span></span>
<span data-ttu-id="91f33-108">Uprawnienia Dodaj podmioty zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="91f33-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91f33-109">EXAMPLES</span></span>

### <span data-ttu-id="91f33-110">Przykład 1: Dodawanie uprawnień podmiotów zabezpieczeń bazy danych</span><span class="sxs-lookup"><span data-stu-id="91f33-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="91f33-111">Powyższe polecenie dodaje uprawnienia podmiotów zabezpieczeń bazy danych</span><span class="sxs-lookup"><span data-stu-id="91f33-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="91f33-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91f33-112">PARAMETERS</span></span>

### <span data-ttu-id="91f33-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="91f33-113">-ClusterName</span></span>
<span data-ttu-id="91f33-114">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="91f33-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91f33-115">-DatabaseName</span></span>
<span data-ttu-id="91f33-116">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="91f33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f33-117">-DefaultProfile</span></span>
<span data-ttu-id="91f33-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91f33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f33-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91f33-119">-InputObject</span></span>
<span data-ttu-id="91f33-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="91f33-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91f33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f33-121">-ResourceGroupName</span></span>
<span data-ttu-id="91f33-122">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="91f33-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="91f33-123">-SubscriptionId</span></span>
<span data-ttu-id="91f33-124">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91f33-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="91f33-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="91f33-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91f33-126">-Value</span><span class="sxs-lookup"><span data-stu-id="91f33-126">-Value</span></span>
<span data-ttu-id="91f33-127">Lista podmiotów Kusto bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="91f33-128">Aby skonstruować, zobacz sekcję notatki dla właściwości wartości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="91f33-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f33-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91f33-129">-Confirm</span></span>
<span data-ttu-id="91f33-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91f33-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f33-131">-WhatIf</span></span>
<span data-ttu-id="91f33-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91f33-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f33-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91f33-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f33-134">CommonParameters</span></span>
<span data-ttu-id="91f33-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f33-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91f33-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f33-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91f33-137">INPUTS</span></span>

### <span data-ttu-id="91f33-138">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="91f33-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="91f33-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91f33-139">OUTPUTS</span></span>

### <span data-ttu-id="91f33-140">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="91f33-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="91f33-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91f33-141">NOTES</span></span>

<span data-ttu-id="91f33-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="91f33-142">ALIASES</span></span>

<span data-ttu-id="91f33-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91f33-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91f33-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="91f33-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91f33-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91f33-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91f33-146">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="91f33-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91f33-147">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="91f33-148">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="91f33-149">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="91f33-150">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="91f33-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="91f33-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91f33-152">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="91f33-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="91f33-153">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="91f33-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="91f33-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="91f33-155">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91f33-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="91f33-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="91f33-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="91f33-157">WARTOŚĆ <IDatabasePrincipal [] >: Lista podmiotów zabezpieczeń bazy Kusto.</span><span class="sxs-lookup"><span data-stu-id="91f33-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="91f33-158">`Name <String>`: Główna nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="91f33-159">`Role <DatabasePrincipalRole>`: Rola główna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="91f33-160">`Type <DatabasePrincipalType>`: Typ podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="91f33-161">`[AppId <String>]`: Identyfikator aplikacji — dotyczy tylko typu głównego aplikacji.</span><span class="sxs-lookup"><span data-stu-id="91f33-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="91f33-162">`[Email <String>]`: Główna wiadomość e-mail bazy danych, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="91f33-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="91f33-163">`[Fqn <String>]`: Główna w pełni kwalifikowana nazwa podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91f33-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="91f33-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91f33-164">RELATED LINKS</span></span>

