---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188507"
---
# <span data-ttu-id="1a3fc-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="1a3fc-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="1a3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3fc-103">Usuń plik DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="1a3fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a3fc-104">SYNTAX</span></span>

### <span data-ttu-id="1a3fc-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="1a3fc-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1a3fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1a3fc-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a3fc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a3fc-107">DESCRIPTION</span></span>
<span data-ttu-id="1a3fc-108">Usuń plik DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="1a3fc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a3fc-109">EXAMPLES</span></span>

### <span data-ttu-id="1a3fc-110">Przykład 1. Usunięcie pola AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="1a3fc-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="1a3fc-111">To polecenie usuwa element AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="1a3fc-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="1a3fc-112">Przykład 2. Usuwanie pola AzDigitalTwinsInstance przez inputObject</span><span class="sxs-lookup"><span data-stu-id="1a3fc-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="1a3fc-113">To polecenie usuwa element AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="1a3fc-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="1a3fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a3fc-114">PARAMETERS</span></span>

### <span data-ttu-id="1a3fc-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1a3fc-115">-AsJob</span></span>
<span data-ttu-id="1a3fc-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1a3fc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1a3fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3fc-117">-DefaultProfile</span></span>
<span data-ttu-id="1a3fc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a3fc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a3fc-119">-InputObject</span></span>
<span data-ttu-id="1a3fc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1a3fc-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a3fc-121">-NoWait</span></span>
<span data-ttu-id="1a3fc-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1a3fc-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a3fc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a3fc-123">-PassThru</span></span>
<span data-ttu-id="1a3fc-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1a3fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a3fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a3fc-126">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="1a3fc-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1a3fc-127">-ResourceName</span></span>
<span data-ttu-id="1a3fc-128">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="1a3fc-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a3fc-129">-SubscriptionId</span></span>
<span data-ttu-id="1a3fc-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="1a3fc-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a3fc-131">-Confirm</span></span>
<span data-ttu-id="1a3fc-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a3fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a3fc-133">-WhatIf</span></span>
<span data-ttu-id="1a3fc-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a3fc-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a3fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3fc-136">CommonParameters</span></span>
<span data-ttu-id="1a3fc-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3fc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a3fc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3fc-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a3fc-139">INPUTS</span></span>

### <span data-ttu-id="1a3fc-140">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="1a3fc-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="1a3fc-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a3fc-141">OUTPUTS</span></span>

### <span data-ttu-id="1a3fc-142">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="1a3fc-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="1a3fc-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a3fc-143">NOTES</span></span>

<span data-ttu-id="1a3fc-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1a3fc-144">ALIASES</span></span>

<span data-ttu-id="1a3fc-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a3fc-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1a3fc-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a3fc-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1a3fc-148">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="1a3fc-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a3fc-149">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="1a3fc-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1a3fc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a3fc-151">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="1a3fc-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="1a3fc-153">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="1a3fc-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="1a3fc-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a3fc-155">RELATED LINKS</span></span>

