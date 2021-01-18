---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 12e43eeb22151df8569e068933036fe29749ed1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501477"
---
# <span data-ttu-id="8716a-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="8716a-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="8716a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8716a-102">SYNOPSIS</span></span>
<span data-ttu-id="8716a-103">Usuwanie uprawnień podmiotów zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="8716a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8716a-104">SYNTAX</span></span>

### <span data-ttu-id="8716a-105">RemoveExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8716a-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8716a-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8716a-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8716a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8716a-107">DESCRIPTION</span></span>
<span data-ttu-id="8716a-108">Usuwanie uprawnień podmiotów zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="8716a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8716a-109">EXAMPLES</span></span>

### <span data-ttu-id="8716a-110">Przykład 1: usuwanie uprawnień podmiotów zabezpieczeń bazy danych</span><span class="sxs-lookup"><span data-stu-id="8716a-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="8716a-111">Powyższe polecenie usuwa uprawnienia podmiotów zabezpieczeń bazy danych</span><span class="sxs-lookup"><span data-stu-id="8716a-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="8716a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8716a-112">PARAMETERS</span></span>

### <span data-ttu-id="8716a-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="8716a-113">-ClusterName</span></span>
<span data-ttu-id="8716a-114">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8716a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8716a-115">-DatabaseName</span></span>
<span data-ttu-id="8716a-116">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="8716a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8716a-117">-DefaultProfile</span></span>
<span data-ttu-id="8716a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8716a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8716a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8716a-119">-InputObject</span></span>
<span data-ttu-id="8716a-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8716a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8716a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8716a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8716a-122">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8716a-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8716a-123">-SubscriptionId</span></span>
<span data-ttu-id="8716a-124">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8716a-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8716a-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8716a-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8716a-126">-Value</span><span class="sxs-lookup"><span data-stu-id="8716a-126">-Value</span></span>
<span data-ttu-id="8716a-127">Lista podmiotów Kusto bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="8716a-128">Aby skonstruować, zobacz sekcję notatki dla właściwości wartości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8716a-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="8716a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8716a-129">-Confirm</span></span>
<span data-ttu-id="8716a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8716a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8716a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8716a-131">-WhatIf</span></span>
<span data-ttu-id="8716a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8716a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8716a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8716a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8716a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8716a-134">CommonParameters</span></span>
<span data-ttu-id="8716a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8716a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8716a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8716a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8716a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8716a-137">INPUTS</span></span>

### <span data-ttu-id="8716a-138">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8716a-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8716a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8716a-139">OUTPUTS</span></span>

### <span data-ttu-id="8716a-140">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="8716a-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="8716a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8716a-141">NOTES</span></span>

<span data-ttu-id="8716a-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8716a-142">ALIASES</span></span>

<span data-ttu-id="8716a-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8716a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8716a-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8716a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8716a-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8716a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8716a-146">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8716a-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8716a-147">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8716a-148">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8716a-149">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8716a-150">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8716a-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8716a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8716a-152">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8716a-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8716a-153">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8716a-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8716a-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8716a-155">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8716a-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8716a-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8716a-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="8716a-157">WARTOŚĆ <IDatabasePrincipal [] >: Lista podmiotów zabezpieczeń bazy Kusto.</span><span class="sxs-lookup"><span data-stu-id="8716a-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="8716a-158">`Name <String>`: Główna nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="8716a-159">`Role <DatabasePrincipalRole>`: Rola główna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="8716a-160">`Type <DatabasePrincipalType>`: Typ podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="8716a-161">`[AppId <String>]`: Identyfikator aplikacji — dotyczy tylko typu głównego aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8716a-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="8716a-162">`[Email <String>]`: Główna wiadomość e-mail bazy danych, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="8716a-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="8716a-163">`[Fqn <String>]`: Główna w pełni kwalifikowana nazwa podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8716a-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="8716a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8716a-164">RELATED LINKS</span></span>

