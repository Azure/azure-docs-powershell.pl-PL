---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1cbc4b8274a619514268e8412f7f9123a5e9e58a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202186"
---
# <span data-ttu-id="d569d-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="d569d-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="d569d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d569d-102">SYNOPSIS</span></span>
<span data-ttu-id="d569d-103">Testowanie połączenia z serwerem bazy danych</span><span class="sxs-lookup"><span data-stu-id="d569d-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="d569d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d569d-104">SYNTAX</span></span>

### <span data-ttu-id="d569d-105">Test (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d569d-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d569d-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="d569d-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d569d-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d569d-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d569d-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="d569d-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d569d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d569d-109">DESCRIPTION</span></span>
<span data-ttu-id="d569d-110">Testowanie połączenia z serwerem bazy danych</span><span class="sxs-lookup"><span data-stu-id="d569d-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="d569d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d569d-111">EXAMPLES</span></span>

### <span data-ttu-id="d569d-112">Przykład 1. Testowanie połączenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="d569d-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="d569d-113">Testowanie połączenia przez grupę zasobów i nazwę serwera</span><span class="sxs-lookup"><span data-stu-id="d569d-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="d569d-114">Przykład 2. Testowanie połączenia według tożsamości</span><span class="sxs-lookup"><span data-stu-id="d569d-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="d569d-115">Testowanie połączenia za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="d569d-115">Test connection by the identity</span></span>

### <span data-ttu-id="d569d-116">Przykład 3. Testowanie zapytania według nazwy</span><span class="sxs-lookup"><span data-stu-id="d569d-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="d569d-117">Testowanie zapytania według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="d569d-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="d569d-118">Przykład 4. Testowanie połączenia według tożsamości</span><span class="sxs-lookup"><span data-stu-id="d569d-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="d569d-119">Testowanie zapytania według tożsamości</span><span class="sxs-lookup"><span data-stu-id="d569d-119">Test a query by the identity</span></span>

## <span data-ttu-id="d569d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d569d-120">PARAMETERS</span></span>

### <span data-ttu-id="d569d-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d569d-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d569d-122">Hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="d569d-122">The password of the administrator.</span></span>
<span data-ttu-id="d569d-123">Minimalna liczba znaków: 8 i maksymalnie 128 znaków.</span><span class="sxs-lookup"><span data-stu-id="d569d-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="d569d-124">Hasło musi zawierać znaki z trzech z następujących kategorii: angielskie wielkie litery, angielskie małe litery, cyfry i znaki niealalnumeryczne.</span><span class="sxs-lookup"><span data-stu-id="d569d-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="d569d-125">-AdministratorUserName</span></span>
<span data-ttu-id="d569d-126">Nazwa użytkownika administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="d569d-126">Administrator username for the server.</span></span>
<span data-ttu-id="d569d-127">Po jej skonfigurowaniu nie będzie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="d569d-127">Once set, it cannot be changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d569d-128">-DatabaseName</span></span>
<span data-ttu-id="d569d-129">Nazwa bazy danych do połączenia.</span><span class="sxs-lookup"><span data-stu-id="d569d-129">The database name to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d569d-130">-DefaultProfile</span></span>
<span data-ttu-id="d569d-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d569d-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d569d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d569d-132">-InputObject</span></span>
<span data-ttu-id="d569d-133">Serwer, z którym ma nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="d569d-133">The server to connect.</span></span>
<span data-ttu-id="d569d-134">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="d569d-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d569d-135">-Name</span></span>
<span data-ttu-id="d569d-136">Nazwa serwera, na którym ma nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="d569d-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="d569d-137">-QueryText</span></span>
<span data-ttu-id="d569d-138">Zapytanie do przetestowania bazy danych</span><span class="sxs-lookup"><span data-stu-id="d569d-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d569d-139">-ResourceGroupName</span></span>
<span data-ttu-id="d569d-140">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d569d-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d569d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d569d-141">CommonParameters</span></span>
<span data-ttu-id="d569d-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d569d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d569d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d569d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d569d-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d569d-144">INPUTS</span></span>

### <span data-ttu-id="d569d-145">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d569d-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d569d-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d569d-146">OUTPUTS</span></span>

### <span data-ttu-id="d569d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d569d-147">System.String</span></span>

## <span data-ttu-id="d569d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d569d-148">NOTES</span></span>

<span data-ttu-id="d569d-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d569d-149">ALIASES</span></span>

<span data-ttu-id="d569d-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d569d-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d569d-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d569d-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d569d-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d569d-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d569d-153">INPUTOBJECT: <IPostgreSqlIdentity> Serwer do nawiązania połączenia.</span><span class="sxs-lookup"><span data-stu-id="d569d-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="d569d-154">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="d569d-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d569d-155">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d569d-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d569d-156">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="d569d-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d569d-157">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d569d-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d569d-158">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d569d-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d569d-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d569d-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d569d-160">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="d569d-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="d569d-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="d569d-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d569d-162">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="d569d-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d569d-163">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d569d-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d569d-164">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d569d-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d569d-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d569d-165">RELATED LINKS</span></span>

