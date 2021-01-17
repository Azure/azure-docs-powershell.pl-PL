---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/start-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
ms.openlocfilehash: bdda5653a3b7f612fc96d3522bffe15e92649bbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360311"
---
# <span data-ttu-id="7b56c-101">Start-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="7b56c-101">Start-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="7b56c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b56c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b56c-103">Uruchamia serwer.</span><span class="sxs-lookup"><span data-stu-id="7b56c-103">Starts a server.</span></span>

## <span data-ttu-id="7b56c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b56c-104">SYNTAX</span></span>

### <span data-ttu-id="7b56c-105">Początek (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7b56c-105">Start (Default)</span></span>
```
Start-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b56c-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b56c-106">StartViaIdentity</span></span>
```
Start-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b56c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7b56c-107">DESCRIPTION</span></span>
<span data-ttu-id="7b56c-108">Uruchamia serwer.</span><span class="sxs-lookup"><span data-stu-id="7b56c-108">Starts a server.</span></span>

## <span data-ttu-id="7b56c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b56c-109">EXAMPLES</span></span>

### <span data-ttu-id="7b56c-110">Przykład 1. Uruchom serwer według nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="7b56c-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="7b56c-111">Uruchamianie serwera za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="7b56c-111">Start the server by name</span></span>

### <span data-ttu-id="7b56c-112">Przykład 2: uruchamianie serwera za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="7b56c-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/start"
PS C:\> Start-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="7b56c-113">Uruchamianie serwera za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="7b56c-113">Start the server by identity</span></span>

## <span data-ttu-id="7b56c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b56c-114">PARAMETERS</span></span>

### <span data-ttu-id="7b56c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b56c-115">-AsJob</span></span>
<span data-ttu-id="7b56c-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7b56c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7b56c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b56c-117">-DefaultProfile</span></span>
<span data-ttu-id="7b56c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b56c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b56c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b56c-119">-InputObject</span></span>
<span data-ttu-id="7b56c-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7b56c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b56c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b56c-121">-Name</span></span>
<span data-ttu-id="7b56c-122">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7b56c-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b56c-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7b56c-123">-NoWait</span></span>
<span data-ttu-id="7b56c-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7b56c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7b56c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b56c-125">-PassThru</span></span>
<span data-ttu-id="7b56c-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="7b56c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7b56c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b56c-127">-ResourceGroupName</span></span>
<span data-ttu-id="7b56c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b56c-128">The name of the resource group.</span></span>
<span data-ttu-id="7b56c-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7b56c-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b56c-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7b56c-130">-SubscriptionId</span></span>
<span data-ttu-id="7b56c-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7b56c-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b56c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b56c-132">-Confirm</span></span>
<span data-ttu-id="7b56c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b56c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b56c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b56c-134">-WhatIf</span></span>
<span data-ttu-id="7b56c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b56c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b56c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b56c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b56c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b56c-137">CommonParameters</span></span>
<span data-ttu-id="7b56c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b56c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b56c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b56c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b56c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b56c-140">INPUTS</span></span>

### <span data-ttu-id="7b56c-141">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7b56c-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7b56c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b56c-142">OUTPUTS</span></span>

### <span data-ttu-id="7b56c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b56c-143">System.Boolean</span></span>

## <span data-ttu-id="7b56c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b56c-144">NOTES</span></span>

<span data-ttu-id="7b56c-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7b56c-145">ALIASES</span></span>

<span data-ttu-id="7b56c-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b56c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b56c-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7b56c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b56c-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b56c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b56c-149">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7b56c-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b56c-150">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="7b56c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7b56c-151">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7b56c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7b56c-152">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="7b56c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7b56c-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7b56c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b56c-154">`[KeyName <String>]`: Nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="7b56c-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="7b56c-155">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7b56c-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7b56c-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b56c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7b56c-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7b56c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="7b56c-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7b56c-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7b56c-159">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="7b56c-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7b56c-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7b56c-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7b56c-161">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7b56c-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7b56c-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b56c-162">RELATED LINKS</span></span>

