---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499138"
---
# <span data-ttu-id="1150e-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="1150e-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="1150e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1150e-102">SYNOPSIS</span></span>
<span data-ttu-id="1150e-103">Usuwanie DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="1150e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1150e-104">SYNTAX</span></span>

### <span data-ttu-id="1150e-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1150e-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1150e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1150e-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1150e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1150e-107">DESCRIPTION</span></span>
<span data-ttu-id="1150e-108">Usuwanie DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="1150e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1150e-109">EXAMPLES</span></span>

### <span data-ttu-id="1150e-110">Przykład 1. Usuń AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="1150e-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="1150e-111">To polecenie usuwa AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="1150e-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="1150e-112">Przykład 2: usuwanie AzDigitalTwinsInstance za pomocą obiektu Inputobject</span><span class="sxs-lookup"><span data-stu-id="1150e-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="1150e-113">To polecenie usuwa AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="1150e-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="1150e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1150e-114">PARAMETERS</span></span>

### <span data-ttu-id="1150e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1150e-115">-AsJob</span></span>
<span data-ttu-id="1150e-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1150e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1150e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1150e-117">-DefaultProfile</span></span>
<span data-ttu-id="1150e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1150e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1150e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1150e-119">-InputObject</span></span>
<span data-ttu-id="1150e-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1150e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1150e-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1150e-121">-NoWait</span></span>
<span data-ttu-id="1150e-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1150e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1150e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1150e-123">-PassThru</span></span>
<span data-ttu-id="1150e-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="1150e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1150e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1150e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1150e-126">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="1150e-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1150e-127">-ResourceName</span></span>
<span data-ttu-id="1150e-128">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="1150e-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1150e-129">-SubscriptionId</span></span>
<span data-ttu-id="1150e-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1150e-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="1150e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1150e-131">-Confirm</span></span>
<span data-ttu-id="1150e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1150e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1150e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1150e-133">-WhatIf</span></span>
<span data-ttu-id="1150e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1150e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1150e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1150e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1150e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1150e-136">CommonParameters</span></span>
<span data-ttu-id="1150e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1150e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1150e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1150e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1150e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1150e-139">INPUTS</span></span>

### <span data-ttu-id="1150e-140">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="1150e-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="1150e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1150e-141">OUTPUTS</span></span>

### <span data-ttu-id="1150e-142">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="1150e-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="1150e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1150e-143">NOTES</span></span>

<span data-ttu-id="1150e-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1150e-144">ALIASES</span></span>

<span data-ttu-id="1150e-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1150e-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1150e-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1150e-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1150e-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1150e-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1150e-148">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1150e-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1150e-149">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="1150e-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="1150e-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1150e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1150e-151">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="1150e-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="1150e-153">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1150e-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="1150e-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1150e-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="1150e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1150e-155">RELATED LINKS</span></span>

