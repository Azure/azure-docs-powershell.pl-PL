---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491126"
---
# <span data-ttu-id="bc38b-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="bc38b-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="bc38b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc38b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc38b-103">Wyłączenie (odrzucanie) rekomendacji dotyczących wrażliwości na kolumny w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="bc38b-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="bc38b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc38b-104">SYNTAX</span></span>

### <span data-ttu-id="bc38b-105">InputObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc38b-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc38b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc38b-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc38b-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc38b-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc38b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc38b-108">DESCRIPTION</span></span>
<span data-ttu-id="bc38b-109">Polecenie cmdlet Disable-AzSynapseSqlPoolSensitivityRecommendation wyłącza (odrzuca) zalecenia dotyczące wrażliwości na kolumny w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="bc38b-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="bc38b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc38b-110">EXAMPLES</span></span>

### <span data-ttu-id="bc38b-111">Przykład 1: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w puli usługi Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="bc38b-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="bc38b-112">Przykład 2: wyłączanie zaleceń dotyczących wrażliwości na kolumny, które mają rekomendacje dotyczące wrażliwości w puli usługi Azure Synapse SQL, korzystając z połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="bc38b-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="bc38b-113">Przykład 3: wyłączanie rekomendacji dotyczących wrażliwości dla danej kolumny w puli usługi Azure Synapse SQL przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="bc38b-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="bc38b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc38b-114">PARAMETERS</span></span>

### <span data-ttu-id="bc38b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc38b-115">-AsJob</span></span>
<span data-ttu-id="bc38b-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bc38b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc38b-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="bc38b-117">-ColumnName</span></span>
<span data-ttu-id="bc38b-118">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="bc38b-118">Name of column.</span></span>

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

### <span data-ttu-id="bc38b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc38b-119">-DefaultProfile</span></span>
<span data-ttu-id="bc38b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc38b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc38b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc38b-121">-InputObject</span></span>
<span data-ttu-id="bc38b-122">Obiekt reprezentujący klasyfikację wrażliwości puli SQL.</span><span class="sxs-lookup"><span data-stu-id="bc38b-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="bc38b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc38b-123">-PassThru</span></span>
<span data-ttu-id="bc38b-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="bc38b-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bc38b-125">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="bc38b-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bc38b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc38b-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc38b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc38b-127">Resource group name.</span></span>

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

### <span data-ttu-id="bc38b-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bc38b-128">-SchemaName</span></span>
<span data-ttu-id="bc38b-129">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="bc38b-129">Name of schema.</span></span>

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

### <span data-ttu-id="bc38b-130">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="bc38b-130">-SqlPoolName</span></span>
<span data-ttu-id="bc38b-131">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="bc38b-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="bc38b-132">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="bc38b-132">-SqlPoolObject</span></span>
<span data-ttu-id="bc38b-133">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="bc38b-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bc38b-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="bc38b-134">-TableName</span></span>
<span data-ttu-id="bc38b-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="bc38b-135">Name of table.</span></span>

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

### <span data-ttu-id="bc38b-136">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="bc38b-136">-WorkspaceName</span></span>
<span data-ttu-id="bc38b-137">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="bc38b-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bc38b-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc38b-138">-Confirm</span></span>
<span data-ttu-id="bc38b-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc38b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc38b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc38b-140">-WhatIf</span></span>
<span data-ttu-id="bc38b-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc38b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc38b-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc38b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc38b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc38b-143">CommonParameters</span></span>
<span data-ttu-id="bc38b-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc38b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc38b-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc38b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc38b-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc38b-146">INPUTS</span></span>

### <span data-ttu-id="bc38b-147">Microsoft. Azure. Commands. Synapse. models. dataklasyfikacyjn. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="bc38b-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="bc38b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bc38b-148">System.String</span></span>

### <span data-ttu-id="bc38b-149">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bc38b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bc38b-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc38b-150">OUTPUTS</span></span>

### <span data-ttu-id="bc38b-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc38b-151">System.Boolean</span></span>

## <span data-ttu-id="bc38b-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc38b-152">NOTES</span></span>

## <span data-ttu-id="bc38b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc38b-153">RELATED LINKS</span></span>
