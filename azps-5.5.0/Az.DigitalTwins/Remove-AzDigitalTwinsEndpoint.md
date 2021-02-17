---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196363"
---
# <span data-ttu-id="b05a4-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b05a4-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="b05a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b05a4-103">Usuwanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="b05a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b05a4-104">SYNTAX</span></span>

### <span data-ttu-id="b05a4-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="b05a4-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b05a4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b05a4-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b05a4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b05a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b05a4-108">Usuwanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="b05a4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b05a4-109">EXAMPLES</span></span>

### <span data-ttu-id="b05a4-110">Przykład 1. Usunięcie pliku azDigitalTwinsEndPoint według nazwy programu EndPointName</span><span class="sxs-lookup"><span data-stu-id="b05a4-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="b05a4-111">Usuwanie pliku azDigitalTwinsEndPoint według wartości EndPointName ResourceGroupName i ResourceName</span><span class="sxs-lookup"><span data-stu-id="b05a4-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="b05a4-112">Przykład 2. Usunięcie obiektu azDigitalTwinsEndPoint według obiektu</span><span class="sxs-lookup"><span data-stu-id="b05a4-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="b05a4-113">Usuwanie obiektu azDigitalTwinsEndPoint</span><span class="sxs-lookup"><span data-stu-id="b05a4-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="b05a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b05a4-114">PARAMETERS</span></span>

### <span data-ttu-id="b05a4-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b05a4-115">-AsJob</span></span>
<span data-ttu-id="b05a4-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b05a4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b05a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05a4-117">-DefaultProfile</span></span>
<span data-ttu-id="b05a4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b05a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b05a4-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b05a4-119">-EndpointName</span></span>
<span data-ttu-id="b05a4-120">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b05a4-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="b05a4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b05a4-121">-InputObject</span></span>
<span data-ttu-id="b05a4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b05a4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b05a4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b05a4-123">-NoWait</span></span>
<span data-ttu-id="b05a4-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b05a4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b05a4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b05a4-125">-PassThru</span></span>
<span data-ttu-id="b05a4-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b05a4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b05a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b05a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="b05a4-128">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b05a4-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b05a4-129">-ResourceName</span></span>
<span data-ttu-id="b05a4-130">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b05a4-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b05a4-131">-SubscriptionId</span></span>
<span data-ttu-id="b05a4-132">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b05a4-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="b05a4-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b05a4-133">-Confirm</span></span>
<span data-ttu-id="b05a4-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b05a4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b05a4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05a4-135">-WhatIf</span></span>
<span data-ttu-id="b05a4-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b05a4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b05a4-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b05a4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b05a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05a4-138">CommonParameters</span></span>
<span data-ttu-id="b05a4-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05a4-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b05a4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05a4-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b05a4-141">INPUTS</span></span>

### <span data-ttu-id="b05a4-142">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="b05a4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="b05a4-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b05a4-143">OUTPUTS</span></span>

### <span data-ttu-id="b05a4-144">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="b05a4-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="b05a4-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b05a4-145">NOTES</span></span>

<span data-ttu-id="b05a4-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b05a4-146">ALIASES</span></span>

<span data-ttu-id="b05a4-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b05a4-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b05a4-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b05a4-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b05a4-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b05a4-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b05a4-150">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b05a4-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b05a4-151">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b05a4-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="b05a4-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b05a4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b05a4-153">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b05a4-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b05a4-155">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b05a4-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b05a4-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b05a4-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="b05a4-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b05a4-157">RELATED LINKS</span></span>

