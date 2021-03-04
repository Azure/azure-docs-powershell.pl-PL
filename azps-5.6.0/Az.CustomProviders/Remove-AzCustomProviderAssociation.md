---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 6d3a6863044722be49efb78a71e3e0fbe82db5e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998754"
---
# <span data-ttu-id="275eb-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="275eb-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="275eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275eb-102">SYNOPSIS</span></span>
<span data-ttu-id="275eb-103">Usuwanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-103">Delete an association.</span></span>

## <span data-ttu-id="275eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="275eb-104">SYNTAX</span></span>

### <span data-ttu-id="275eb-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="275eb-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="275eb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="275eb-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="275eb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="275eb-107">DESCRIPTION</span></span>
<span data-ttu-id="275eb-108">Usuwanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-108">Delete an association.</span></span>

## <span data-ttu-id="275eb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="275eb-109">EXAMPLES</span></span>

### <span data-ttu-id="275eb-110">Przykład 1. Usuwanie niestandardowego skojarzenia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="275eb-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="275eb-111">Usuwanie niestandardowego skojarzenia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="275eb-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="275eb-112">Przykład 2. Usuwanie niestandardowego skojarzenia dostawcy z usługą Piping</span><span class="sxs-lookup"><span data-stu-id="275eb-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="275eb-113">Usuwanie niestandardowego skojarzenia dostawców za pomocą funkcji rurowych i funkcji PassThru w celu wskazania sukcesu lub niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="275eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="275eb-114">PARAMETERS</span></span>

### <span data-ttu-id="275eb-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="275eb-115">-AsJob</span></span>
<span data-ttu-id="275eb-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="275eb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="275eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275eb-117">-DefaultProfile</span></span>
<span data-ttu-id="275eb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="275eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="275eb-119">-InputObject</span></span>
<span data-ttu-id="275eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="275eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="275eb-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="275eb-121">-Name</span></span>
<span data-ttu-id="275eb-122">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275eb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="275eb-123">-NoWait</span></span>
<span data-ttu-id="275eb-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="275eb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="275eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="275eb-125">-PassThru</span></span>
<span data-ttu-id="275eb-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="275eb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="275eb-127">— Zakres</span><span class="sxs-lookup"><span data-stu-id="275eb-127">-Scope</span></span>
<span data-ttu-id="275eb-128">Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-128">The scope of the association.</span></span>

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

### <span data-ttu-id="275eb-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="275eb-129">-Confirm</span></span>
<span data-ttu-id="275eb-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="275eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275eb-131">-WhatIf</span></span>
<span data-ttu-id="275eb-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275eb-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="275eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275eb-134">CommonParameters</span></span>
<span data-ttu-id="275eb-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275eb-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="275eb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275eb-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275eb-137">INPUTS</span></span>

### <span data-ttu-id="275eb-138">Microsoft.Azure.PowerShell.Cmdlet.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="275eb-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="275eb-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275eb-139">OUTPUTS</span></span>

### <span data-ttu-id="275eb-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="275eb-140">System.Boolean</span></span>

## <span data-ttu-id="275eb-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="275eb-141">NOTES</span></span>

<span data-ttu-id="275eb-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="275eb-142">ALIASES</span></span>

<span data-ttu-id="275eb-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="275eb-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="275eb-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="275eb-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="275eb-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="275eb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="275eb-146">INPUTOBJECT: <ICustomProvidersIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="275eb-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="275eb-147">`[AssociationName <String>]`: nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="275eb-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="275eb-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="275eb-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="275eb-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="275eb-150">`[ResourceProviderName <String>]`: nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="275eb-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="275eb-151">`[Scope <String>]`: zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="275eb-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="275eb-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="275eb-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="275eb-153">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="275eb-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="275eb-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="275eb-154">RELATED LINKS</span></span>

