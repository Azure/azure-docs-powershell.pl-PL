---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324310"
---
# <span data-ttu-id="cd5bd-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="cd5bd-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="cd5bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5bd-103">Usuwa określony dedykowany HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="cd5bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd5bd-104">SYNTAX</span></span>

### <span data-ttu-id="cd5bd-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cd5bd-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd5bd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd5bd-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd5bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd5bd-107">DESCRIPTION</span></span>
<span data-ttu-id="cd5bd-108">Usuwa określony dedykowany HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="cd5bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd5bd-109">EXAMPLES</span></span>

### <span data-ttu-id="cd5bd-110">Przykład 1: usuwanie dedykowanego modułu HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="cd5bd-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="cd5bd-111">Ta commnad usuwa sprzętowy moduł zabezpieczeń (HSM) według nazwy.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="cd5bd-112">Przykład 2: usuwanie dedykowanego modułu HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="cd5bd-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="cd5bd-113">Ten commnad usuwa dedykowany obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="cd5bd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd5bd-114">PARAMETERS</span></span>

### <span data-ttu-id="cd5bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd5bd-115">-AsJob</span></span>
<span data-ttu-id="cd5bd-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="cd5bd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cd5bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5bd-117">-DefaultProfile</span></span>
<span data-ttu-id="cd5bd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5bd-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd5bd-119">-InputObject</span></span>
<span data-ttu-id="cd5bd-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5bd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd5bd-121">-Name</span></span>
<span data-ttu-id="cd5bd-122">Nazwa dedykowanego modułu HSM do usunięcia</span><span class="sxs-lookup"><span data-stu-id="cd5bd-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="cd5bd-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cd5bd-123">-NoWait</span></span>
<span data-ttu-id="cd5bd-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="cd5bd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd5bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd5bd-125">-PassThru</span></span>
<span data-ttu-id="cd5bd-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd5bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd5bd-128">Nazwa grupy zasobów, do której należy dedykowany HSM.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="cd5bd-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cd5bd-129">-SubscriptionId</span></span>
<span data-ttu-id="cd5bd-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd5bd-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd5bd-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd5bd-132">-Confirm</span></span>
<span data-ttu-id="cd5bd-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd5bd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd5bd-134">-WhatIf</span></span>
<span data-ttu-id="cd5bd-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd5bd-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd5bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5bd-137">CommonParameters</span></span>
<span data-ttu-id="cd5bd-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5bd-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd5bd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5bd-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd5bd-140">INPUTS</span></span>

### <span data-ttu-id="cd5bd-141">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="cd5bd-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="cd5bd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd5bd-142">OUTPUTS</span></span>

### <span data-ttu-id="cd5bd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd5bd-143">System.Boolean</span></span>

## <span data-ttu-id="cd5bd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd5bd-144">NOTES</span></span>

<span data-ttu-id="cd5bd-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="cd5bd-145">ALIASES</span></span>

<span data-ttu-id="cd5bd-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd5bd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd5bd-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd5bd-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd5bd-149">INPUTobject <IDedicatedHsmIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="cd5bd-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd5bd-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cd5bd-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd5bd-151">`[Name <String>]`: Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="cd5bd-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="cd5bd-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="cd5bd-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cd5bd-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cd5bd-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cd5bd-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd5bd-155">RELATED LINKS</span></span>

