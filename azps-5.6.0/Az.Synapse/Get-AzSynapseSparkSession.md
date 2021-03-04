---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: efe733250c43d79aa8296db380ac453d44231c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011313"
---
# <span data-ttu-id="28c82-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="28c82-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="28c82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28c82-102">SYNOPSIS</span></span>
<span data-ttu-id="28c82-103">Pobiera sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="28c82-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="28c82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28c82-104">SYNTAX</span></span>

### <span data-ttu-id="28c82-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="28c82-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28c82-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c82-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28c82-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="28c82-107">DESCRIPTION</span></span>
<span data-ttu-id="28c82-108">Polecenie **cmdlet Get-AzSynapseSparkSession** pobiera informacje o sesji azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="28c82-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="28c82-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28c82-109">EXAMPLES</span></span>

### <span data-ttu-id="28c82-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28c82-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="28c82-111">To polecenie pobiera wszystkie sesje przebiegu w czasie w ramach określonej puli przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="28c82-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="28c82-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="28c82-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="28c82-113">To polecenie pobiera sesję przebiegu w czasie o określonym identyfikatorze przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="28c82-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="28c82-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="28c82-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="28c82-115">To polecenie pobiera wszystkie sesje przebiegu w czasie w ramach określonej puli przebiegu w czasie za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="28c82-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="28c82-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28c82-116">PARAMETERS</span></span>

### <span data-ttu-id="28c82-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="28c82-117">-ApplicationId</span></span>
<span data-ttu-id="28c82-118">Identyfikator aplikacji sesji.</span><span class="sxs-lookup"><span data-stu-id="28c82-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="28c82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c82-119">-DefaultProfile</span></span>
<span data-ttu-id="28c82-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="28c82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c82-121">- Natłok</span><span class="sxs-lookup"><span data-stu-id="28c82-121">-LivyId</span></span>
<span data-ttu-id="28c82-122">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="28c82-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="28c82-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="28c82-123">-Name</span></span>
<span data-ttu-id="28c82-124">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="28c82-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="28c82-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="28c82-125">-SparkPoolName</span></span>
<span data-ttu-id="28c82-126">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="28c82-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="28c82-127">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="28c82-127">-SparkPoolObject</span></span>
<span data-ttu-id="28c82-128">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="28c82-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="28c82-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28c82-129">-WorkspaceName</span></span>
<span data-ttu-id="28c82-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="28c82-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="28c82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c82-131">CommonParameters</span></span>
<span data-ttu-id="28c82-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c82-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28c82-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c82-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28c82-134">INPUTS</span></span>

### <span data-ttu-id="28c82-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="28c82-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="28c82-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28c82-136">OUTPUTS</span></span>

### <span data-ttu-id="28c82-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="28c82-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="28c82-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28c82-138">NOTES</span></span>

## <span data-ttu-id="28c82-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28c82-139">RELATED LINKS</span></span>
