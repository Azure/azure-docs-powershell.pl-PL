---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221713"
---
# <span data-ttu-id="2e53d-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="2e53d-101">Get-AzImportExport</span></span>

## <span data-ttu-id="2e53d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e53d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e53d-103">Pobiera informacje o istniejącym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="2e53d-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="2e53d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e53d-104">SYNTAX</span></span>

### <span data-ttu-id="2e53d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2e53d-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e53d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2e53d-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e53d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e53d-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e53d-108">List1</span><span class="sxs-lookup"><span data-stu-id="2e53d-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e53d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2e53d-109">DESCRIPTION</span></span>
<span data-ttu-id="2e53d-110">Pobiera informacje o istniejącym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="2e53d-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="2e53d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e53d-111">EXAMPLES</span></span>

### <span data-ttu-id="2e53d-112">Przykład 1: pobieranie zadania programu ImportExport z domyślnym kontekstem</span><span class="sxs-lookup"><span data-stu-id="2e53d-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2e53d-113">To polecenie cmdlet pobiera zadanie ImportExport z kontekstem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="2e53d-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="2e53d-114">Przykład 2: pobieranie zadania ImportExport według grupy zasobów i nazwy zadania</span><span class="sxs-lookup"><span data-stu-id="2e53d-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2e53d-115">To polecenie cmdlet pobiera zadanie ImportExport według grupy zasobów i nazwy zadania.</span><span class="sxs-lookup"><span data-stu-id="2e53d-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="2e53d-116">Przykład 3: wyświetla wszystkie zadania ImportExport w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e53d-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2e53d-117">To polecenie cmdlet wyświetla wszystkie zadania ImportExport w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e53d-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="2e53d-118">Przykład 4: pobieranie zadania ImportExport według tożsamości</span><span class="sxs-lookup"><span data-stu-id="2e53d-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2e53d-119">Te listy poleceń cmdlet pobierają zadania ImportExport według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2e53d-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="2e53d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e53d-120">PARAMETERS</span></span>

### <span data-ttu-id="2e53d-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2e53d-121">-AcceptLanguage</span></span>
<span data-ttu-id="2e53d-122">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="2e53d-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="2e53d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e53d-123">-DefaultProfile</span></span>
<span data-ttu-id="2e53d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e53d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e53d-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="2e53d-125">-Filter</span></span>
<span data-ttu-id="2e53d-126">Można użyć w celu ograniczenia wyników do określonych warunków.</span><span class="sxs-lookup"><span data-stu-id="2e53d-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e53d-127">-InputObject</span></span>
<span data-ttu-id="2e53d-128">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2e53d-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e53d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e53d-129">-Name</span></span>
<span data-ttu-id="2e53d-130">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="2e53d-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e53d-131">-ResourceGroupName</span></span>
<span data-ttu-id="2e53d-132">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2e53d-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53d-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e53d-133">-SubscriptionId</span></span>
<span data-ttu-id="2e53d-134">Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e53d-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53d-135">-Początek</span><span class="sxs-lookup"><span data-stu-id="2e53d-135">-Top</span></span>
<span data-ttu-id="2e53d-136">Wartość całkowita określająca liczbę zwracanych zadań.</span><span class="sxs-lookup"><span data-stu-id="2e53d-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="2e53d-137">Wartość nie może przekroczyć 100.</span><span class="sxs-lookup"><span data-stu-id="2e53d-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e53d-138">CommonParameters</span></span>
<span data-ttu-id="2e53d-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e53d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e53d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e53d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e53d-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e53d-141">INPUTS</span></span>

### <span data-ttu-id="2e53d-142">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="2e53d-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="2e53d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e53d-143">OUTPUTS</span></span>

### <span data-ttu-id="2e53d-144">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="2e53d-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="2e53d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e53d-145">NOTES</span></span>

<span data-ttu-id="2e53d-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2e53d-146">ALIASES</span></span>

<span data-ttu-id="2e53d-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e53d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e53d-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2e53d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e53d-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e53d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e53d-150">INPUTobject <IImportExportIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2e53d-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e53d-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2e53d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e53d-152">`[JobName <String>]`: Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="2e53d-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="2e53d-153">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2e53d-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="2e53d-154">Na przykład w przypadku zachodniego, USA lub zachodniego.</span><span class="sxs-lookup"><span data-stu-id="2e53d-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="2e53d-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2e53d-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="2e53d-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e53d-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="2e53d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e53d-157">RELATED LINKS</span></span>

