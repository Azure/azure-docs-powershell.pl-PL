---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383840"
---
# <span data-ttu-id="5f97c-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="5f97c-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="5f97c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f97c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f97c-103">Pobiera bieżące typy informacji oraz etykiety liter kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="5f97c-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="5f97c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f97c-104">SYNTAX</span></span>

### <span data-ttu-id="5f97c-105">SqlPoolObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f97c-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f97c-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f97c-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f97c-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f97c-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f97c-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f97c-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f97c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5f97c-109">DESCRIPTION</span></span>
<span data-ttu-id="5f97c-110">Polecenie cmdlet Get-AzSynapseSqlPoolSensitivityClassification zwraca bieżące typy informacji oraz etykiety liter kolumn w puli usługi Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="5f97c-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="5f97c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f97c-111">EXAMPLES</span></span>

### <span data-ttu-id="5f97c-112">Przykład 1: pobieranie bieżących typów informacji i etykiet wrażliwości puli usługi Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="5f97c-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="5f97c-113">Przykład 2: pobieranie bieżących typów informacji i etykiet wrażliwości puli usługi Azure Synapse SQL z potokiem.</span><span class="sxs-lookup"><span data-stu-id="5f97c-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
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

### <span data-ttu-id="5f97c-114">Przykład 3: uzyskiwanie informacji o bieżącym typie i wrażliwości konkretnej kolumny w puli usługi Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="5f97c-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="5f97c-115">Przykład 4: uzyskiwanie bieżącego typu informacji i etykiety wrażliwości określonej kolumny puli usługi Azure Synapse SQL przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="5f97c-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="5f97c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f97c-116">PARAMETERS</span></span>

### <span data-ttu-id="5f97c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f97c-117">-AsJob</span></span>
<span data-ttu-id="5f97c-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5f97c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f97c-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5f97c-119">-ColumnName</span></span>
<span data-ttu-id="5f97c-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="5f97c-120">Name of column.</span></span>

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

### <span data-ttu-id="5f97c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f97c-121">-DefaultProfile</span></span>
<span data-ttu-id="5f97c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f97c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f97c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f97c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f97c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f97c-124">Resource group name.</span></span>

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

### <span data-ttu-id="5f97c-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5f97c-125">-SchemaName</span></span>
<span data-ttu-id="5f97c-126">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="5f97c-126">Name of schema.</span></span>

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

### <span data-ttu-id="5f97c-127">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="5f97c-127">-SqlPoolName</span></span>
<span data-ttu-id="5f97c-128">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5f97c-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5f97c-129">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="5f97c-129">-SqlPoolObject</span></span>
<span data-ttu-id="5f97c-130">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5f97c-130">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5f97c-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="5f97c-131">-TableName</span></span>
<span data-ttu-id="5f97c-132">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="5f97c-132">Name of table.</span></span>

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

### <span data-ttu-id="5f97c-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5f97c-133">-WorkspaceName</span></span>
<span data-ttu-id="5f97c-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5f97c-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5f97c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f97c-135">CommonParameters</span></span>
<span data-ttu-id="5f97c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f97c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f97c-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f97c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f97c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f97c-138">INPUTS</span></span>

### <span data-ttu-id="5f97c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5f97c-139">System.String</span></span>

### <span data-ttu-id="5f97c-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5f97c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5f97c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f97c-141">OUTPUTS</span></span>

### <span data-ttu-id="5f97c-142">Microsoft. Azure. Commands. Synapse. models. dataklasyfikacyjn. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5f97c-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="5f97c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f97c-143">NOTES</span></span>

## <span data-ttu-id="5f97c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f97c-144">RELATED LINKS</span></span>
