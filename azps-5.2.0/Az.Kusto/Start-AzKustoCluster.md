---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350914"
---
# <span data-ttu-id="2d473-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="2d473-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="2d473-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d473-102">SYNOPSIS</span></span>
<span data-ttu-id="2d473-103">Uruchamia klaster programu Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="2d473-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d473-104">SYNTAX</span></span>

### <span data-ttu-id="2d473-105">Początek (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2d473-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d473-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2d473-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d473-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2d473-107">DESCRIPTION</span></span>
<span data-ttu-id="2d473-108">Uruchamia klaster programu Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="2d473-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d473-109">EXAMPLES</span></span>

### <span data-ttu-id="2d473-110">Przykład 1. Uruchom klaster programu Kusto</span><span class="sxs-lookup"><span data-stu-id="2d473-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="2d473-111">Powyższe polecenie uruchamia klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="2d473-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d473-112">PARAMETERS</span></span>

### <span data-ttu-id="2d473-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d473-113">-AsJob</span></span>
<span data-ttu-id="2d473-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2d473-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2d473-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d473-115">-DefaultProfile</span></span>
<span data-ttu-id="2d473-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d473-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d473-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d473-117">-InputObject</span></span>
<span data-ttu-id="2d473-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2d473-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d473-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d473-119">-Name</span></span>
<span data-ttu-id="2d473-120">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d473-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2d473-121">-NoWait</span></span>
<span data-ttu-id="2d473-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2d473-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2d473-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d473-123">-PassThru</span></span>
<span data-ttu-id="2d473-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2d473-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2d473-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d473-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d473-126">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2d473-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2d473-127">-SubscriptionId</span></span>
<span data-ttu-id="2d473-128">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d473-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d473-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2d473-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2d473-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d473-130">-Confirm</span></span>
<span data-ttu-id="2d473-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d473-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d473-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d473-132">-WhatIf</span></span>
<span data-ttu-id="2d473-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d473-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d473-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d473-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d473-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d473-135">CommonParameters</span></span>
<span data-ttu-id="2d473-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d473-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d473-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d473-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d473-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d473-138">INPUTS</span></span>

### <span data-ttu-id="2d473-139">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2d473-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2d473-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d473-140">OUTPUTS</span></span>

### <span data-ttu-id="2d473-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d473-141">System.Boolean</span></span>

## <span data-ttu-id="2d473-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d473-142">NOTES</span></span>

<span data-ttu-id="2d473-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2d473-143">ALIASES</span></span>

<span data-ttu-id="2d473-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d473-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d473-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2d473-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d473-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2d473-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d473-147">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2d473-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d473-148">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2d473-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2d473-149">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2d473-150">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="2d473-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2d473-151">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2d473-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2d473-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d473-153">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d473-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2d473-154">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2d473-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2d473-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="2d473-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2d473-156">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d473-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2d473-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2d473-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2d473-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d473-158">RELATED LINKS</span></span>

