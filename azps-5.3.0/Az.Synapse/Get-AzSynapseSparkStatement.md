---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383971"
---
# <span data-ttu-id="8dd24-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8dd24-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="8dd24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8dd24-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd24-103">Pobiera instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="8dd24-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8dd24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8dd24-104">SYNTAX</span></span>

### <span data-ttu-id="8dd24-105">GetSparkStatementsByIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8dd24-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd24-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd24-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dd24-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8dd24-107">DESCRIPTION</span></span>
<span data-ttu-id="8dd24-108">Polecenie cmdlet **Get-AzSynapseSparkStatement** pobiera informacje o instrukcji Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="8dd24-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8dd24-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8dd24-109">EXAMPLES</span></span>

### <span data-ttu-id="8dd24-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8dd24-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="8dd24-111">To polecenie pobiera wszystkie instrukcje usługi Spark w ramach sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="8dd24-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="8dd24-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8dd24-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="8dd24-113">To polecenie pobiera instrukcję Spark z określonym IDENTYFIKATORem livy.</span><span class="sxs-lookup"><span data-stu-id="8dd24-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="8dd24-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8dd24-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="8dd24-115">To polecenie pobiera wszystkie instrukcje usługi Spark w sesji Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8dd24-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="8dd24-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8dd24-116">PARAMETERS</span></span>

### <span data-ttu-id="8dd24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd24-117">-DefaultProfile</span></span>
<span data-ttu-id="8dd24-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd24-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8dd24-119">-LivyId</span></span>
<span data-ttu-id="8dd24-120">Identyfikator instrukcji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="8dd24-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="8dd24-121">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="8dd24-121">-SessionId</span></span>
<span data-ttu-id="8dd24-122">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="8dd24-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="8dd24-123">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="8dd24-123">-SessionObject</span></span>
<span data-ttu-id="8dd24-124">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8dd24-124">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8dd24-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8dd24-125">-SparkPoolName</span></span>
<span data-ttu-id="8dd24-126">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="8dd24-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8dd24-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8dd24-127">-WorkspaceName</span></span>
<span data-ttu-id="8dd24-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8dd24-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8dd24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd24-129">CommonParameters</span></span>
<span data-ttu-id="8dd24-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd24-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dd24-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd24-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dd24-132">INPUTS</span></span>

### <span data-ttu-id="8dd24-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8dd24-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8dd24-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8dd24-134">OUTPUTS</span></span>

### <span data-ttu-id="8dd24-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8dd24-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="8dd24-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8dd24-136">NOTES</span></span>

## <span data-ttu-id="8dd24-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dd24-137">RELATED LINKS</span></span>
