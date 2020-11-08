---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225575"
---
# <span data-ttu-id="f06c1-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="f06c1-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="f06c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f06c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f06c1-103">Wywołuje instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f06c1-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f06c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f06c1-104">SYNTAX</span></span>

### <span data-ttu-id="f06c1-105">RunSparkStatementByCodePathParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f06c1-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f06c1-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06c1-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f06c1-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06c1-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f06c1-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06c1-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f06c1-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f06c1-109">DESCRIPTION</span></span>
<span data-ttu-id="f06c1-110">Polecenie cmdlet **Invoke-AzSynapseSparkStatement** wywołuje instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f06c1-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f06c1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f06c1-111">EXAMPLES</span></span>

### <span data-ttu-id="f06c1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f06c1-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="f06c1-113">Te polecenia rozpoczynają sesję platformy Spark, a następnie wywołują wbudowaną instrukcję Spark za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="f06c1-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="f06c1-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f06c1-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="f06c1-115">Te polecenia rozpoczynają sesję platformy Spark, a następnie wywołują wbudowaną instrukcję Spark.</span><span class="sxs-lookup"><span data-stu-id="f06c1-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="f06c1-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f06c1-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="f06c1-117">Te polecenia rozpoczynają sesję platformy Spark, a następnie wywołują instrukcje programu Spark w pliku.</span><span class="sxs-lookup"><span data-stu-id="f06c1-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="f06c1-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f06c1-118">PARAMETERS</span></span>

### <span data-ttu-id="f06c1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f06c1-119">-AsJob</span></span>
<span data-ttu-id="f06c1-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f06c1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f06c1-121">— Kod</span><span class="sxs-lookup"><span data-stu-id="f06c1-121">-Code</span></span>
<span data-ttu-id="f06c1-122">Kod wykonania.</span><span class="sxs-lookup"><span data-stu-id="f06c1-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06c1-123">-DefaultProfile</span></span>
<span data-ttu-id="f06c1-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f06c1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f06c1-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f06c1-125">-FilePath</span></span>
<span data-ttu-id="f06c1-126">Określa ścieżkę pliku lokalnego zawierającą kod wykonania.</span><span class="sxs-lookup"><span data-stu-id="f06c1-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-127">-Language</span><span class="sxs-lookup"><span data-stu-id="f06c1-127">-Language</span></span>
<span data-ttu-id="f06c1-128">Język kodu wykonania.</span><span class="sxs-lookup"><span data-stu-id="f06c1-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-129">-Response</span><span class="sxs-lookup"><span data-stu-id="f06c1-129">-Response</span></span>
<span data-ttu-id="f06c1-130">Wskazuje, że należy zwrócić pełną odpowiedź.</span><span class="sxs-lookup"><span data-stu-id="f06c1-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="f06c1-131">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="f06c1-131">-SessionId</span></span>
<span data-ttu-id="f06c1-132">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="f06c1-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-133">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="f06c1-133">-SessionObject</span></span>
<span data-ttu-id="f06c1-134">Obiekt wejściowy sesji usługi Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f06c1-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f06c1-135">-SparkPoolName</span></span>
<span data-ttu-id="f06c1-136">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="f06c1-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-137">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f06c1-137">-WorkspaceName</span></span>
<span data-ttu-id="f06c1-138">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f06c1-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06c1-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f06c1-139">-Confirm</span></span>
<span data-ttu-id="f06c1-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f06c1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f06c1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f06c1-141">-WhatIf</span></span>
<span data-ttu-id="f06c1-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f06c1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f06c1-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f06c1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f06c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06c1-144">CommonParameters</span></span>
<span data-ttu-id="f06c1-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f06c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06c1-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f06c1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06c1-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f06c1-147">INPUTS</span></span>

### <span data-ttu-id="f06c1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f06c1-148">System.String</span></span>

### <span data-ttu-id="f06c1-149">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f06c1-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f06c1-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f06c1-150">OUTPUTS</span></span>

### <span data-ttu-id="f06c1-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="f06c1-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="f06c1-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f06c1-152">NOTES</span></span>

## <span data-ttu-id="f06c1-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f06c1-153">RELATED LINKS</span></span>
