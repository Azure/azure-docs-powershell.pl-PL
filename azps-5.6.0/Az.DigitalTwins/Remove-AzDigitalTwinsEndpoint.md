---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: f7d8b5665ff150e0501d77a76c2dde7e4a947cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984929"
---
# <span data-ttu-id="2171f-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="2171f-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="2171f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2171f-102">SYNOPSIS</span></span>
<span data-ttu-id="2171f-103">Usuwanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="2171f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2171f-104">SYNTAX</span></span>

### <span data-ttu-id="2171f-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="2171f-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2171f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2171f-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2171f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2171f-107">DESCRIPTION</span></span>
<span data-ttu-id="2171f-108">Usuwanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="2171f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2171f-109">EXAMPLES</span></span>

### <span data-ttu-id="2171f-110">Przykład 1. Usunięcie pliku azDigitalTwinsEndPoint według nazwy programu EndPointName</span><span class="sxs-lookup"><span data-stu-id="2171f-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="2171f-111">Usuwanie pliku azDigitalTwinsEndPoint według wartości EndPointName ResourceGroupName i ResourceName</span><span class="sxs-lookup"><span data-stu-id="2171f-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="2171f-112">Przykład 2. Usunięcie obiektu azDigitalTwinsEndPoint według obiektu</span><span class="sxs-lookup"><span data-stu-id="2171f-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="2171f-113">Usuwanie obiektu azDigitalTwinsEndPoint według obiektu</span><span class="sxs-lookup"><span data-stu-id="2171f-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="2171f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2171f-114">PARAMETERS</span></span>

### <span data-ttu-id="2171f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2171f-115">-AsJob</span></span>
<span data-ttu-id="2171f-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2171f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2171f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2171f-117">-DefaultProfile</span></span>
<span data-ttu-id="2171f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2171f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2171f-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2171f-119">-EndpointName</span></span>
<span data-ttu-id="2171f-120">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2171f-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="2171f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2171f-121">-InputObject</span></span>
<span data-ttu-id="2171f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2171f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2171f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2171f-123">-NoWait</span></span>
<span data-ttu-id="2171f-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2171f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2171f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2171f-125">-PassThru</span></span>
<span data-ttu-id="2171f-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="2171f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2171f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2171f-127">-ResourceGroupName</span></span>
<span data-ttu-id="2171f-128">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="2171f-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2171f-129">-ResourceName</span></span>
<span data-ttu-id="2171f-130">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="2171f-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2171f-131">-SubscriptionId</span></span>
<span data-ttu-id="2171f-132">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2171f-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="2171f-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2171f-133">-Confirm</span></span>
<span data-ttu-id="2171f-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2171f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2171f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2171f-135">-WhatIf</span></span>
<span data-ttu-id="2171f-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2171f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2171f-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2171f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2171f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2171f-138">CommonParameters</span></span>
<span data-ttu-id="2171f-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2171f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2171f-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2171f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2171f-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2171f-141">INPUTS</span></span>

### <span data-ttu-id="2171f-142">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="2171f-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="2171f-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2171f-143">OUTPUTS</span></span>

### <span data-ttu-id="2171f-144">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="2171f-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="2171f-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2171f-145">NOTES</span></span>

<span data-ttu-id="2171f-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2171f-146">ALIASES</span></span>

<span data-ttu-id="2171f-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2171f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2171f-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2171f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2171f-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2171f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2171f-150">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="2171f-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2171f-151">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2171f-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="2171f-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2171f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2171f-153">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2171f-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2171f-155">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2171f-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2171f-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2171f-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="2171f-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2171f-157">RELATED LINKS</span></span>

