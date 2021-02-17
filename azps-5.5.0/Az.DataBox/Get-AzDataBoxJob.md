---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177171"
---
# <span data-ttu-id="78b6f-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="78b6f-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="78b6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="78b6f-103">Pobiera informacje o zadaniach pola danych</span><span class="sxs-lookup"><span data-stu-id="78b6f-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="78b6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78b6f-104">SYNTAX</span></span>

### <span data-ttu-id="78b6f-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="78b6f-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b6f-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78b6f-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78b6f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78b6f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78b6f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="78b6f-108">DESCRIPTION</span></span>
<span data-ttu-id="78b6f-109">Polecenie **cmdlet Get-AzDataBoxJobs** pobiera informacje o zadaniach skrzynki danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="78b6f-110">Jeśli określisz grupę zasobów, to polecenie cmdlet pobiera wszystkie zadania pola danych w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="78b6f-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="78b6f-111">Jeśli wraz z nazwą grupy zasobów określisz nazwę zadania, to polecenie cmdlet pobiera informacje o tym zadaniu określonego pola danych.</span><span class="sxs-lookup"><span data-stu-id="78b6f-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="78b6f-112">Jeśli nie określisz niczego innego niż identyfikator subskrypcji, to polecenie cmdlet pobiera informacje o wszystkich zadaniach skrzynki danych w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="78b6f-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="78b6f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78b6f-113">EXAMPLES</span></span>

### <span data-ttu-id="78b6f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78b6f-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="78b6f-115">Get-AzDataBoxJob bez żadnych parametrów pobiera wszystkie zadania pola danych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="78b6f-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="78b6f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="78b6f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="78b6f-117">Get-AzDataBoxJob parametrem ResourceGroupName pobiera wszystkie zadania pola danych w ramach określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="78b6f-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="78b6f-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="78b6f-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="78b6f-119">Get-AzDataBoxJob z określonymi nazwami ResourceGroupName i Name spowoduje pobranie określonego zadania pola danych</span><span class="sxs-lookup"><span data-stu-id="78b6f-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="78b6f-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="78b6f-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="78b6f-121">Get-AzDataBoxJob z określoną wartością ResourceId spowoduje pobranie określonego zadania pola danych</span><span class="sxs-lookup"><span data-stu-id="78b6f-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="78b6f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78b6f-122">PARAMETERS</span></span>

### <span data-ttu-id="78b6f-123">— Przerwano</span><span class="sxs-lookup"><span data-stu-id="78b6f-123">-Aborted</span></span>
<span data-ttu-id="78b6f-124">Przełączanie parametru w celu zdalnego dostępu do przerwanych zadań</span><span class="sxs-lookup"><span data-stu-id="78b6f-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-125">- Anulowano</span><span class="sxs-lookup"><span data-stu-id="78b6f-125">-Cancelled</span></span>
<span data-ttu-id="78b6f-126">Przełączanie parametru w celu zdalnego dostępu do anulowanych zadań</span><span class="sxs-lookup"><span data-stu-id="78b6f-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-127">— Ukończone</span><span class="sxs-lookup"><span data-stu-id="78b6f-127">-Completed</span></span>
<span data-ttu-id="78b6f-128">Przełączanie parametru w celu zdalnego dostępu do ukończonych zadań</span><span class="sxs-lookup"><span data-stu-id="78b6f-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="78b6f-129">-CompletedWithError</span></span>
<span data-ttu-id="78b6f-130">Przełączanie parametru do zadań zdalnego dostępu zakończonych błędami</span><span class="sxs-lookup"><span data-stu-id="78b6f-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b6f-131">-DefaultProfile</span></span>
<span data-ttu-id="78b6f-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78b6f-133">-Name</span></span>
<span data-ttu-id="78b6f-134">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="78b6f-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b6f-135">-ResourceGroupName</span></span>
<span data-ttu-id="78b6f-136">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="78b6f-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78b6f-137">-ResourceId</span></span>
<span data-ttu-id="78b6f-138">Identyfikator zasobu zadania w skrzynce danych</span><span class="sxs-lookup"><span data-stu-id="78b6f-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b6f-139">CommonParameters</span></span>
<span data-ttu-id="78b6f-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b6f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b6f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78b6f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b6f-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78b6f-142">INPUTS</span></span>

### <span data-ttu-id="78b6f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="78b6f-143">System.String</span></span>

## <span data-ttu-id="78b6f-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78b6f-144">OUTPUTS</span></span>

### <span data-ttu-id="78b6f-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="78b6f-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="78b6f-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78b6f-146">NOTES</span></span>

## <span data-ttu-id="78b6f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78b6f-147">RELATED LINKS</span></span>
