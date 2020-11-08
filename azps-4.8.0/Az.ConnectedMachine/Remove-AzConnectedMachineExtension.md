---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063566"
---
# <span data-ttu-id="c2082-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c2082-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="c2082-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2082-102">SYNOPSIS</span></span>
<span data-ttu-id="c2082-103">Operacja usunięcia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c2082-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="c2082-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2082-104">SYNTAX</span></span>

### <span data-ttu-id="c2082-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c2082-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c2082-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c2082-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2082-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2082-107">DESCRIPTION</span></span>
<span data-ttu-id="c2082-108">Operacja usunięcia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c2082-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="c2082-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2082-109">EXAMPLES</span></span>

### <span data-ttu-id="c2082-110">Przykład 1: Usuwanie rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="c2082-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="c2082-111">Usuwa rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="c2082-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="c2082-112">Przykład 2: Usuwanie rozszerzenia za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="c2082-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="c2082-113">Usuwa wszystkie rozszerzenia określonego komputera.</span><span class="sxs-lookup"><span data-stu-id="c2082-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="c2082-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2082-114">PARAMETERS</span></span>

### <span data-ttu-id="c2082-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2082-115">-AsJob</span></span>
<span data-ttu-id="c2082-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c2082-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c2082-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2082-117">-DefaultProfile</span></span>
<span data-ttu-id="c2082-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2082-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2082-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2082-119">-InputObject</span></span>
<span data-ttu-id="c2082-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c2082-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2082-121">-NazwaKomputera</span><span class="sxs-lookup"><span data-stu-id="c2082-121">-MachineName</span></span>
<span data-ttu-id="c2082-122">Nazwa komputera, na którym należy usunąć rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="c2082-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="c2082-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2082-123">-Name</span></span>
<span data-ttu-id="c2082-124">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="c2082-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="c2082-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c2082-125">-NoWait</span></span>
<span data-ttu-id="c2082-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c2082-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c2082-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2082-127">-PassThru</span></span>
<span data-ttu-id="c2082-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="c2082-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c2082-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2082-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2082-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2082-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2082-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c2082-131">-SubscriptionId</span></span>
<span data-ttu-id="c2082-132">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2082-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2082-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c2082-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c2082-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2082-134">-Confirm</span></span>
<span data-ttu-id="c2082-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2082-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2082-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2082-136">-WhatIf</span></span>
<span data-ttu-id="c2082-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2082-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2082-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2082-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2082-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2082-139">CommonParameters</span></span>
<span data-ttu-id="c2082-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2082-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2082-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2082-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2082-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2082-142">INPUTS</span></span>

### <span data-ttu-id="c2082-143">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="c2082-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="c2082-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2082-144">OUTPUTS</span></span>

### <span data-ttu-id="c2082-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2082-145">System.Boolean</span></span>

## <span data-ttu-id="c2082-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2082-146">NOTES</span></span>

<span data-ttu-id="c2082-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c2082-147">ALIASES</span></span>

<span data-ttu-id="c2082-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2082-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2082-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c2082-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2082-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2082-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2082-151">INPUTobject <IConnectedMachineIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c2082-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2082-152">`[ExtensionName <String>]`: Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="c2082-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="c2082-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c2082-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2082-154">`[Name <String>]`: Nazwa maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="c2082-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="c2082-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2082-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c2082-156">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2082-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c2082-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c2082-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c2082-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2082-158">RELATED LINKS</span></span>

