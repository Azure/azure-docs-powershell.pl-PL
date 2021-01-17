---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489873"
---
# <span data-ttu-id="e5671-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5671-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="e5671-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5671-102">SYNOPSIS</span></span>
<span data-ttu-id="e5671-103">Usuwanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="e5671-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5671-104">SYNTAX</span></span>

### <span data-ttu-id="e5671-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e5671-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e5671-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5671-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5671-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e5671-107">DESCRIPTION</span></span>
<span data-ttu-id="e5671-108">Usuwanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="e5671-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5671-109">EXAMPLES</span></span>

### <span data-ttu-id="e5671-110">Przykład 1. Usuń azDigitalTwinsEndPoint za pomocą punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e5671-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="e5671-111">Usuwanie azDigitalTwinsEndPoint za pomocą ResourceGroupName i resourceName</span><span class="sxs-lookup"><span data-stu-id="e5671-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="e5671-112">Przykład 2: usuwanie azDigitalTwinsEndPoint przez obiekt</span><span class="sxs-lookup"><span data-stu-id="e5671-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="e5671-113">Usuwanie azDigitalTwinsEndPoint przez obiekt</span><span class="sxs-lookup"><span data-stu-id="e5671-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="e5671-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5671-114">PARAMETERS</span></span>

### <span data-ttu-id="e5671-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5671-115">-AsJob</span></span>
<span data-ttu-id="e5671-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e5671-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e5671-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5671-117">-DefaultProfile</span></span>
<span data-ttu-id="e5671-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5671-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5671-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e5671-119">-EndpointName</span></span>
<span data-ttu-id="e5671-120">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e5671-120">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5671-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5671-121">-InputObject</span></span>
<span data-ttu-id="e5671-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e5671-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5671-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e5671-123">-NoWait</span></span>
<span data-ttu-id="e5671-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e5671-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e5671-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5671-125">-PassThru</span></span>
<span data-ttu-id="e5671-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e5671-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e5671-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5671-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5671-128">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5671-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e5671-129">-ResourceName</span></span>
<span data-ttu-id="e5671-130">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-130">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5671-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e5671-131">-SubscriptionId</span></span>
<span data-ttu-id="e5671-132">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e5671-132">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5671-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5671-133">-Confirm</span></span>
<span data-ttu-id="e5671-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5671-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5671-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5671-135">-WhatIf</span></span>
<span data-ttu-id="e5671-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5671-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5671-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5671-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5671-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5671-138">CommonParameters</span></span>
<span data-ttu-id="e5671-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5671-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5671-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5671-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5671-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5671-141">INPUTS</span></span>

### <span data-ttu-id="e5671-142">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e5671-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e5671-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5671-143">OUTPUTS</span></span>

### <span data-ttu-id="e5671-144">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="e5671-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="e5671-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5671-145">NOTES</span></span>

<span data-ttu-id="e5671-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e5671-146">ALIASES</span></span>

<span data-ttu-id="e5671-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5671-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5671-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e5671-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5671-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5671-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5671-150">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e5671-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5671-151">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e5671-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e5671-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e5671-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5671-153">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e5671-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e5671-155">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e5671-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e5671-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e5671-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e5671-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5671-157">RELATED LINKS</span></span>

