---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 62894b5d879febdeeb7c14360c16c66fb8a28ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983962"
---
# <span data-ttu-id="8df13-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8df13-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="8df13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df13-102">SYNOPSIS</span></span>
<span data-ttu-id="8df13-103">Wywoływanie instrukcji Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="8df13-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8df13-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8df13-104">SYNTAX</span></span>

### <span data-ttu-id="8df13-105">RunSparkStatementByCodePathParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8df13-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df13-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df13-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df13-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df13-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8df13-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df13-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8df13-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8df13-109">DESCRIPTION</span></span>
<span data-ttu-id="8df13-110">Polecenie **cmdlet Invoke-AzSynapseSparkStatement** wywołuje instrukcja Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="8df13-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8df13-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8df13-111">EXAMPLES</span></span>

### <span data-ttu-id="8df13-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8df13-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="8df13-113">Te polecenia uruchamiają sesję przebiegu w trakcie, a następnie wywołują w tekście instrukcja Przebiegu w przebiegu w potoku.</span><span class="sxs-lookup"><span data-stu-id="8df13-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="8df13-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8df13-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="8df13-115">Te polecenia uruchom sesję przebiegu w przebiegu w trakcie, a następnie wywołaj w tekście instrukcja Spark.</span><span class="sxs-lookup"><span data-stu-id="8df13-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="8df13-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8df13-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="8df13-117">Te polecenia uruchamiają sesję przebiegu w trakcie, a następnie wywołują instrukcje przebiegu w przebiegu w pliku.</span><span class="sxs-lookup"><span data-stu-id="8df13-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="8df13-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8df13-118">PARAMETERS</span></span>

### <span data-ttu-id="8df13-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8df13-119">-AsJob</span></span>
<span data-ttu-id="8df13-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8df13-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8df13-121">— Kod</span><span class="sxs-lookup"><span data-stu-id="8df13-121">-Code</span></span>
<span data-ttu-id="8df13-122">Kod wykonywania.</span><span class="sxs-lookup"><span data-stu-id="8df13-122">The execution code.</span></span>

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

### <span data-ttu-id="8df13-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df13-123">-DefaultProfile</span></span>
<span data-ttu-id="8df13-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8df13-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8df13-125">- FilePath</span><span class="sxs-lookup"><span data-stu-id="8df13-125">-FilePath</span></span>
<span data-ttu-id="8df13-126">Określa lokalną ścieżkę pliku zawierającą kod wykonywania.</span><span class="sxs-lookup"><span data-stu-id="8df13-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="8df13-127">— język</span><span class="sxs-lookup"><span data-stu-id="8df13-127">-Language</span></span>
<span data-ttu-id="8df13-128">Język kodu wykonywania.</span><span class="sxs-lookup"><span data-stu-id="8df13-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="8df13-129">— Odpowiedź</span><span class="sxs-lookup"><span data-stu-id="8df13-129">-Response</span></span>
<span data-ttu-id="8df13-130">Wskazuje, że powinna zostać zwrócona pełna odpowiedź.</span><span class="sxs-lookup"><span data-stu-id="8df13-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="8df13-131">- SessionId</span><span class="sxs-lookup"><span data-stu-id="8df13-131">-SessionId</span></span>
<span data-ttu-id="8df13-132">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="8df13-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="8df13-133">- SessionObject</span><span class="sxs-lookup"><span data-stu-id="8df13-133">-SessionObject</span></span>
<span data-ttu-id="8df13-134">Obiekt wprowadzania sesji przebiegu w przebiegu w trakcie przebiegu w trakcie potoku.</span><span class="sxs-lookup"><span data-stu-id="8df13-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8df13-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8df13-135">-SparkPoolName</span></span>
<span data-ttu-id="8df13-136">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="8df13-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8df13-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8df13-137">-WorkspaceName</span></span>
<span data-ttu-id="8df13-138">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="8df13-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8df13-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8df13-139">-Confirm</span></span>
<span data-ttu-id="8df13-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8df13-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df13-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df13-141">-WhatIf</span></span>
<span data-ttu-id="8df13-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8df13-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8df13-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8df13-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df13-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df13-144">CommonParameters</span></span>
<span data-ttu-id="8df13-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df13-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df13-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8df13-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df13-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8df13-147">INPUTS</span></span>

### <span data-ttu-id="8df13-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8df13-148">System.String</span></span>

### <span data-ttu-id="8df13-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8df13-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8df13-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8df13-150">OUTPUTS</span></span>

### <span data-ttu-id="8df13-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8df13-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="8df13-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8df13-152">NOTES</span></span>

## <span data-ttu-id="8df13-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8df13-153">RELATED LINKS</span></span>
