---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350926"
---
# <span data-ttu-id="a39ce-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a39ce-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="a39ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a39ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ce-103">Sprawdza, czy nazwa klastra jest prawidłowa i nie jest jeszcze używana.</span><span class="sxs-lookup"><span data-stu-id="a39ce-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="a39ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a39ce-104">SYNTAX</span></span>

### <span data-ttu-id="a39ce-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a39ce-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a39ce-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a39ce-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a39ce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a39ce-107">DESCRIPTION</span></span>
<span data-ttu-id="a39ce-108">Sprawdza, czy nazwa klastra jest prawidłowa i nie jest jeszcze używana.</span><span class="sxs-lookup"><span data-stu-id="a39ce-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="a39ce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a39ce-109">EXAMPLES</span></span>

### <span data-ttu-id="a39ce-110">Przykład 1: Sprawdzanie dostępności nazwy klastra usługi Kusto, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="a39ce-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="a39ce-111">Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "testnewkustocluster" istnieje w regionie "Wschodnie USA".</span><span class="sxs-lookup"><span data-stu-id="a39ce-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="a39ce-112">Przykład 2: Sprawdzanie dostępności nazwy klastra Kusto, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="a39ce-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="a39ce-113">Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "availablekustocluster" istnieje w regionie "Wschodnie USA".</span><span class="sxs-lookup"><span data-stu-id="a39ce-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="a39ce-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a39ce-114">PARAMETERS</span></span>

### <span data-ttu-id="a39ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ce-115">-DefaultProfile</span></span>
<span data-ttu-id="a39ce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a39ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39ce-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a39ce-117">-InputObject</span></span>
<span data-ttu-id="a39ce-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a39ce-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a39ce-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a39ce-119">-Location</span></span>
<span data-ttu-id="a39ce-120">Lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a39ce-120">Azure location.</span></span>

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

### <span data-ttu-id="a39ce-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a39ce-121">-Name</span></span>
<span data-ttu-id="a39ce-122">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="a39ce-122">Cluster name.</span></span>

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

### <span data-ttu-id="a39ce-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a39ce-123">-SubscriptionId</span></span>
<span data-ttu-id="a39ce-124">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a39ce-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a39ce-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a39ce-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a39ce-126">-Type</span><span class="sxs-lookup"><span data-stu-id="a39ce-126">-Type</span></span>
<span data-ttu-id="a39ce-127">Typ zasobu, Microsoft. Kusto/klastrów.</span><span class="sxs-lookup"><span data-stu-id="a39ce-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="a39ce-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a39ce-128">-Confirm</span></span>
<span data-ttu-id="a39ce-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39ce-130">-WhatIf</span></span>
<span data-ttu-id="a39ce-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39ce-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a39ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ce-133">CommonParameters</span></span>
<span data-ttu-id="a39ce-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ce-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a39ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ce-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a39ce-136">INPUTS</span></span>

### <span data-ttu-id="a39ce-137">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a39ce-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a39ce-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a39ce-138">OUTPUTS</span></span>

### <span data-ttu-id="a39ce-139">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="a39ce-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="a39ce-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a39ce-140">NOTES</span></span>

<span data-ttu-id="a39ce-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a39ce-141">ALIASES</span></span>

<span data-ttu-id="a39ce-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a39ce-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a39ce-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a39ce-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a39ce-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a39ce-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a39ce-145">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a39ce-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a39ce-146">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a39ce-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a39ce-147">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a39ce-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a39ce-148">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="a39ce-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a39ce-149">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a39ce-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a39ce-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a39ce-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a39ce-151">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a39ce-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a39ce-152">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a39ce-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a39ce-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a39ce-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a39ce-154">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a39ce-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a39ce-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a39ce-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a39ce-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a39ce-156">RELATED LINKS</span></span>

