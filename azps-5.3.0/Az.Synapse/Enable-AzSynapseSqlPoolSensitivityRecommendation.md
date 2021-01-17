---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491121"
---
# <span data-ttu-id="f03a1-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f03a1-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="f03a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f03a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f03a1-103">Włączanie rekomendacji dotyczących wrażliwości na kolumny (rekomendacje są domyślnie włączone we wszystkich kolumnach) w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="f03a1-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="f03a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f03a1-104">SYNTAX</span></span>

### <span data-ttu-id="f03a1-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f03a1-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f03a1-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f03a1-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f03a1-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f03a1-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f03a1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f03a1-108">DESCRIPTION</span></span>
<span data-ttu-id="f03a1-109">Polecenie cmdlet Enable-AzSynapseSqlPoolSensitivityRecommendation włącza zalecenia dotyczące wrażliwości na kolumny w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="f03a1-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="f03a1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f03a1-110">EXAMPLES</span></span>

### <span data-ttu-id="f03a1-111">Przykład 1: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny w puli usługi Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="f03a1-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f03a1-112">Przykład 2: Włączanie rekomendacji dotyczących wrażliwości dla danej kolumny puli usługi Azure Synapse SQL przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="f03a1-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f03a1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f03a1-113">PARAMETERS</span></span>

### <span data-ttu-id="f03a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03a1-114">-AsJob</span></span>
<span data-ttu-id="f03a1-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f03a1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f03a1-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f03a1-116">-ColumnName</span></span>
<span data-ttu-id="f03a1-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="f03a1-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03a1-118">-DefaultProfile</span></span>
<span data-ttu-id="f03a1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f03a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03a1-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f03a1-120">-InputObject</span></span>
<span data-ttu-id="f03a1-121">Obiekt reprezentujący klasyfikację wrażliwości puli SQL.</span><span class="sxs-lookup"><span data-stu-id="f03a1-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f03a1-122">-PassThru</span></span>
<span data-ttu-id="f03a1-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f03a1-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f03a1-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="f03a1-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f03a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="f03a1-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f03a1-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f03a1-127">-SchemaName</span></span>
<span data-ttu-id="f03a1-128">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="f03a1-128">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-129">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="f03a1-129">-SqlPoolName</span></span>
<span data-ttu-id="f03a1-130">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f03a1-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-131">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="f03a1-131">-SqlPoolObject</span></span>
<span data-ttu-id="f03a1-132">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f03a1-132">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="f03a1-133">-TableName</span></span>
<span data-ttu-id="f03a1-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="f03a1-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-135">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f03a1-135">-WorkspaceName</span></span>
<span data-ttu-id="f03a1-136">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f03a1-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03a1-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f03a1-137">-Confirm</span></span>
<span data-ttu-id="f03a1-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f03a1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03a1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03a1-139">-WhatIf</span></span>
<span data-ttu-id="f03a1-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f03a1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03a1-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f03a1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03a1-142">CommonParameters</span></span>
<span data-ttu-id="f03a1-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03a1-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f03a1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03a1-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f03a1-145">INPUTS</span></span>

### <span data-ttu-id="f03a1-146">Microsoft. Azure. Commands. Synapse. models. dataklasyfikacyjn. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f03a1-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="f03a1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f03a1-147">System.String</span></span>

### <span data-ttu-id="f03a1-148">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f03a1-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f03a1-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f03a1-149">OUTPUTS</span></span>

### <span data-ttu-id="f03a1-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f03a1-150">System.Boolean</span></span>

## <span data-ttu-id="f03a1-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f03a1-151">NOTES</span></span>

## <span data-ttu-id="f03a1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f03a1-152">RELATED LINKS</span></span>
