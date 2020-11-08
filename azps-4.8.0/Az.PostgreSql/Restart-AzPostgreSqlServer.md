---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219311"
---
# <span data-ttu-id="90cd3-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="90cd3-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="90cd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="90cd3-103">Ponowne uruchamianie serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-103">Restarts a server.</span></span>

## <span data-ttu-id="90cd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90cd3-104">SYNTAX</span></span>

### <span data-ttu-id="90cd3-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="90cd3-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90cd3-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90cd3-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90cd3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="90cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="90cd3-108">Ponowne uruchamianie serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-108">Restarts a server.</span></span>

## <span data-ttu-id="90cd3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="90cd3-110">Przykład 1: ponowne uruchomienie serwera PostgreSql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="90cd3-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="90cd3-111">To polecenie cmdlet ponownie uruchamia PostgreSql serwera według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="90cd3-112">Przykład 2: ponowne uruchomienie PostgreSql serwera za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="90cd3-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="90cd3-113">Te polecenia cmdlet ponownie uruchamiają PostgreSql serwer po tożsamości.</span><span class="sxs-lookup"><span data-stu-id="90cd3-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="90cd3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90cd3-114">PARAMETERS</span></span>

### <span data-ttu-id="90cd3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90cd3-115">-AsJob</span></span>
<span data-ttu-id="90cd3-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="90cd3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="90cd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90cd3-117">-DefaultProfile</span></span>
<span data-ttu-id="90cd3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90cd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90cd3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90cd3-119">-InputObject</span></span>
<span data-ttu-id="90cd3-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="90cd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90cd3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90cd3-121">-Name</span></span>
<span data-ttu-id="90cd3-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cd3-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="90cd3-123">-NoWait</span></span>
<span data-ttu-id="90cd3-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="90cd3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90cd3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90cd3-125">-PassThru</span></span>
<span data-ttu-id="90cd3-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="90cd3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="90cd3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90cd3-127">-ResourceGroupName</span></span>
<span data-ttu-id="90cd3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90cd3-128">The name of the resource group.</span></span>
<span data-ttu-id="90cd3-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="90cd3-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cd3-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="90cd3-130">-SubscriptionId</span></span>
<span data-ttu-id="90cd3-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="90cd3-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cd3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90cd3-132">-Confirm</span></span>
<span data-ttu-id="90cd3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90cd3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90cd3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90cd3-134">-WhatIf</span></span>
<span data-ttu-id="90cd3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90cd3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90cd3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90cd3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90cd3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90cd3-137">CommonParameters</span></span>
<span data-ttu-id="90cd3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90cd3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90cd3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90cd3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90cd3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90cd3-140">INPUTS</span></span>

### <span data-ttu-id="90cd3-141">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="90cd3-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="90cd3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90cd3-142">OUTPUTS</span></span>

### <span data-ttu-id="90cd3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90cd3-143">System.Boolean</span></span>

## <span data-ttu-id="90cd3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90cd3-144">NOTES</span></span>

<span data-ttu-id="90cd3-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="90cd3-145">ALIASES</span></span>

<span data-ttu-id="90cd3-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90cd3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90cd3-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="90cd3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90cd3-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90cd3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90cd3-149">INPUTobject <IPostgreSqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="90cd3-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90cd3-150">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="90cd3-151">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="90cd3-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="90cd3-152">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="90cd3-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="90cd3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90cd3-154">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="90cd3-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="90cd3-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90cd3-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="90cd3-156">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="90cd3-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="90cd3-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="90cd3-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="90cd3-158">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="90cd3-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="90cd3-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="90cd3-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="90cd3-160">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90cd3-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="90cd3-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90cd3-161">RELATED LINKS</span></span>

