---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504168"
---
# <span data-ttu-id="faefd-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="faefd-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="faefd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="faefd-102">SYNOPSIS</span></span>
<span data-ttu-id="faefd-103">Operacja usuwania CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="faefd-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="faefd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="faefd-104">SYNTAX</span></span>

### <span data-ttu-id="faefd-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="faefd-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="faefd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="faefd-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faefd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="faefd-107">DESCRIPTION</span></span>
<span data-ttu-id="faefd-108">Operacja usuwania CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="faefd-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="faefd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="faefd-109">EXAMPLES</span></span>

### <span data-ttu-id="faefd-110">Przykład 1: usuwanie określonego zasobu komunikacyjnego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="faefd-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="faefd-111">Usuwanie lub usuwanie zasobu komunikacyjnego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="faefd-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="faefd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="faefd-112">PARAMETERS</span></span>

### <span data-ttu-id="faefd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faefd-113">-AsJob</span></span>
<span data-ttu-id="faefd-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="faefd-114">Run the command as a job</span></span>

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

### <span data-ttu-id="faefd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faefd-115">-DefaultProfile</span></span>
<span data-ttu-id="faefd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="faefd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faefd-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="faefd-117">-InputObject</span></span>
<span data-ttu-id="faefd-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="faefd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faefd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="faefd-119">-Name</span></span>
<span data-ttu-id="faefd-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="faefd-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faefd-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="faefd-121">-NoWait</span></span>
<span data-ttu-id="faefd-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="faefd-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="faefd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faefd-123">-PassThru</span></span>
<span data-ttu-id="faefd-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="faefd-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="faefd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faefd-125">-ResourceGroupName</span></span>
<span data-ttu-id="faefd-126">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="faefd-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="faefd-127">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="faefd-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="faefd-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="faefd-128">-SubscriptionId</span></span>
<span data-ttu-id="faefd-129">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="faefd-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="faefd-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="faefd-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="faefd-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="faefd-131">-Confirm</span></span>
<span data-ttu-id="faefd-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faefd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faefd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faefd-133">-WhatIf</span></span>
<span data-ttu-id="faefd-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faefd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faefd-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="faefd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faefd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faefd-136">CommonParameters</span></span>
<span data-ttu-id="faefd-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faefd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faefd-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faefd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faefd-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="faefd-139">INPUTS</span></span>

### <span data-ttu-id="faefd-140">Microsoft. Azure. PowerShell. cmdlet. Communication. models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="faefd-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="faefd-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="faefd-141">OUTPUTS</span></span>

### <span data-ttu-id="faefd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="faefd-142">System.Boolean</span></span>

## <span data-ttu-id="faefd-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="faefd-143">NOTES</span></span>

<span data-ttu-id="faefd-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="faefd-144">ALIASES</span></span>

<span data-ttu-id="faefd-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="faefd-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="faefd-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="faefd-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="faefd-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="faefd-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="faefd-148">INPUTobject <ICommunicationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="faefd-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="faefd-149">`[CommunicationServiceName <String>]`: Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="faefd-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="faefd-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="faefd-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="faefd-151">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="faefd-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="faefd-152">`[OperationId <String>]`: Identyfikator trwającej operacji asynchronicznej</span><span class="sxs-lookup"><span data-stu-id="faefd-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="faefd-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="faefd-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="faefd-154">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="faefd-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="faefd-155">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="faefd-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="faefd-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="faefd-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="faefd-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="faefd-157">RELATED LINKS</span></span>

