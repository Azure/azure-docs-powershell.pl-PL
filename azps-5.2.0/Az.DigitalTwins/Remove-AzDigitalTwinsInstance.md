---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346969"
---
# <span data-ttu-id="5ba6a-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5ba6a-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="5ba6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ba6a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba6a-103">Usuwanie DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5ba6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ba6a-104">SYNTAX</span></span>

### <span data-ttu-id="5ba6a-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5ba6a-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ba6a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ba6a-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ba6a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ba6a-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba6a-108">Usuwanie DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5ba6a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ba6a-109">EXAMPLES</span></span>

### <span data-ttu-id="5ba6a-110">Przykład 1. Usuń AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="5ba6a-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="5ba6a-111">To polecenie usuwa AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="5ba6a-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="5ba6a-112">Przykład 2: usuwanie AzDigitalTwinsInstance za pomocą obiektu Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ba6a-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="5ba6a-113">To polecenie usuwa AzDigitalTwinsInstance według nazwy</span><span class="sxs-lookup"><span data-stu-id="5ba6a-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="5ba6a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba6a-114">PARAMETERS</span></span>

### <span data-ttu-id="5ba6a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ba6a-115">-AsJob</span></span>
<span data-ttu-id="5ba6a-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5ba6a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5ba6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba6a-117">-DefaultProfile</span></span>
<span data-ttu-id="5ba6a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba6a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ba6a-119">-InputObject</span></span>
<span data-ttu-id="5ba6a-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ba6a-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5ba6a-121">-NoWait</span></span>
<span data-ttu-id="5ba6a-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5ba6a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ba6a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ba6a-123">-PassThru</span></span>
<span data-ttu-id="5ba6a-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ba6a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba6a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5ba6a-126">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5ba6a-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5ba6a-127">-ResourceName</span></span>
<span data-ttu-id="5ba6a-128">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5ba6a-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5ba6a-129">-SubscriptionId</span></span>
<span data-ttu-id="5ba6a-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="5ba6a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ba6a-131">-Confirm</span></span>
<span data-ttu-id="5ba6a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba6a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba6a-133">-WhatIf</span></span>
<span data-ttu-id="5ba6a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba6a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba6a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba6a-136">CommonParameters</span></span>
<span data-ttu-id="5ba6a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba6a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ba6a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba6a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba6a-139">INPUTS</span></span>

### <span data-ttu-id="5ba6a-140">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="5ba6a-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="5ba6a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ba6a-141">OUTPUTS</span></span>

### <span data-ttu-id="5ba6a-142">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="5ba6a-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="5ba6a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ba6a-143">NOTES</span></span>

<span data-ttu-id="5ba6a-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5ba6a-144">ALIASES</span></span>

<span data-ttu-id="5ba6a-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba6a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ba6a-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ba6a-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ba6a-148">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="5ba6a-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ba6a-149">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="5ba6a-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5ba6a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ba6a-151">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5ba6a-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5ba6a-153">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5ba6a-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5ba6a-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="5ba6a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba6a-155">RELATED LINKS</span></span>

