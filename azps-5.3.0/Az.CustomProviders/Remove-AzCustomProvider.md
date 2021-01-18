---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503757"
---
# <span data-ttu-id="a6bc3-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a6bc3-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="a6bc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bc3-103">Usuwa niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="a6bc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6bc3-104">SYNTAX</span></span>

### <span data-ttu-id="a6bc3-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a6bc3-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6bc3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6bc3-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6bc3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a6bc3-107">DESCRIPTION</span></span>
<span data-ttu-id="a6bc3-108">Usuwa niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="a6bc3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6bc3-109">EXAMPLES</span></span>

### <span data-ttu-id="a6bc3-110">Przykład 1. Usuń dostawcę niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="a6bc3-111">Usuwanie dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="a6bc3-111">Remove a custom provider</span></span>

### <span data-ttu-id="a6bc3-112">Przykład 2: Usuwanie niestandardowego dostawcy z PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bc3-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="a6bc3-113">Usuń dostawcę niestandardowego przy użyciu funkcji PassThru, aby wskazać sukces lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="a6bc3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6bc3-114">PARAMETERS</span></span>

### <span data-ttu-id="a6bc3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6bc3-115">-AsJob</span></span>
<span data-ttu-id="a6bc3-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a6bc3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a6bc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bc3-117">-DefaultProfile</span></span>
<span data-ttu-id="a6bc3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bc3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6bc3-119">-InputObject</span></span>
<span data-ttu-id="a6bc3-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6bc3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6bc3-121">-Name</span></span>
<span data-ttu-id="a6bc3-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6bc3-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a6bc3-123">-NoWait</span></span>
<span data-ttu-id="a6bc3-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a6bc3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6bc3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bc3-125">-PassThru</span></span>
<span data-ttu-id="a6bc3-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6bc3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bc3-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6bc3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6bc3-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a6bc3-129">-SubscriptionId</span></span>
<span data-ttu-id="a6bc3-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-130">The Azure subscription ID.</span></span>
<span data-ttu-id="a6bc3-131">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a6bc3-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a6bc3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6bc3-132">-Confirm</span></span>
<span data-ttu-id="a6bc3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bc3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bc3-134">-WhatIf</span></span>
<span data-ttu-id="a6bc3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bc3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bc3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bc3-137">CommonParameters</span></span>
<span data-ttu-id="a6bc3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bc3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6bc3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bc3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6bc3-140">INPUTS</span></span>

### <span data-ttu-id="a6bc3-141">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="a6bc3-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a6bc3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6bc3-142">OUTPUTS</span></span>

### <span data-ttu-id="a6bc3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6bc3-143">System.Boolean</span></span>

## <span data-ttu-id="a6bc3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6bc3-144">NOTES</span></span>

<span data-ttu-id="a6bc3-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a6bc3-145">ALIASES</span></span>

<span data-ttu-id="a6bc3-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6bc3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6bc3-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6bc3-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6bc3-149">INPUTobject <ICustomProvidersIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a6bc3-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6bc3-150">`[AssociationName <String>]`: Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a6bc3-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a6bc3-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6bc3-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a6bc3-153">`[ResourceProviderName <String>]`: Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a6bc3-154">`[Scope <String>]`: Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a6bc3-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bc3-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a6bc3-156">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a6bc3-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a6bc3-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6bc3-157">RELATED LINKS</span></span>

