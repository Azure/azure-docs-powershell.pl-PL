---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195619"
---
# <span data-ttu-id="f9538-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="f9538-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="f9538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9538-102">SYNOPSIS</span></span>
<span data-ttu-id="f9538-103">Pobiera zadanie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f9538-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="f9538-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9538-104">SYNTAX</span></span>

### <span data-ttu-id="f9538-105">GetSparkJobsByIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f9538-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9538-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9538-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9538-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9538-107">DESCRIPTION</span></span>
<span data-ttu-id="f9538-108">Polecenie **cmdlet Get-AzSynapseSparkJob** pobiera zadanie Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f9538-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="f9538-109">Jeśli nie określisz zadania, to polecenie cmdlet będzie pobierać wszystkie zadania.</span><span class="sxs-lookup"><span data-stu-id="f9538-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="f9538-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9538-110">EXAMPLES</span></span>

### <span data-ttu-id="f9538-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9538-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="f9538-112">To polecenie pobiera wszystkie zadania w ramach puli przebiegu w czas.</span><span class="sxs-lookup"><span data-stu-id="f9538-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="f9538-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9538-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="f9538-114">To polecenie pobiera zadanie z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="f9538-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="f9538-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9538-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="f9538-116">To polecenie pobiera zadanie z określonym identyfikatorem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f9538-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="f9538-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f9538-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="f9538-118">To polecenie pobiera wszystkie zadania w puli przebiegu w przebiegu w potoku.</span><span class="sxs-lookup"><span data-stu-id="f9538-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="f9538-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9538-119">PARAMETERS</span></span>

### <span data-ttu-id="f9538-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f9538-120">-ApplicationId</span></span>
<span data-ttu-id="f9538-121">Identyfikator aplikacji sesji.</span><span class="sxs-lookup"><span data-stu-id="f9538-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="f9538-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9538-122">-DefaultProfile</span></span>
<span data-ttu-id="f9538-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9538-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9538-124">- Natłok</span><span class="sxs-lookup"><span data-stu-id="f9538-124">-LivyId</span></span>
<span data-ttu-id="f9538-125">Identyfikator zadania przebiegu w sparku.</span><span class="sxs-lookup"><span data-stu-id="f9538-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9538-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f9538-126">-Name</span></span>
<span data-ttu-id="f9538-127">Nazwa zadania przebiegu w przebiegu w imieniu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9538-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="f9538-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f9538-128">-SparkPoolName</span></span>
<span data-ttu-id="f9538-129">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="f9538-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9538-130">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="f9538-130">-SparkPoolObject</span></span>
<span data-ttu-id="f9538-131">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu w uścisce, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="f9538-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9538-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9538-132">-WorkspaceName</span></span>
<span data-ttu-id="f9538-133">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f9538-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9538-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9538-134">CommonParameters</span></span>
<span data-ttu-id="f9538-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9538-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9538-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9538-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9538-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9538-137">INPUTS</span></span>

### <span data-ttu-id="f9538-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f9538-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f9538-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9538-139">OUTPUTS</span></span>

### <span data-ttu-id="f9538-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="f9538-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="f9538-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9538-141">NOTES</span></span>

## <span data-ttu-id="f9538-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9538-142">RELATED LINKS</span></span>
