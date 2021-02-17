---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188291"
---
# <span data-ttu-id="bdbae-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="bdbae-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="bdbae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdbae-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbae-103">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="bdbae-103">Deletes an existing job.</span></span>
<span data-ttu-id="bdbae-104">Tylko zadania w stanach Tworzenie lub Wykonane można usuwać.</span><span class="sxs-lookup"><span data-stu-id="bdbae-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="bdbae-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdbae-105">SYNTAX</span></span>

### <span data-ttu-id="bdbae-106">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="bdbae-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bdbae-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdbae-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bdbae-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdbae-108">DESCRIPTION</span></span>
<span data-ttu-id="bdbae-109">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="bdbae-109">Deletes an existing job.</span></span>
<span data-ttu-id="bdbae-110">Tylko zadania w stanach Tworzenie lub Wykonane można usuwać.</span><span class="sxs-lookup"><span data-stu-id="bdbae-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="bdbae-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdbae-111">EXAMPLES</span></span>

### <span data-ttu-id="bdbae-112">Przykład 1. Usuwanie zadania ImportExport według nazwy serwera i grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bdbae-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="bdbae-113">To polecenie cmdlet usuwa zadanie ImportExport według nazwy serwera i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdbae-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="bdbae-114">Przykład 2. Usuwanie zadania ImportExport według tożsamości</span><span class="sxs-lookup"><span data-stu-id="bdbae-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="bdbae-115">To polecenie cmdlet usuwa zadanie ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="bdbae-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="bdbae-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdbae-116">PARAMETERS</span></span>

### <span data-ttu-id="bdbae-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="bdbae-117">-AcceptLanguage</span></span>
<span data-ttu-id="bdbae-118">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="bdbae-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="bdbae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbae-119">-DefaultProfile</span></span>
<span data-ttu-id="bdbae-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdbae-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdbae-121">-InputObject</span></span>
<span data-ttu-id="bdbae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bdbae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bdbae-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bdbae-123">-Name</span></span>
<span data-ttu-id="bdbae-124">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="bdbae-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="bdbae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdbae-125">-PassThru</span></span>
<span data-ttu-id="bdbae-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bdbae-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bdbae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbae-127">-ResourceGroupName</span></span>
<span data-ttu-id="bdbae-128">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bdbae-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="bdbae-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdbae-129">-SubscriptionId</span></span>
<span data-ttu-id="bdbae-130">Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbae-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="bdbae-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdbae-131">-Confirm</span></span>
<span data-ttu-id="bdbae-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdbae-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbae-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbae-133">-WhatIf</span></span>
<span data-ttu-id="bdbae-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdbae-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbae-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bdbae-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbae-136">CommonParameters</span></span>
<span data-ttu-id="bdbae-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdbae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbae-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdbae-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbae-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdbae-139">INPUTS</span></span>

### <span data-ttu-id="bdbae-140">Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="bdbae-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="bdbae-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdbae-141">OUTPUTS</span></span>

### <span data-ttu-id="bdbae-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdbae-142">System.Boolean</span></span>

## <span data-ttu-id="bdbae-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdbae-143">NOTES</span></span>

<span data-ttu-id="bdbae-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bdbae-144">ALIASES</span></span>

<span data-ttu-id="bdbae-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdbae-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdbae-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bdbae-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdbae-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdbae-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdbae-148">INPUTOBJECT: <IImportExportIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bdbae-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdbae-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bdbae-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdbae-150">`[JobName <String>]`: nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="bdbae-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="bdbae-151">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bdbae-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="bdbae-152">Na przykład Stany Zjednoczone Lub Zachód.</span><span class="sxs-lookup"><span data-stu-id="bdbae-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="bdbae-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bdbae-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="bdbae-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbae-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="bdbae-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdbae-155">RELATED LINKS</span></span>

