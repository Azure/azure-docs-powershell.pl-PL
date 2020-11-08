---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220995"
---
# <span data-ttu-id="102a9-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="102a9-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="102a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="102a9-102">SYNOPSIS</span></span>
<span data-ttu-id="102a9-103">Pobiera sesję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="102a9-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="102a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="102a9-104">SYNTAX</span></span>

### <span data-ttu-id="102a9-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="102a9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="102a9-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="102a9-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="102a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="102a9-107">DESCRIPTION</span></span>
<span data-ttu-id="102a9-108">Polecenie cmdlet **Get-AzSynapseSparkSession** pobiera informacje o sesji usługi Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="102a9-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="102a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="102a9-109">EXAMPLES</span></span>

### <span data-ttu-id="102a9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="102a9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="102a9-111">To polecenie pobiera wszystkie sesje platformy Spark w ramach określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="102a9-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="102a9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="102a9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="102a9-113">To polecenie pobiera sesję programu Spark o określonym IDENTYFIKATORze livy.</span><span class="sxs-lookup"><span data-stu-id="102a9-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="102a9-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="102a9-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="102a9-115">To polecenie pobiera wszystkie sesje platformy Spark w określonej puli platformy Spark za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="102a9-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="102a9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="102a9-116">PARAMETERS</span></span>

### <span data-ttu-id="102a9-117">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="102a9-117">-ApplicationId</span></span>
<span data-ttu-id="102a9-118">Identyfikator aplikacji sesji.</span><span class="sxs-lookup"><span data-stu-id="102a9-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="102a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102a9-119">-DefaultProfile</span></span>
<span data-ttu-id="102a9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="102a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102a9-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="102a9-121">-LivyId</span></span>
<span data-ttu-id="102a9-122">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="102a9-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="102a9-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="102a9-123">-Name</span></span>
<span data-ttu-id="102a9-124">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="102a9-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="102a9-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="102a9-125">-SparkPoolName</span></span>
<span data-ttu-id="102a9-126">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="102a9-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="102a9-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="102a9-127">-SparkPoolObject</span></span>
<span data-ttu-id="102a9-128">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="102a9-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="102a9-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="102a9-129">-WorkspaceName</span></span>
<span data-ttu-id="102a9-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="102a9-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="102a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102a9-131">CommonParameters</span></span>
<span data-ttu-id="102a9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="102a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102a9-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="102a9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102a9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="102a9-134">INPUTS</span></span>

### <span data-ttu-id="102a9-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="102a9-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="102a9-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="102a9-136">OUTPUTS</span></span>

### <span data-ttu-id="102a9-137">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="102a9-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="102a9-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="102a9-138">NOTES</span></span>

## <span data-ttu-id="102a9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="102a9-139">RELATED LINKS</span></span>
