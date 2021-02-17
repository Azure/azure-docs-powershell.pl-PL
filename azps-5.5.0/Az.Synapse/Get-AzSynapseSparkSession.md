---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243122"
---
# <span data-ttu-id="9a48d-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9a48d-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="9a48d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a48d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a48d-103">Pobiera sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9a48d-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9a48d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a48d-104">SYNTAX</span></span>

### <span data-ttu-id="9a48d-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9a48d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a48d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a48d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a48d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a48d-107">DESCRIPTION</span></span>
<span data-ttu-id="9a48d-108">Polecenie **cmdlet Get-AzSynapseSparkSession** pobiera informacje o sesji azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9a48d-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9a48d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a48d-109">EXAMPLES</span></span>

### <span data-ttu-id="9a48d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a48d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="9a48d-111">To polecenie pobiera wszystkie sesje przebiegu w czasie w ramach określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="9a48d-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="9a48d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9a48d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="9a48d-113">To polecenie pobiera sesję przebiegu w czasie o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="9a48d-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="9a48d-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9a48d-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="9a48d-115">To polecenie pobiera wszystkie sesje przebiegu w czasie w ramach określonej puli przebiegu w czasie za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="9a48d-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="9a48d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a48d-116">PARAMETERS</span></span>

### <span data-ttu-id="9a48d-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9a48d-117">-ApplicationId</span></span>
<span data-ttu-id="9a48d-118">Identyfikator aplikacji sesji.</span><span class="sxs-lookup"><span data-stu-id="9a48d-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="9a48d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a48d-119">-DefaultProfile</span></span>
<span data-ttu-id="9a48d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a48d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a48d-121">- Natłok</span><span class="sxs-lookup"><span data-stu-id="9a48d-121">-LivyId</span></span>
<span data-ttu-id="9a48d-122">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="9a48d-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="9a48d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9a48d-123">-Name</span></span>
<span data-ttu-id="9a48d-124">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="9a48d-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9a48d-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9a48d-125">-SparkPoolName</span></span>
<span data-ttu-id="9a48d-126">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="9a48d-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9a48d-127">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9a48d-127">-SparkPoolObject</span></span>
<span data-ttu-id="9a48d-128">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu w uścisce, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="9a48d-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a48d-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a48d-129">-WorkspaceName</span></span>
<span data-ttu-id="9a48d-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9a48d-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9a48d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a48d-131">CommonParameters</span></span>
<span data-ttu-id="9a48d-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a48d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a48d-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a48d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a48d-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a48d-134">INPUTS</span></span>

### <span data-ttu-id="9a48d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9a48d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="9a48d-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a48d-136">OUTPUTS</span></span>

### <span data-ttu-id="9a48d-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9a48d-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9a48d-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a48d-138">NOTES</span></span>

## <span data-ttu-id="9a48d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a48d-139">RELATED LINKS</span></span>
