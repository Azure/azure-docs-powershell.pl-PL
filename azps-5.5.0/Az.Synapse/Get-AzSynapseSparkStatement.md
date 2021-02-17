---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182786"
---
# <span data-ttu-id="dc686-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="dc686-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="dc686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc686-102">SYNOPSIS</span></span>
<span data-ttu-id="dc686-103">Pobiera zestawienie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="dc686-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="dc686-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc686-104">SYNTAX</span></span>

### <span data-ttu-id="dc686-105">GetSparkStatementsByIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dc686-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc686-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc686-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc686-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc686-107">DESCRIPTION</span></span>
<span data-ttu-id="dc686-108">Polecenie **cmdlet Get-AzSynapseSparkStatement** pobiera informacje o instrukcji Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="dc686-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="dc686-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc686-109">EXAMPLES</span></span>

### <span data-ttu-id="dc686-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc686-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="dc686-111">To polecenie pobiera wszystkie instrukcje przebiegu w trakcie sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="dc686-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="dc686-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dc686-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="dc686-113">To polecenie pobiera instrukcje przebiegu w czasie z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="dc686-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="dc686-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dc686-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="dc686-115">To polecenie pobiera wszystkie instrukcje przebiegu w przebiegu w ramach sesji przebiegu w przebiegu w potoku.</span><span class="sxs-lookup"><span data-stu-id="dc686-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="dc686-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc686-116">PARAMETERS</span></span>

### <span data-ttu-id="dc686-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc686-117">-DefaultProfile</span></span>
<span data-ttu-id="dc686-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc686-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc686-119">- Natłok</span><span class="sxs-lookup"><span data-stu-id="dc686-119">-LivyId</span></span>
<span data-ttu-id="dc686-120">Identyfikator instrukcji Spark.</span><span class="sxs-lookup"><span data-stu-id="dc686-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="dc686-121">- SessionId</span><span class="sxs-lookup"><span data-stu-id="dc686-121">-SessionId</span></span>
<span data-ttu-id="dc686-122">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="dc686-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-123">- SessionObject</span><span class="sxs-lookup"><span data-stu-id="dc686-123">-SessionObject</span></span>
<span data-ttu-id="dc686-124">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu w uścisce, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="dc686-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="dc686-125">-SparkPoolName</span></span>
<span data-ttu-id="dc686-126">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="dc686-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dc686-127">-WorkspaceName</span></span>
<span data-ttu-id="dc686-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="dc686-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc686-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc686-129">CommonParameters</span></span>
<span data-ttu-id="dc686-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc686-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc686-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc686-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc686-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc686-132">INPUTS</span></span>

### <span data-ttu-id="dc686-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="dc686-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="dc686-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc686-134">OUTPUTS</span></span>

### <span data-ttu-id="dc686-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="dc686-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="dc686-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc686-136">NOTES</span></span>

## <span data-ttu-id="dc686-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc686-137">RELATED LINKS</span></span>
