---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221181"
---
# <span data-ttu-id="03df0-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="03df0-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="03df0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03df0-102">SYNOPSIS</span></span>
<span data-ttu-id="03df0-103">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="03df0-103">Deletes an existing job.</span></span>
<span data-ttu-id="03df0-104">Można usuwać tylko zadania w Stanach Tworzenie lub ukończone.</span><span class="sxs-lookup"><span data-stu-id="03df0-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="03df0-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03df0-105">SYNTAX</span></span>

### <span data-ttu-id="03df0-106">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="03df0-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03df0-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03df0-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03df0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03df0-108">DESCRIPTION</span></span>
<span data-ttu-id="03df0-109">Usuwa istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="03df0-109">Deletes an existing job.</span></span>
<span data-ttu-id="03df0-110">Można usuwać tylko zadania w Stanach Tworzenie lub ukończone.</span><span class="sxs-lookup"><span data-stu-id="03df0-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="03df0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03df0-111">EXAMPLES</span></span>

### <span data-ttu-id="03df0-112">Przykład 1: usuwanie zadania programu ImportExport według nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="03df0-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="03df0-113">To polecenie cmdlet usuwa zadanie ImportExport przez przydzielonej nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="03df0-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="03df0-114">Przykład 2: usuwanie zadania ImportExport według tożsamości</span><span class="sxs-lookup"><span data-stu-id="03df0-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="03df0-115">Te polecenia cmdlet usuwają zadanie ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="03df0-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="03df0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03df0-116">PARAMETERS</span></span>

### <span data-ttu-id="03df0-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="03df0-117">-AcceptLanguage</span></span>
<span data-ttu-id="03df0-118">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="03df0-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="03df0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03df0-119">-DefaultProfile</span></span>
<span data-ttu-id="03df0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03df0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03df0-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03df0-121">-InputObject</span></span>
<span data-ttu-id="03df0-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="03df0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="03df0-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03df0-123">-Name</span></span>
<span data-ttu-id="03df0-124">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="03df0-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="03df0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03df0-125">-PassThru</span></span>
<span data-ttu-id="03df0-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="03df0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="03df0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03df0-127">-ResourceGroupName</span></span>
<span data-ttu-id="03df0-128">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="03df0-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="03df0-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03df0-129">-SubscriptionId</span></span>
<span data-ttu-id="03df0-130">Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="03df0-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="03df0-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03df0-131">-Confirm</span></span>
<span data-ttu-id="03df0-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03df0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03df0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03df0-133">-WhatIf</span></span>
<span data-ttu-id="03df0-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03df0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03df0-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03df0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03df0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03df0-136">CommonParameters</span></span>
<span data-ttu-id="03df0-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03df0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03df0-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03df0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03df0-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03df0-139">INPUTS</span></span>

### <span data-ttu-id="03df0-140">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="03df0-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="03df0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03df0-141">OUTPUTS</span></span>

### <span data-ttu-id="03df0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03df0-142">System.Boolean</span></span>

## <span data-ttu-id="03df0-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03df0-143">NOTES</span></span>

<span data-ttu-id="03df0-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="03df0-144">ALIASES</span></span>

<span data-ttu-id="03df0-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03df0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03df0-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="03df0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03df0-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03df0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03df0-148">INPUTobject <IImportExportIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="03df0-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03df0-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="03df0-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03df0-150">`[JobName <String>]`: Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="03df0-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="03df0-151">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="03df0-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="03df0-152">Na przykład w przypadku zachodniego, USA lub zachodniego.</span><span class="sxs-lookup"><span data-stu-id="03df0-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="03df0-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="03df0-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="03df0-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="03df0-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="03df0-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03df0-155">RELATED LINKS</span></span>

