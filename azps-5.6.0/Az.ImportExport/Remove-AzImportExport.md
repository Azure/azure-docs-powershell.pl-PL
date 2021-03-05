---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: c4ba805ca2f8f89fcc3ed23747f71c9efff01d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977105"
---
# <span data-ttu-id="517a6-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="517a6-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="517a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="517a6-102">SYNOPSIS</span></span>
<span data-ttu-id="517a6-103">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="517a6-103">Deletes an existing job.</span></span>
<span data-ttu-id="517a6-104">Można usuwać tylko zadania w stanach Tworzenie lub Ukończone.</span><span class="sxs-lookup"><span data-stu-id="517a6-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="517a6-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="517a6-105">SYNTAX</span></span>

### <span data-ttu-id="517a6-106">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="517a6-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="517a6-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="517a6-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="517a6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="517a6-108">DESCRIPTION</span></span>
<span data-ttu-id="517a6-109">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="517a6-109">Deletes an existing job.</span></span>
<span data-ttu-id="517a6-110">Można usuwać tylko zadania w stanach Tworzenie lub Ukończone.</span><span class="sxs-lookup"><span data-stu-id="517a6-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="517a6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="517a6-111">EXAMPLES</span></span>

### <span data-ttu-id="517a6-112">Przykład 1. Usuwanie zadania ImportExport według nazwy serwera i grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="517a6-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="517a6-113">To polecenie cmdlet usuwa zadanie ImportExport według nazwy serwera i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="517a6-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="517a6-114">Przykład 2. Usuwanie zadania ImportExport według tożsamości</span><span class="sxs-lookup"><span data-stu-id="517a6-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="517a6-115">To polecenie cmdlet usuwa zadanie ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="517a6-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="517a6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="517a6-116">PARAMETERS</span></span>

### <span data-ttu-id="517a6-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="517a6-117">-AcceptLanguage</span></span>
<span data-ttu-id="517a6-118">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="517a6-118">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517a6-119">-DefaultProfile</span></span>
<span data-ttu-id="517a6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="517a6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517a6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="517a6-121">-InputObject</span></span>
<span data-ttu-id="517a6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="517a6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="517a6-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="517a6-123">-Name</span></span>
<span data-ttu-id="517a6-124">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="517a6-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517a6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="517a6-125">-PassThru</span></span>
<span data-ttu-id="517a6-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="517a6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="517a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="517a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="517a6-128">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="517a6-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="517a6-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="517a6-129">-SubscriptionId</span></span>
<span data-ttu-id="517a6-130">Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="517a6-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="517a6-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="517a6-131">-Confirm</span></span>
<span data-ttu-id="517a6-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="517a6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="517a6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517a6-133">-WhatIf</span></span>
<span data-ttu-id="517a6-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517a6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="517a6-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="517a6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="517a6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517a6-136">CommonParameters</span></span>
<span data-ttu-id="517a6-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517a6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517a6-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="517a6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517a6-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="517a6-139">INPUTS</span></span>

### <span data-ttu-id="517a6-140">Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="517a6-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="517a6-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="517a6-141">OUTPUTS</span></span>

### <span data-ttu-id="517a6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="517a6-142">System.Boolean</span></span>

## <span data-ttu-id="517a6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="517a6-143">NOTES</span></span>

<span data-ttu-id="517a6-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="517a6-144">ALIASES</span></span>

<span data-ttu-id="517a6-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="517a6-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="517a6-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="517a6-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="517a6-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="517a6-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="517a6-148">INPUTOBJECT: <IImportExportIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="517a6-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="517a6-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="517a6-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="517a6-150">`[JobName <String>]`: nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="517a6-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="517a6-151">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="517a6-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="517a6-152">Na przykład Stany Zjednoczone Lub Zachód.</span><span class="sxs-lookup"><span data-stu-id="517a6-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="517a6-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="517a6-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="517a6-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="517a6-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="517a6-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="517a6-155">RELATED LINKS</span></span>

