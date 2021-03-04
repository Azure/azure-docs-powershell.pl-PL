---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c01d481b5ee9351de0b099a144a709c89a3990ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964577"
---
# <span data-ttu-id="f4cc6-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f4cc6-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f4cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cc6-103">Dodawanie uprawnień głównych użytkowników bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="f4cc6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4cc6-104">SYNTAX</span></span>

### <span data-ttu-id="f4cc6-105">AddExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="f4cc6-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f4cc6-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f4cc6-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4cc6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4cc6-107">DESCRIPTION</span></span>
<span data-ttu-id="f4cc6-108">Dodawanie uprawnień głównych użytkowników bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="f4cc6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4cc6-109">EXAMPLES</span></span>

### <span data-ttu-id="f4cc6-110">Przykład 1. Dodawanie uprawnień głównych użytkowników bazy danych</span><span class="sxs-lookup"><span data-stu-id="f4cc6-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f4cc6-111">Powyższe polecenie dodaje uprawnienia głównych użytkowników bazy danych</span><span class="sxs-lookup"><span data-stu-id="f4cc6-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="f4cc6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4cc6-112">PARAMETERS</span></span>

### <span data-ttu-id="f4cc6-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f4cc6-113">-ClusterName</span></span>
<span data-ttu-id="f4cc6-114">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f4cc6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4cc6-115">-DatabaseName</span></span>
<span data-ttu-id="f4cc6-116">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f4cc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cc6-117">-DefaultProfile</span></span>
<span data-ttu-id="f4cc6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4cc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4cc6-119">-InputObject</span></span>
<span data-ttu-id="f4cc6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4cc6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4cc6-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4cc6-122">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f4cc6-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4cc6-123">-SubscriptionId</span></span>
<span data-ttu-id="f4cc6-124">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4cc6-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f4cc6-126">— Wartość</span><span class="sxs-lookup"><span data-stu-id="f4cc6-126">-Value</span></span>
<span data-ttu-id="f4cc6-127">Lista głównych użytkowników bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="f4cc6-128">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WARTOŚCI i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cc6-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4cc6-129">-Confirm</span></span>
<span data-ttu-id="f4cc6-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4cc6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4cc6-131">-WhatIf</span></span>
<span data-ttu-id="f4cc6-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4cc6-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4cc6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cc6-134">CommonParameters</span></span>
<span data-ttu-id="f4cc6-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cc6-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4cc6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cc6-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4cc6-137">INPUTS</span></span>

### <span data-ttu-id="f4cc6-138">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f4cc6-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f4cc6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4cc6-139">OUTPUTS</span></span>

### <span data-ttu-id="f4cc6-140">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f4cc6-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="f4cc6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4cc6-141">NOTES</span></span>

<span data-ttu-id="f4cc6-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f4cc6-142">ALIASES</span></span>

<span data-ttu-id="f4cc6-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4cc6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4cc6-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4cc6-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4cc6-146">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f4cc6-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4cc6-147">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f4cc6-148">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f4cc6-149">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f4cc6-150">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f4cc6-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f4cc6-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4cc6-152">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f4cc6-153">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f4cc6-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f4cc6-155">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4cc6-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f4cc6-157">VALUE <IDatabasePrincipal[]>: Lista głównych podmiotów bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="f4cc6-158">`Name <String>`: główna nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="f4cc6-159">`Role <DatabasePrincipalRole>`: Rola podmiotu bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="f4cc6-160">`Type <DatabasePrincipalType>`: typ podmiotu bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="f4cc6-161">`[AppId <String>]`: Identyfikator aplikacji — odpowiedni tylko dla typu podmiotu zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="f4cc6-162">`[Email <String>]`: Główny adres e-mail bazy danych, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="f4cc6-163">`[Fqn <String>]`: W pełni kwalifikowana nazwa podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f4cc6-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="f4cc6-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4cc6-164">RELATED LINKS</span></span>

