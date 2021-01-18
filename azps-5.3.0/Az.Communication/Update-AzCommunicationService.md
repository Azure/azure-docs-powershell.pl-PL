---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504163"
---
# <span data-ttu-id="3e979-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="3e979-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="3e979-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e979-102">SYNOPSIS</span></span>
<span data-ttu-id="3e979-103">Operacja aktualizowania istniejącego CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3e979-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="3e979-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e979-104">SYNTAX</span></span>

### <span data-ttu-id="3e979-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e979-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e979-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3e979-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e979-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e979-107">DESCRIPTION</span></span>
<span data-ttu-id="3e979-108">Operacja aktualizowania istniejącego CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3e979-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="3e979-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e979-109">EXAMPLES</span></span>

### <span data-ttu-id="3e979-110">Przykład 1. Uaktualnij istniejący zasób ACS, aby miał Tagi</span><span class="sxs-lookup"><span data-stu-id="3e979-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="3e979-111">Dołącza podane znaczniki do określonego zasobu ACS.</span><span class="sxs-lookup"><span data-stu-id="3e979-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="3e979-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e979-112">PARAMETERS</span></span>

### <span data-ttu-id="3e979-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e979-113">-DefaultProfile</span></span>
<span data-ttu-id="3e979-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e979-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e979-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e979-115">-InputObject</span></span>
<span data-ttu-id="3e979-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3e979-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e979-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e979-117">-Name</span></span>
<span data-ttu-id="3e979-118">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3e979-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e979-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e979-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e979-120">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="3e979-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3e979-121">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3e979-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e979-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3e979-122">-SubscriptionId</span></span>
<span data-ttu-id="3e979-123">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e979-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e979-124">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3e979-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e979-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e979-125">-Tag</span></span>
<span data-ttu-id="3e979-126">Tagi usługi, która jest listą par wartości klucza opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="3e979-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e979-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e979-127">-Confirm</span></span>
<span data-ttu-id="3e979-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e979-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e979-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e979-129">-WhatIf</span></span>
<span data-ttu-id="3e979-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e979-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e979-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e979-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e979-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e979-132">CommonParameters</span></span>
<span data-ttu-id="3e979-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e979-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e979-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e979-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e979-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e979-135">INPUTS</span></span>

### <span data-ttu-id="3e979-136">Microsoft. Azure. PowerShell. cmdlet. Communication. models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="3e979-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="3e979-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e979-137">OUTPUTS</span></span>

### <span data-ttu-id="3e979-138">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="3e979-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="3e979-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e979-139">NOTES</span></span>

<span data-ttu-id="3e979-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3e979-140">ALIASES</span></span>

<span data-ttu-id="3e979-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e979-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e979-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3e979-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e979-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e979-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e979-144">INPUTobject <ICommunicationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3e979-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e979-145">`[CommunicationServiceName <String>]`: Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3e979-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="3e979-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3e979-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e979-147">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3e979-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="3e979-148">`[OperationId <String>]`: Identyfikator trwającej operacji asynchronicznej</span><span class="sxs-lookup"><span data-stu-id="3e979-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="3e979-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="3e979-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3e979-150">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3e979-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3e979-151">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e979-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3e979-152">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3e979-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3e979-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e979-153">RELATED LINKS</span></span>

