---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327115"
---
# <span data-ttu-id="56a5a-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="56a5a-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="56a5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="56a5a-103">Pobiera informacje o zadaniach DATAbox</span><span class="sxs-lookup"><span data-stu-id="56a5a-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="56a5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56a5a-104">SYNTAX</span></span>

### <span data-ttu-id="56a5a-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56a5a-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56a5a-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56a5a-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56a5a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56a5a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56a5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="56a5a-108">DESCRIPTION</span></span>
<span data-ttu-id="56a5a-109">Polecenie cmdlet **Get-AzDataBoxJobs** pobiera informacje o zadaniach DATAbox w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56a5a-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="56a5a-110">Jeśli określisz grupę zasobów, to polecenie cmdlet będzie pobierać wszystkie zadania DATAbox pod tą grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="56a5a-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="56a5a-111">Jeśli określisz nazwę zadania wraz z nazwą grupy zasobów, to polecenie cmdlet będzie pobierać informacje o tym konkretnym zadaniu DATAbox.</span><span class="sxs-lookup"><span data-stu-id="56a5a-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="56a5a-112">Jeśli nie określisz niczego innego niż identyfikator abonamentu, to polecenie cmdlet będzie pobierać informacje o wszystkich databoxych zadaniach w ramach tego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="56a5a-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="56a5a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56a5a-113">EXAMPLES</span></span>

### <span data-ttu-id="56a5a-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56a5a-114">Example 1</span></span>
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

<span data-ttu-id="56a5a-115">Get-AzDataBoxJob bez żadnych parametrów pobiera wszystkie zadania DATAbox w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="56a5a-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="56a5a-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="56a5a-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="56a5a-117">Get-AzDataBoxJob z parametrem ResourceGroupName pobiera wszystkie zadania DATAbox w ramach określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56a5a-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="56a5a-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="56a5a-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="56a5a-119">Get-AzDataBoxJob o podanej nazwie i ResourceGroupName będą pobierać określone zadanie DATAbox</span><span class="sxs-lookup"><span data-stu-id="56a5a-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="56a5a-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="56a5a-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="56a5a-121">Get-AzDataBoxJob z określonym identyfikatorem ResourceId spowoduje pobranie określonego zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="56a5a-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="56a5a-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56a5a-122">PARAMETERS</span></span>

### <span data-ttu-id="56a5a-123">-Przerwano</span><span class="sxs-lookup"><span data-stu-id="56a5a-123">-Aborted</span></span>
<span data-ttu-id="56a5a-124">Parametr Przełącz umożliwiający pobieranie przerwanych zadań</span><span class="sxs-lookup"><span data-stu-id="56a5a-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="56a5a-125">— Anulowano</span><span class="sxs-lookup"><span data-stu-id="56a5a-125">-Cancelled</span></span>
<span data-ttu-id="56a5a-126">Parametr Przełącz umożliwiający pobieranie anulowanych zadań</span><span class="sxs-lookup"><span data-stu-id="56a5a-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="56a5a-127">— Ukończono</span><span class="sxs-lookup"><span data-stu-id="56a5a-127">-Completed</span></span>
<span data-ttu-id="56a5a-128">Parametr Przełącz umożliwiający pobranie ukończonych zadań</span><span class="sxs-lookup"><span data-stu-id="56a5a-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="56a5a-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="56a5a-129">-CompletedWithError</span></span>
<span data-ttu-id="56a5a-130">Parametr Przełącz umożliwiający pobranie zadań wykonanych z błędami</span><span class="sxs-lookup"><span data-stu-id="56a5a-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="56a5a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a5a-131">-DefaultProfile</span></span>
<span data-ttu-id="56a5a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56a5a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56a5a-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56a5a-133">-Name</span></span>
<span data-ttu-id="56a5a-134">Nazwa zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="56a5a-134">Databox Job Name</span></span>

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

### <span data-ttu-id="56a5a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a5a-135">-ResourceGroupName</span></span>
<span data-ttu-id="56a5a-136">Nazwa grupy zasobów zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="56a5a-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="56a5a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56a5a-137">-ResourceId</span></span>
<span data-ttu-id="56a5a-138">Identyfikator zasobu zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="56a5a-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="56a5a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a5a-139">CommonParameters</span></span>
<span data-ttu-id="56a5a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a5a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a5a-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56a5a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a5a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56a5a-142">INPUTS</span></span>

### <span data-ttu-id="56a5a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="56a5a-143">System.String</span></span>

## <span data-ttu-id="56a5a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56a5a-144">OUTPUTS</span></span>

### <span data-ttu-id="56a5a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="56a5a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="56a5a-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56a5a-146">NOTES</span></span>

## <span data-ttu-id="56a5a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56a5a-147">RELATED LINKS</span></span>
