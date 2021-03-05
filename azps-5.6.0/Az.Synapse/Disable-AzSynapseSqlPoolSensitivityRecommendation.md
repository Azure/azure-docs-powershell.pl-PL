---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: a9085433bb888fa8e37405881a20a55a4f08b96d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961105"
---
# <span data-ttu-id="66d0f-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="66d0f-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="66d0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="66d0f-103">Wyłącza (odrzuca) zalecenia dotyczące wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="66d0f-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="66d0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66d0f-104">SYNTAX</span></span>

### <span data-ttu-id="66d0f-105">InputObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="66d0f-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d0f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d0f-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d0f-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="66d0f-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d0f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="66d0f-108">DESCRIPTION</span></span>
<span data-ttu-id="66d0f-109">Polecenie Disable-AzSynapseSqlPoolSensitivityRecommendation wyłącza (odrzuca) zalecenia dotyczące wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="66d0f-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="66d0f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66d0f-110">EXAMPLES</span></span>

### <span data-ttu-id="66d0f-111">Przykład 1. Wyłączanie rekomendacji wrażliwości dla danej kolumny w puli sql Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="66d0f-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="66d0f-112">Przykład 2. Wyłącz zalecenia dotyczące wrażliwości dla kolumn, które mają zalecenia wrażliwości w puli sql Synapse Azure przy użyciu funkcji Piping.</span><span class="sxs-lookup"><span data-stu-id="66d0f-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="66d0f-113">Przykład 3. Wyłączanie rekomendacji wrażliwości dla danej kolumny w puli sql Synapse Azure przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="66d0f-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="66d0f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66d0f-114">PARAMETERS</span></span>

### <span data-ttu-id="66d0f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="66d0f-115">-AsJob</span></span>
<span data-ttu-id="66d0f-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="66d0f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66d0f-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="66d0f-117">-ColumnName</span></span>
<span data-ttu-id="66d0f-118">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="66d0f-118">Name of column.</span></span>

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

### <span data-ttu-id="66d0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d0f-119">-DefaultProfile</span></span>
<span data-ttu-id="66d0f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66d0f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d0f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66d0f-121">-InputObject</span></span>
<span data-ttu-id="66d0f-122">Obiekt reprezentujący klasyfikację wrażliwości puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="66d0f-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="66d0f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66d0f-123">-PassThru</span></span>
<span data-ttu-id="66d0f-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="66d0f-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="66d0f-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="66d0f-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="66d0f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d0f-126">-ResourceGroupName</span></span>
<span data-ttu-id="66d0f-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66d0f-127">Resource group name.</span></span>

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

### <span data-ttu-id="66d0f-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="66d0f-128">-SchemaName</span></span>
<span data-ttu-id="66d0f-129">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="66d0f-129">Name of schema.</span></span>

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

### <span data-ttu-id="66d0f-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="66d0f-130">-SqlPoolName</span></span>
<span data-ttu-id="66d0f-131">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="66d0f-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="66d0f-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="66d0f-132">-SqlPoolObject</span></span>
<span data-ttu-id="66d0f-133">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="66d0f-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="66d0f-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="66d0f-134">-TableName</span></span>
<span data-ttu-id="66d0f-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="66d0f-135">Name of table.</span></span>

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

### <span data-ttu-id="66d0f-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66d0f-136">-WorkspaceName</span></span>
<span data-ttu-id="66d0f-137">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="66d0f-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="66d0f-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66d0f-138">-Confirm</span></span>
<span data-ttu-id="66d0f-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="66d0f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d0f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d0f-140">-WhatIf</span></span>
<span data-ttu-id="66d0f-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66d0f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d0f-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="66d0f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d0f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d0f-143">CommonParameters</span></span>
<span data-ttu-id="66d0f-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d0f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d0f-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66d0f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d0f-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66d0f-146">INPUTS</span></span>

### <span data-ttu-id="66d0f-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="66d0f-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="66d0f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="66d0f-148">System.String</span></span>

### <span data-ttu-id="66d0f-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66d0f-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="66d0f-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66d0f-150">OUTPUTS</span></span>

### <span data-ttu-id="66d0f-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66d0f-151">System.Boolean</span></span>

## <span data-ttu-id="66d0f-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66d0f-152">NOTES</span></span>

## <span data-ttu-id="66d0f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66d0f-153">RELATED LINKS</span></span>
