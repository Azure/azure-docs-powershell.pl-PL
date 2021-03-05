---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: d33f092bc72f480766ed81de66abbe1e001dfa42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984915"
---
# <span data-ttu-id="4d4d0-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4d4d0-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="4d4d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4d0-103">Sprawdź, czy jest dostępna nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="4d4d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d4d0-104">SYNTAX</span></span>

### <span data-ttu-id="4d4d0-105">CheckExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="4d4d0-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d4d0-106">Sprawdź</span><span class="sxs-lookup"><span data-stu-id="4d4d0-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d4d0-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d4d0-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4d4d0-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4d4d0-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d4d0-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d4d0-109">DESCRIPTION</span></span>
<span data-ttu-id="4d4d0-110">Sprawdź, czy jest dostępna nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="4d4d0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d4d0-111">EXAMPLES</span></span>

### <span data-ttu-id="4d4d0-112">Przykład 1. Sprawdź nazwę według lokalizacji i nazwy.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="4d4d0-113">Sprawdź dostępność nazwy według lokalizacji i nazwy.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="4d4d0-114">Przykład 2. Sprawdź nazwę pola DigitalTwinsObject i CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="4d4d0-115">Uzyskaj usługę DigitalTwinsInstance i utwórz obiekt Requset, aby sprawdzić dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="4d4d0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d4d0-116">PARAMETERS</span></span>

### <span data-ttu-id="4d4d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4d0-117">-DefaultProfile</span></span>
<span data-ttu-id="4d4d0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4d0-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="4d4d0-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="4d4d0-120">Wynik zwrócony z żądania dostępności nazwy sprawdzania nazwy bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="4d4d0-121">Aby skonstruować, zobacz sekcję NOTES dla właściwości DIGITALTWINSINSTANCECHECKNAME i utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4d0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d4d0-122">-InputObject</span></span>
<span data-ttu-id="4d4d0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4d0-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4d4d0-124">-Location</span></span>
<span data-ttu-id="4d4d0-125">Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4d0-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4d4d0-126">-Name</span></span>
<span data-ttu-id="4d4d0-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4d0-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d4d0-128">-SubscriptionId</span></span>
<span data-ttu-id="4d4d0-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4d0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d4d0-130">-Confirm</span></span>
<span data-ttu-id="4d4d0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d4d0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d4d0-132">-WhatIf</span></span>
<span data-ttu-id="4d4d0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d4d0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d4d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4d0-135">CommonParameters</span></span>
<span data-ttu-id="4d4d0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4d0-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d4d0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4d0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d4d0-138">INPUTS</span></span>

### <span data-ttu-id="4d4d0-139">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="4d4d0-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="4d4d0-140">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="4d4d0-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="4d4d0-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d4d0-141">OUTPUTS</span></span>

### <span data-ttu-id="4d4d0-142">Microsoft.Azure.PowerShell.cmdlet.DigitalTwins.Models.Api20201031.iCheckNameResult</span><span class="sxs-lookup"><span data-stu-id="4d4d0-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="4d4d0-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d4d0-143">NOTES</span></span>

<span data-ttu-id="4d4d0-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4d4d0-144">ALIASES</span></span>

<span data-ttu-id="4d4d0-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d4d0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d4d0-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d4d0-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d4d0-148">DIGITALTWINSINSTANCECHECKNAME: Wynik zwrócony z żądania dostępności <ICheckNameRequest> nazwy sprawdzania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="4d4d0-149">`Name <String>`: nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="4d4d0-150">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4d4d0-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d4d0-151">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="4d4d0-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4d4d0-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d4d0-153">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4d4d0-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4d4d0-155">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4d4d0-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4d4d0-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4d4d0-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d4d0-157">RELATED LINKS</span></span>

