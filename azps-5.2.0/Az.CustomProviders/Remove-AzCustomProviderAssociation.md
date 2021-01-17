---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330745"
---
# <span data-ttu-id="f35ef-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="f35ef-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="f35ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f35ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f35ef-103">Usuwanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="f35ef-103">Delete an association.</span></span>

## <span data-ttu-id="f35ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f35ef-104">SYNTAX</span></span>

### <span data-ttu-id="f35ef-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f35ef-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f35ef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f35ef-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f35ef-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f35ef-107">DESCRIPTION</span></span>
<span data-ttu-id="f35ef-108">Usuwanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="f35ef-108">Delete an association.</span></span>

## <span data-ttu-id="f35ef-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f35ef-109">EXAMPLES</span></span>

### <span data-ttu-id="f35ef-110">Przykład 1: Usunięcie skojarzenia dostawcy niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="f35ef-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="f35ef-111">Usuwanie skojarzenia dostawcy niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="f35ef-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="f35ef-112">Przykład 2: Usuwanie niestandardowego skojarzenia dostawcy za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="f35ef-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="f35ef-113">Usuń skojarzenie dostawcy niestandardowego przy użyciu instalacji rurowej i funkcji PassThru, aby wskazać sukces lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="f35ef-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="f35ef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f35ef-114">PARAMETERS</span></span>

### <span data-ttu-id="f35ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f35ef-115">-AsJob</span></span>
<span data-ttu-id="f35ef-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f35ef-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f35ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f35ef-117">-DefaultProfile</span></span>
<span data-ttu-id="f35ef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f35ef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f35ef-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f35ef-119">-InputObject</span></span>
<span data-ttu-id="f35ef-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f35ef-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f35ef-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f35ef-121">-Name</span></span>
<span data-ttu-id="f35ef-122">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="f35ef-122">The name of the association.</span></span>

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

### <span data-ttu-id="f35ef-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f35ef-123">-NoWait</span></span>
<span data-ttu-id="f35ef-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f35ef-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f35ef-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f35ef-125">-PassThru</span></span>
<span data-ttu-id="f35ef-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="f35ef-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f35ef-127">-Zakres</span><span class="sxs-lookup"><span data-stu-id="f35ef-127">-Scope</span></span>
<span data-ttu-id="f35ef-128">Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="f35ef-128">The scope of the association.</span></span>

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

### <span data-ttu-id="f35ef-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f35ef-129">-Confirm</span></span>
<span data-ttu-id="f35ef-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f35ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f35ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f35ef-131">-WhatIf</span></span>
<span data-ttu-id="f35ef-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f35ef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f35ef-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f35ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f35ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f35ef-134">CommonParameters</span></span>
<span data-ttu-id="f35ef-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f35ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f35ef-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f35ef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f35ef-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f35ef-137">INPUTS</span></span>

### <span data-ttu-id="f35ef-138">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="f35ef-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="f35ef-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f35ef-139">OUTPUTS</span></span>

### <span data-ttu-id="f35ef-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f35ef-140">System.Boolean</span></span>

## <span data-ttu-id="f35ef-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f35ef-141">NOTES</span></span>

<span data-ttu-id="f35ef-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f35ef-142">ALIASES</span></span>

<span data-ttu-id="f35ef-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f35ef-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f35ef-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f35ef-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f35ef-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f35ef-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f35ef-146">INPUTobject <ICustomProvidersIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f35ef-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f35ef-147">`[AssociationName <String>]`: Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="f35ef-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="f35ef-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f35ef-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f35ef-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f35ef-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f35ef-150">`[ResourceProviderName <String>]`: Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f35ef-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="f35ef-151">`[Scope <String>]`: Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="f35ef-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="f35ef-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f35ef-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="f35ef-153">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="f35ef-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="f35ef-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f35ef-154">RELATED LINKS</span></span>

