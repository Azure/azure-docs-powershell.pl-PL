---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: 4b9186265287c52c27cff6cb1a7f0d0570949e76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991614"
---
# <span data-ttu-id="56b0d-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="56b0d-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="56b0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="56b0d-103">Generuj ponownie klucz dostępu usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="56b0d-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="56b0d-104">KluczPodstawowy i Klucz Pomocniczy nie można ponownie wygenerować jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="56b0d-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="56b0d-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56b0d-105">SYNTAX</span></span>

### <span data-ttu-id="56b0d-106">Generuj ponownieRozwiń (domyślne)</span><span class="sxs-lookup"><span data-stu-id="56b0d-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="56b0d-107">Generuj ponownie</span><span class="sxs-lookup"><span data-stu-id="56b0d-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56b0d-108">Generuj generujViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56b0d-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56b0d-109">Generuj generujViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="56b0d-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56b0d-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="56b0d-110">DESCRIPTION</span></span>
<span data-ttu-id="56b0d-111">Generuj ponownie klucz dostępu usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="56b0d-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="56b0d-112">KluczPodstawowy i Klucz Pomocniczy nie można ponownie wygenerować jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="56b0d-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="56b0d-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56b0d-113">EXAMPLES</span></span>

### <span data-ttu-id="56b0d-114">Przykład 1. Ponowne generowanie klucza podstawowego przy użyciu skrótu IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="56b0d-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="56b0d-115">Unieważnia poprzedni klucz podstawowy, ponownie generuj nowy klucz i zwraca go.</span><span class="sxs-lookup"><span data-stu-id="56b0d-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="56b0d-116">Przykład 2. Ponowne generowanie klucza pomocniczego przy użyciu typu klucza</span><span class="sxs-lookup"><span data-stu-id="56b0d-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="56b0d-117">Unieważnia poprzedni klucz pomocniczy, ponownie generuj nowy klucz i zwraca go.</span><span class="sxs-lookup"><span data-stu-id="56b0d-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="56b0d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56b0d-118">PARAMETERS</span></span>

### <span data-ttu-id="56b0d-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="56b0d-119">-CommunicationServiceName</span></span>
<span data-ttu-id="56b0d-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="56b0d-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b0d-121">-DefaultProfile</span></span>
<span data-ttu-id="56b0d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56b0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b0d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56b0d-123">-InputObject</span></span>
<span data-ttu-id="56b0d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="56b0d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56b0d-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="56b0d-125">-KeyType</span></span>
<span data-ttu-id="56b0d-126">Typ klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="56b0d-126">The keyType to regenerate.</span></span>
<span data-ttu-id="56b0d-127">Musi to być "podstawowy" lub "pomocniczy" (bez uwzględniania liter).</span><span class="sxs-lookup"><span data-stu-id="56b0d-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b0d-128">- Parametr</span><span class="sxs-lookup"><span data-stu-id="56b0d-128">-Parameter</span></span>
<span data-ttu-id="56b0d-129">Parametry opisują żądanie ponownego wygenerowania kluczy dostępu W celu skonstruowania zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach PARAMETRu i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="56b0d-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56b0d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b0d-130">-ResourceGroupName</span></span>
<span data-ttu-id="56b0d-131">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="56b0d-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="56b0d-132">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="56b0d-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b0d-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56b0d-133">-SubscriptionId</span></span>
<span data-ttu-id="56b0d-134">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56b0d-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="56b0d-135">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="56b0d-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b0d-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56b0d-136">-Confirm</span></span>
<span data-ttu-id="56b0d-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56b0d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56b0d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56b0d-138">-WhatIf</span></span>
<span data-ttu-id="56b0d-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b0d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56b0d-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56b0d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56b0d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b0d-141">CommonParameters</span></span>
<span data-ttu-id="56b0d-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b0d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b0d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56b0d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b0d-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56b0d-144">INPUTS</span></span>

### <span data-ttu-id="56b0d-145">Microsoft.Azure.PowerShell.Cmdlet.Communication.Models.Api200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="56b0d-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="56b0d-146">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="56b0d-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="56b0d-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56b0d-147">OUTPUTS</span></span>

### <span data-ttu-id="56b0d-148">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="56b0d-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="56b0d-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56b0d-149">NOTES</span></span>

<span data-ttu-id="56b0d-150">ALIASY</span><span class="sxs-lookup"><span data-stu-id="56b0d-150">ALIASES</span></span>

<span data-ttu-id="56b0d-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56b0d-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56b0d-152">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="56b0d-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56b0d-153">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56b0d-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56b0d-154">INPUTOBJECT: <ICommunicationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="56b0d-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56b0d-155">`[CommunicationServiceName <String>]`: nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="56b0d-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="56b0d-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="56b0d-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56b0d-157">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="56b0d-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="56b0d-158">`[OperationId <String>]`: Identyfikator trwającej operacji synchronizacji</span><span class="sxs-lookup"><span data-stu-id="56b0d-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="56b0d-159">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="56b0d-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="56b0d-160">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="56b0d-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="56b0d-161">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56b0d-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="56b0d-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="56b0d-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="56b0d-163">PARAMETR: <IRegenerateKeyParameters> Parametry opisują żądanie ponownego wygenerowania kluczy dostępu</span><span class="sxs-lookup"><span data-stu-id="56b0d-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="56b0d-164">`[KeyType <KeyType?>]`: typ klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="56b0d-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="56b0d-165">Musi to być "podstawowy" lub "pomocniczy" (bez uwzględniania liter).</span><span class="sxs-lookup"><span data-stu-id="56b0d-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="56b0d-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56b0d-166">RELATED LINKS</span></span>

