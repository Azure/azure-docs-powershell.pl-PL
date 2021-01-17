---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346930"
---
# <span data-ttu-id="83895-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="83895-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="83895-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83895-102">SYNOPSIS</span></span>
<span data-ttu-id="83895-103">Sprawdź, czy nazwa DigitalTwinsInstance jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="83895-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="83895-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83895-104">SYNTAX</span></span>

### <span data-ttu-id="83895-105">CheckExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83895-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83895-106">Wyszukaj</span><span class="sxs-lookup"><span data-stu-id="83895-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83895-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83895-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="83895-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83895-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83895-109">Opis</span><span class="sxs-lookup"><span data-stu-id="83895-109">DESCRIPTION</span></span>
<span data-ttu-id="83895-110">Sprawdź, czy nazwa DigitalTwinsInstance jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="83895-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="83895-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83895-111">EXAMPLES</span></span>

### <span data-ttu-id="83895-112">Przykład 1. Sprawdź nazwę według lokalizacji i nazwy.</span><span class="sxs-lookup"><span data-stu-id="83895-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="83895-113">Sprawdź dostępność nazwy według lokalizacji i nazwy.</span><span class="sxs-lookup"><span data-stu-id="83895-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="83895-114">Przykład 2: Sprawdź nazwy według DigitalTwinsObject i CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="83895-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="83895-115">Pobierz DigitalTwinsInstance i Utwórz obiekt Requset, aby przetestować dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="83895-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="83895-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83895-116">PARAMETERS</span></span>

### <span data-ttu-id="83895-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83895-117">-DefaultProfile</span></span>
<span data-ttu-id="83895-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83895-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83895-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="83895-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="83895-120">Wynik zwrócony przez bazę danych sprawdza żądanie uzyskania dostępu do nazwy.</span><span class="sxs-lookup"><span data-stu-id="83895-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="83895-121">Aby skonstruować, zobacz sekcję notatki dla właściwości DIGITALTWINSINSTANCECHECKNAME i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="83895-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

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

### <span data-ttu-id="83895-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83895-122">-InputObject</span></span>
<span data-ttu-id="83895-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="83895-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83895-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="83895-124">-Location</span></span>
<span data-ttu-id="83895-125">Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83895-125">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="83895-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83895-126">-Name</span></span>
<span data-ttu-id="83895-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="83895-127">Resource name.</span></span>

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

### <span data-ttu-id="83895-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="83895-128">-SubscriptionId</span></span>
<span data-ttu-id="83895-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83895-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="83895-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83895-130">-Confirm</span></span>
<span data-ttu-id="83895-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83895-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83895-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83895-132">-WhatIf</span></span>
<span data-ttu-id="83895-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83895-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83895-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83895-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83895-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83895-135">CommonParameters</span></span>
<span data-ttu-id="83895-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83895-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83895-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83895-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83895-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83895-138">INPUTS</span></span>

### <span data-ttu-id="83895-139">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="83895-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="83895-140">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="83895-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="83895-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83895-141">OUTPUTS</span></span>

### <span data-ttu-id="83895-142">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="83895-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="83895-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83895-143">NOTES</span></span>

<span data-ttu-id="83895-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="83895-144">ALIASES</span></span>

<span data-ttu-id="83895-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83895-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83895-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="83895-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83895-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83895-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83895-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest> : wynik zwrócony przez bazę danych sprawdza żądanie uzyskania dostępu do nazwy.</span><span class="sxs-lookup"><span data-stu-id="83895-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="83895-149">`Name <String>`: Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="83895-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="83895-150">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="83895-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83895-151">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="83895-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="83895-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="83895-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83895-153">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83895-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="83895-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83895-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="83895-155">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83895-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="83895-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83895-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="83895-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83895-157">RELATED LINKS</span></span>

