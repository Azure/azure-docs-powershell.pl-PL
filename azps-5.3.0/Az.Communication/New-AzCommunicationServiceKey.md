---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501966"
---
# <span data-ttu-id="c2459-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="c2459-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="c2459-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2459-102">SYNOPSIS</span></span>
<span data-ttu-id="c2459-103">Ponowne generowanie klucza dostępu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c2459-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="c2459-104">PrimaryKey i SecondaryKey nie mogą być ponownie generowane w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="c2459-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="c2459-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2459-105">SYNTAX</span></span>

### <span data-ttu-id="c2459-106">RegenerateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2459-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c2459-107">Ponowne generowanie</span><span class="sxs-lookup"><span data-stu-id="c2459-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2459-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c2459-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2459-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c2459-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2459-110">Opis</span><span class="sxs-lookup"><span data-stu-id="c2459-110">DESCRIPTION</span></span>
<span data-ttu-id="c2459-111">Ponowne generowanie klucza dostępu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c2459-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="c2459-112">PrimaryKey i SecondaryKey nie mogą być ponownie generowane w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="c2459-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="c2459-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2459-113">EXAMPLES</span></span>

### <span data-ttu-id="c2459-114">Przykład 1. regeneruje klucz podstawowy za pomocą IRegenerateKeyParameters Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2459-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="c2459-115">Unieważnia poprzedni klucz podstawowy, ponownie Wygeneruj nowy i zwróci go.</span><span class="sxs-lookup"><span data-stu-id="c2459-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="c2459-116">Przykład 2: generuje ponownie klucz pomocniczy przy użyciu klucza KeyType.</span><span class="sxs-lookup"><span data-stu-id="c2459-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="c2459-117">Unieważnia poprzedni klucz pomocniczy, ponownie Wygeneruj nowy i zwróci go.</span><span class="sxs-lookup"><span data-stu-id="c2459-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="c2459-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2459-118">PARAMETERS</span></span>

### <span data-ttu-id="c2459-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="c2459-119">-CommunicationServiceName</span></span>
<span data-ttu-id="c2459-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c2459-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="c2459-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2459-121">-DefaultProfile</span></span>
<span data-ttu-id="c2459-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2459-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2459-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2459-123">-InputObject</span></span>
<span data-ttu-id="c2459-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c2459-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2459-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c2459-125">-KeyType</span></span>
<span data-ttu-id="c2459-126">Właściwość keyType do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="c2459-126">The keyType to regenerate.</span></span>
<span data-ttu-id="c2459-127">Musi mieć wartość "podstawowy" lub "pomocniczy" (bez uwzględniania wielkości liter).</span><span class="sxs-lookup"><span data-stu-id="c2459-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

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

### <span data-ttu-id="c2459-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c2459-128">-Parameter</span></span>
<span data-ttu-id="c2459-129">Parametry zawiera opis żądania ponownego wygenerowania kluczy dostępu do skonstruowania, zobacz sekcję notatki dla właściwości parametrów i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="c2459-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2459-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2459-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2459-131">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="c2459-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c2459-132">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="c2459-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c2459-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c2459-133">-SubscriptionId</span></span>
<span data-ttu-id="c2459-134">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2459-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2459-135">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c2459-135">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c2459-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2459-136">-Confirm</span></span>
<span data-ttu-id="c2459-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2459-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2459-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2459-138">-WhatIf</span></span>
<span data-ttu-id="c2459-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2459-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2459-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2459-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2459-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2459-141">CommonParameters</span></span>
<span data-ttu-id="c2459-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2459-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2459-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2459-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2459-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2459-144">INPUTS</span></span>

### <span data-ttu-id="c2459-145">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="c2459-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="c2459-146">Microsoft. Azure. PowerShell. cmdlet. Communication. models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="c2459-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="c2459-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2459-147">OUTPUTS</span></span>

### <span data-ttu-id="c2459-148">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="c2459-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="c2459-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2459-149">NOTES</span></span>

<span data-ttu-id="c2459-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c2459-150">ALIASES</span></span>

<span data-ttu-id="c2459-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2459-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2459-152">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c2459-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2459-153">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2459-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2459-154">INPUTobject <ICommunicationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c2459-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2459-155">`[CommunicationServiceName <String>]`: Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c2459-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="c2459-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c2459-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2459-157">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c2459-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="c2459-158">`[OperationId <String>]`: Identyfikator trwającej operacji asynchronicznej</span><span class="sxs-lookup"><span data-stu-id="c2459-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="c2459-159">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="c2459-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c2459-160">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="c2459-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c2459-161">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2459-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c2459-162">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c2459-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="c2459-163">PARAMETR <IRegenerateKeyParameters> : parametry zawiera opis żądania ponownego generowania kluczy dostępu</span><span class="sxs-lookup"><span data-stu-id="c2459-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="c2459-164">`[KeyType <KeyType?>]`: Właściwość keyType, która ma zostać wygenerowana ponownie.</span><span class="sxs-lookup"><span data-stu-id="c2459-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="c2459-165">Musi mieć wartość "podstawowy" lub "pomocniczy" (bez uwzględniania wielkości liter).</span><span class="sxs-lookup"><span data-stu-id="c2459-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="c2459-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2459-166">RELATED LINKS</span></span>

