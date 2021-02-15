---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197363"
---
# <span data-ttu-id="d12ac-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="d12ac-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="d12ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d12ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d12ac-103">Pobiera bieżące typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="d12ac-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="d12ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d12ac-104">SYNTAX</span></span>

### <span data-ttu-id="d12ac-105">SqlPoolObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d12ac-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12ac-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="d12ac-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12ac-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d12ac-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12ac-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d12ac-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d12ac-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d12ac-109">DESCRIPTION</span></span>
<span data-ttu-id="d12ac-110">Polecenie Get-AzSynapseSqlPoolSensitivityClassification zwraca bieżące typy informacji i etykiety wrażliwości kolumn w puli SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="d12ac-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="d12ac-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d12ac-111">EXAMPLES</span></span>

### <span data-ttu-id="d12ac-112">Przykład 1. Uzyskiwanie bieżących typów informacji i etykiet wrażliwości puli języka SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="d12ac-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="d12ac-113">Przykład 2. Uzyskaj bieżące typy informacji i etykiety wrażliwości puli SQL Synapse platformy Azure z usługą Piping.</span><span class="sxs-lookup"><span data-stu-id="d12ac-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="d12ac-114">Przykład 3. Uzyskaj bieżący typ informacji i etykietę wrażliwości konkretnej kolumny puli sql Synapse platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d12ac-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="d12ac-115">Przykład 4. Pobierz bieżący typ informacji i etykietę wrażliwości określonej kolumny puli sql Synapse platformy Azure przy użyciu usługi Piping.</span><span class="sxs-lookup"><span data-stu-id="d12ac-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="d12ac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d12ac-116">PARAMETERS</span></span>

### <span data-ttu-id="d12ac-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d12ac-117">-AsJob</span></span>
<span data-ttu-id="d12ac-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d12ac-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d12ac-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="d12ac-119">-ColumnName</span></span>
<span data-ttu-id="d12ac-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="d12ac-120">Name of column.</span></span>

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

### <span data-ttu-id="d12ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12ac-121">-DefaultProfile</span></span>
<span data-ttu-id="d12ac-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d12ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d12ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="d12ac-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d12ac-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ac-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d12ac-125">-SchemaName</span></span>
<span data-ttu-id="d12ac-126">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="d12ac-126">Name of schema.</span></span>

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

### <span data-ttu-id="d12ac-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="d12ac-127">-SqlPoolName</span></span>
<span data-ttu-id="d12ac-128">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d12ac-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ac-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="d12ac-129">-SqlPoolObject</span></span>
<span data-ttu-id="d12ac-130">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="d12ac-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ac-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="d12ac-131">-TableName</span></span>
<span data-ttu-id="d12ac-132">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="d12ac-132">Name of table.</span></span>

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

### <span data-ttu-id="d12ac-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d12ac-133">-WorkspaceName</span></span>
<span data-ttu-id="d12ac-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d12ac-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12ac-135">CommonParameters</span></span>
<span data-ttu-id="d12ac-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12ac-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d12ac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12ac-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d12ac-138">INPUTS</span></span>

### <span data-ttu-id="d12ac-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d12ac-139">System.String</span></span>

### <span data-ttu-id="d12ac-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d12ac-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d12ac-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d12ac-141">OUTPUTS</span></span>

### <span data-ttu-id="d12ac-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="d12ac-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="d12ac-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d12ac-143">NOTES</span></span>

## <span data-ttu-id="d12ac-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d12ac-144">RELATED LINKS</span></span>
