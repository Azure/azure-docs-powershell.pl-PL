---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383994"
---
# <span data-ttu-id="a2574-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="a2574-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="a2574-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2574-102">SYNOPSIS</span></span>
<span data-ttu-id="a2574-103">Pobiera zadanie Synapse analiza Spark.</span><span class="sxs-lookup"><span data-stu-id="a2574-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="a2574-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2574-104">SYNTAX</span></span>

### <span data-ttu-id="a2574-105">GetSparkJobsByIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2574-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2574-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2574-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2574-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a2574-107">DESCRIPTION</span></span>
<span data-ttu-id="a2574-108">Polecenie cmdlet **Get-AzSynapseSparkJob** pobiera zadanie usługi Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="a2574-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="a2574-109">Jeśli nie podano zadania, to polecenie cmdlet umożliwia pobieranie wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="a2574-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="a2574-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2574-110">EXAMPLES</span></span>

### <span data-ttu-id="a2574-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2574-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="a2574-112">To polecenie pobiera wszystkie zadania w ramach puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="a2574-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="a2574-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2574-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="a2574-114">To polecenie pobiera zadanie z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="a2574-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="a2574-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a2574-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="a2574-116">To polecenie pobiera zadanie z określonym IDENTYFIKATORem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a2574-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="a2574-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a2574-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="a2574-118">To polecenie pobiera wszystkie zadania w ramach puli usługi Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="a2574-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="a2574-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2574-119">PARAMETERS</span></span>

### <span data-ttu-id="a2574-120">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="a2574-120">-ApplicationId</span></span>
<span data-ttu-id="a2574-121">Identyfikator aplikacji sesji.</span><span class="sxs-lookup"><span data-stu-id="a2574-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="a2574-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2574-122">-DefaultProfile</span></span>
<span data-ttu-id="a2574-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2574-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2574-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="a2574-124">-LivyId</span></span>
<span data-ttu-id="a2574-125">Identyfikator zadania usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="a2574-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="a2574-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2574-126">-Name</span></span>
<span data-ttu-id="a2574-127">Nazwa zadania usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="a2574-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="a2574-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a2574-128">-SparkPoolName</span></span>
<span data-ttu-id="a2574-129">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="a2574-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="a2574-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="a2574-130">-SparkPoolObject</span></span>
<span data-ttu-id="a2574-131">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a2574-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2574-132">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a2574-132">-WorkspaceName</span></span>
<span data-ttu-id="a2574-133">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2574-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2574-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2574-134">CommonParameters</span></span>
<span data-ttu-id="a2574-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2574-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2574-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2574-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2574-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2574-137">INPUTS</span></span>

### <span data-ttu-id="a2574-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a2574-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a2574-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2574-139">OUTPUTS</span></span>

### <span data-ttu-id="a2574-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="a2574-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="a2574-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2574-141">NOTES</span></span>

## <span data-ttu-id="a2574-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2574-142">RELATED LINKS</span></span>
