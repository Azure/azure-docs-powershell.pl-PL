---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501285"
---
# <span data-ttu-id="1f919-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="1f919-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="1f919-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f919-102">SYNOPSIS</span></span>
<span data-ttu-id="1f919-103">Anuluje instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1f919-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="1f919-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f919-104">SYNTAX</span></span>

### <span data-ttu-id="1f919-105">StopSparkStatementByIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f919-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f919-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f919-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f919-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1f919-107">DESCRIPTION</span></span>
<span data-ttu-id="1f919-108">Polecenie cmdlet **stop-AzSynapseSparkStatement** anuluje instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="1f919-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="1f919-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f919-109">EXAMPLES</span></span>

### <span data-ttu-id="1f919-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f919-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="1f919-111">To polecenie anuluje instrukcję Spark przy użyciu określonego identyfikatora livy.</span><span class="sxs-lookup"><span data-stu-id="1f919-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="1f919-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1f919-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="1f919-113">To polecenie anuluje instrukcję Spark z określonym IDENTYFIKATORem livy za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1f919-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="1f919-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f919-114">PARAMETERS</span></span>

### <span data-ttu-id="1f919-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f919-115">-DefaultProfile</span></span>
<span data-ttu-id="1f919-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f919-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f919-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f919-117">-Force</span></span>
<span data-ttu-id="1f919-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f919-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="1f919-119">-LivyId</span></span>
<span data-ttu-id="1f919-120">Identyfikator instrukcji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="1f919-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f919-121">-PassThru</span></span>
<span data-ttu-id="1f919-122">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="1f919-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1f919-123">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="1f919-123">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-124">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="1f919-124">-SessionId</span></span>
<span data-ttu-id="1f919-125">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="1f919-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-126">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="1f919-126">-SessionObject</span></span>
<span data-ttu-id="1f919-127">Obiekt wejściowy sesji usługi Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1f919-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="1f919-128">-SparkPoolName</span></span>
<span data-ttu-id="1f919-129">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="1f919-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1f919-130">-WorkspaceName</span></span>
<span data-ttu-id="1f919-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="1f919-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f919-132">-Confirm</span></span>
<span data-ttu-id="1f919-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f919-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f919-134">-WhatIf</span></span>
<span data-ttu-id="1f919-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f919-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f919-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f919-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f919-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f919-137">CommonParameters</span></span>
<span data-ttu-id="1f919-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f919-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f919-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f919-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f919-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f919-140">INPUTS</span></span>

### <span data-ttu-id="1f919-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="1f919-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="1f919-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f919-142">OUTPUTS</span></span>

### <span data-ttu-id="1f919-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f919-143">System.Boolean</span></span>

## <span data-ttu-id="1f919-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f919-144">NOTES</span></span>

## <span data-ttu-id="1f919-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f919-145">RELATED LINKS</span></span>
