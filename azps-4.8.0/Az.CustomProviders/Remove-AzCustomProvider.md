---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224024"
---
# <span data-ttu-id="7ec2d-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="7ec2d-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="7ec2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ec2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec2d-103">Usuwa niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="7ec2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ec2d-104">SYNTAX</span></span>

### <span data-ttu-id="7ec2d-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7ec2d-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ec2d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ec2d-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ec2d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7ec2d-107">DESCRIPTION</span></span>
<span data-ttu-id="7ec2d-108">Usuwa niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="7ec2d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ec2d-109">EXAMPLES</span></span>

### <span data-ttu-id="7ec2d-110">Przykład 1. Usuń dostawcę niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="7ec2d-111">Usuwanie dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="7ec2d-111">Remove a custom provider</span></span>

### <span data-ttu-id="7ec2d-112">Przykład 2: Usuwanie niestandardowego dostawcy z PassThru</span><span class="sxs-lookup"><span data-stu-id="7ec2d-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="7ec2d-113">Usuń dostawcę niestandardowego przy użyciu funkcji PassThru, aby wskazać sukces lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="7ec2d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ec2d-114">PARAMETERS</span></span>

### <span data-ttu-id="7ec2d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ec2d-115">-AsJob</span></span>
<span data-ttu-id="7ec2d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7ec2d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7ec2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec2d-117">-DefaultProfile</span></span>
<span data-ttu-id="7ec2d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ec2d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ec2d-119">-InputObject</span></span>
<span data-ttu-id="7ec2d-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ec2d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ec2d-121">-Name</span></span>
<span data-ttu-id="7ec2d-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="7ec2d-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7ec2d-123">-NoWait</span></span>
<span data-ttu-id="7ec2d-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7ec2d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7ec2d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ec2d-125">-PassThru</span></span>
<span data-ttu-id="7ec2d-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7ec2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ec2d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ec2d-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7ec2d-129">-SubscriptionId</span></span>
<span data-ttu-id="7ec2d-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-130">The Azure subscription ID.</span></span>
<span data-ttu-id="7ec2d-131">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7ec2d-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7ec2d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ec2d-132">-Confirm</span></span>
<span data-ttu-id="7ec2d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec2d-134">-WhatIf</span></span>
<span data-ttu-id="7ec2d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ec2d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec2d-137">CommonParameters</span></span>
<span data-ttu-id="7ec2d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec2d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec2d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ec2d-140">INPUTS</span></span>

### <span data-ttu-id="7ec2d-141">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="7ec2d-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="7ec2d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ec2d-142">OUTPUTS</span></span>

### <span data-ttu-id="7ec2d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2d-143">System.Boolean</span></span>

## <span data-ttu-id="7ec2d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ec2d-144">NOTES</span></span>

<span data-ttu-id="7ec2d-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7ec2d-145">ALIASES</span></span>

<span data-ttu-id="7ec2d-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ec2d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ec2d-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ec2d-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ec2d-149">INPUTobject <ICustomProvidersIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7ec2d-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ec2d-150">`[AssociationName <String>]`: Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="7ec2d-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7ec2d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ec2d-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7ec2d-153">`[ResourceProviderName <String>]`: Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="7ec2d-154">`[Scope <String>]`: Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="7ec2d-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7ec2d-156">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7ec2d-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7ec2d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ec2d-157">RELATED LINKS</span></span>

