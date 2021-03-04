---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: dcc402b2db390403a6106953b3ecbdd6cc52a2b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954577"
---
# <span data-ttu-id="d1a86-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d1a86-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="d1a86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a86-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a86-103">Sprawdza, czy nazwa klastra jest prawidłowa i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="d1a86-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="d1a86-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1a86-104">SYNTAX</span></span>

### <span data-ttu-id="d1a86-105">CheckExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="d1a86-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1a86-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1a86-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1a86-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1a86-107">DESCRIPTION</span></span>
<span data-ttu-id="d1a86-108">Sprawdza, czy nazwa klastra jest prawidłowa i nie jest już w użyciu.</span><span class="sxs-lookup"><span data-stu-id="d1a86-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="d1a86-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1a86-109">EXAMPLES</span></span>

### <span data-ttu-id="d1a86-110">Przykład 1. Sprawdzanie dostępności nazwa klastra Kusto, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="d1a86-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="d1a86-111">Powyższe polecenie zwraca, czy w regionie "Wschód US" istnieje klaster Kusto o nazwie "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="d1a86-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="d1a86-112">Przykład 2. Sprawdzanie dostępności nazwy klastra Kusto, która nie jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="d1a86-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="d1a86-113">Powyższe polecenie zwraca, czy w regionie "Wschód US" istnieje klaster Kusto o nazwie "availablekustocluster".</span><span class="sxs-lookup"><span data-stu-id="d1a86-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="d1a86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a86-114">PARAMETERS</span></span>

### <span data-ttu-id="d1a86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a86-115">-DefaultProfile</span></span>
<span data-ttu-id="d1a86-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a86-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1a86-117">-InputObject</span></span>
<span data-ttu-id="d1a86-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d1a86-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a86-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d1a86-119">-Location</span></span>
<span data-ttu-id="d1a86-120">Lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a86-120">Azure location.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a86-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1a86-121">-Name</span></span>
<span data-ttu-id="d1a86-122">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="d1a86-122">Cluster name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a86-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1a86-123">-SubscriptionId</span></span>
<span data-ttu-id="d1a86-124">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a86-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d1a86-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d1a86-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a86-126">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d1a86-126">-Type</span></span>
<span data-ttu-id="d1a86-127">Typ zasobu, Microsoft.Kusto/clusters.</span><span class="sxs-lookup"><span data-stu-id="d1a86-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a86-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1a86-128">-Confirm</span></span>
<span data-ttu-id="d1a86-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1a86-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a86-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a86-130">-WhatIf</span></span>
<span data-ttu-id="d1a86-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a86-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a86-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1a86-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a86-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a86-133">CommonParameters</span></span>
<span data-ttu-id="d1a86-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a86-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a86-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1a86-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a86-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1a86-136">INPUTS</span></span>

### <span data-ttu-id="d1a86-137">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d1a86-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d1a86-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1a86-138">OUTPUTS</span></span>

### <span data-ttu-id="d1a86-139">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iCheckNameResult</span><span class="sxs-lookup"><span data-stu-id="d1a86-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="d1a86-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1a86-140">NOTES</span></span>

<span data-ttu-id="d1a86-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d1a86-141">ALIASES</span></span>

<span data-ttu-id="d1a86-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1a86-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1a86-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d1a86-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1a86-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1a86-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1a86-145">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d1a86-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1a86-146">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d1a86-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d1a86-147">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1a86-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d1a86-148">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="d1a86-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d1a86-149">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1a86-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d1a86-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d1a86-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1a86-151">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a86-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d1a86-152">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="d1a86-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d1a86-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1a86-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d1a86-154">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a86-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d1a86-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d1a86-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d1a86-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1a86-156">RELATED LINKS</span></span>

