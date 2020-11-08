---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233208"
---
# <span data-ttu-id="49521-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="49521-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="49521-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49521-102">SYNOPSIS</span></span>
<span data-ttu-id="49521-103">Operacja usuwania tożsamości maszyny hybrydowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="49521-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="49521-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49521-104">SYNTAX</span></span>

### <span data-ttu-id="49521-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="49521-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49521-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49521-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49521-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49521-107">DESCRIPTION</span></span>
<span data-ttu-id="49521-108">Operacja usuwania tożsamości maszyny hybrydowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="49521-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="49521-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49521-109">EXAMPLES</span></span>

### <span data-ttu-id="49521-110">Przykład 1: usuwanie połączonego komputera</span><span class="sxs-lookup"><span data-stu-id="49521-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="49521-111">Usuwa podłączony komputer.</span><span class="sxs-lookup"><span data-stu-id="49521-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="49521-112">Przykład 2: usuwanie połączonych maszyn za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="49521-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="49521-113">Usuwa wszystkie komputery w `contoso-connected-machines` grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="49521-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="49521-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49521-114">PARAMETERS</span></span>

### <span data-ttu-id="49521-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49521-115">-DefaultProfile</span></span>
<span data-ttu-id="49521-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49521-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49521-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="49521-117">-InputObject</span></span>
<span data-ttu-id="49521-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="49521-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49521-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49521-119">-Name</span></span>
<span data-ttu-id="49521-120">Nazwa maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="49521-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="49521-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49521-121">-PassThru</span></span>
<span data-ttu-id="49521-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="49521-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49521-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49521-123">-ResourceGroupName</span></span>
<span data-ttu-id="49521-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49521-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="49521-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="49521-125">-SubscriptionId</span></span>
<span data-ttu-id="49521-126">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49521-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49521-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="49521-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="49521-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49521-128">-Confirm</span></span>
<span data-ttu-id="49521-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49521-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49521-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49521-130">-WhatIf</span></span>
<span data-ttu-id="49521-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49521-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49521-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49521-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49521-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49521-133">CommonParameters</span></span>
<span data-ttu-id="49521-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49521-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49521-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49521-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49521-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49521-136">INPUTS</span></span>

### <span data-ttu-id="49521-137">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="49521-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="49521-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49521-138">OUTPUTS</span></span>

### <span data-ttu-id="49521-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49521-139">System.Boolean</span></span>

## <span data-ttu-id="49521-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49521-140">NOTES</span></span>

<span data-ttu-id="49521-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="49521-141">ALIASES</span></span>

<span data-ttu-id="49521-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49521-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49521-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="49521-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49521-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49521-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49521-145">INPUTobject <IConnectedMachineIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="49521-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49521-146">`[ExtensionName <String>]`: Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="49521-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="49521-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="49521-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49521-148">`[Name <String>]`: Nazwa maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="49521-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="49521-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49521-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="49521-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49521-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="49521-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="49521-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="49521-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49521-152">RELATED LINKS</span></span>

