---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061945"
---
# <span data-ttu-id="61703-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="61703-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="61703-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61703-102">SYNOPSIS</span></span>
<span data-ttu-id="61703-103">Wywołuje instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="61703-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="61703-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61703-104">SYNTAX</span></span>

### <span data-ttu-id="61703-105">RunSparkStatementByCodePathParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61703-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61703-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="61703-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61703-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61703-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61703-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61703-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61703-109">Opis</span><span class="sxs-lookup"><span data-stu-id="61703-109">DESCRIPTION</span></span>
<span data-ttu-id="61703-110">Polecenie cmdlet **Invoke-AzSynapseSparkStatement** wywołuje instrukcję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="61703-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="61703-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61703-111">EXAMPLES</span></span>

### <span data-ttu-id="61703-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="61703-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="61703-113">Te polecenia rozpoczynają sesję platformy Spark, a następnie wywołują wbudowaną instrukcję Spark za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="61703-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="61703-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="61703-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="61703-115">Te polecenia rozpoczynają sesję platformy Spark, a następnie wywołują wbudowaną instrukcję Spark.</span><span class="sxs-lookup"><span data-stu-id="61703-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="61703-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="61703-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="61703-117">Te polecenia rozpoczynają sesję platformy Spark, a następnie wywołują instrukcje programu Spark w pliku.</span><span class="sxs-lookup"><span data-stu-id="61703-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="61703-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61703-118">PARAMETERS</span></span>

### <span data-ttu-id="61703-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61703-119">-AsJob</span></span>
<span data-ttu-id="61703-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="61703-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61703-121">— Kod</span><span class="sxs-lookup"><span data-stu-id="61703-121">-Code</span></span>
<span data-ttu-id="61703-122">Kod wykonania.</span><span class="sxs-lookup"><span data-stu-id="61703-122">The execution code.</span></span>

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

### <span data-ttu-id="61703-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61703-123">-DefaultProfile</span></span>
<span data-ttu-id="61703-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61703-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61703-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="61703-125">-FilePath</span></span>
<span data-ttu-id="61703-126">Określa ścieżkę pliku lokalnego zawierającą kod wykonania.</span><span class="sxs-lookup"><span data-stu-id="61703-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="61703-127">-Language</span><span class="sxs-lookup"><span data-stu-id="61703-127">-Language</span></span>
<span data-ttu-id="61703-128">Język kodu wykonania.</span><span class="sxs-lookup"><span data-stu-id="61703-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="61703-129">-Response</span><span class="sxs-lookup"><span data-stu-id="61703-129">-Response</span></span>
<span data-ttu-id="61703-130">Wskazuje, że należy zwrócić pełną odpowiedź.</span><span class="sxs-lookup"><span data-stu-id="61703-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="61703-131">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="61703-131">-SessionId</span></span>
<span data-ttu-id="61703-132">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="61703-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="61703-133">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="61703-133">-SessionObject</span></span>
<span data-ttu-id="61703-134">Obiekt wejściowy sesji usługi Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="61703-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="61703-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="61703-135">-SparkPoolName</span></span>
<span data-ttu-id="61703-136">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="61703-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="61703-137">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="61703-137">-WorkspaceName</span></span>
<span data-ttu-id="61703-138">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="61703-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="61703-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61703-139">-Confirm</span></span>
<span data-ttu-id="61703-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61703-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61703-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61703-141">-WhatIf</span></span>
<span data-ttu-id="61703-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61703-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61703-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61703-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61703-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61703-144">CommonParameters</span></span>
<span data-ttu-id="61703-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61703-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61703-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61703-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61703-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61703-147">INPUTS</span></span>

### <span data-ttu-id="61703-148">System. String</span><span class="sxs-lookup"><span data-stu-id="61703-148">System.String</span></span>

### <span data-ttu-id="61703-149">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="61703-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="61703-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61703-150">OUTPUTS</span></span>

### <span data-ttu-id="61703-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="61703-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="61703-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61703-152">NOTES</span></span>

## <span data-ttu-id="61703-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61703-153">RELATED LINKS</span></span>
