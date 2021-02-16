---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195610"
---
# <span data-ttu-id="394e2-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="394e2-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="394e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394e2-102">SYNOPSIS</span></span>
<span data-ttu-id="394e2-103">Pobiera zalecane typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="394e2-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="394e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="394e2-104">SYNTAX</span></span>

### <span data-ttu-id="394e2-105">SqlPoolObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="394e2-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="394e2-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="394e2-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="394e2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="394e2-107">DESCRIPTION</span></span>
<span data-ttu-id="394e2-108">Polecenie Get-AzSynapseSqlPoolSensitivityRecommendation zwraca zalecane typy informacji i etykiety wrażliwości kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="394e2-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="394e2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="394e2-109">EXAMPLES</span></span>

### <span data-ttu-id="394e2-110">Przykład 1. Uzyskaj zalecane typy informacji i etykiety wrażliwości puli języka SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="394e2-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="394e2-111">Przykład 2. Uzyskaj zalecane typy informacji i etykiety wrażliwości puli języka SQL Azure Synapse przy użyciu usługi Piping.</span><span class="sxs-lookup"><span data-stu-id="394e2-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="394e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="394e2-112">PARAMETERS</span></span>

### <span data-ttu-id="394e2-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="394e2-113">-AsJob</span></span>
<span data-ttu-id="394e2-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="394e2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="394e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394e2-115">-DefaultProfile</span></span>
<span data-ttu-id="394e2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="394e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="394e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="394e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="394e2-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="394e2-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e2-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="394e2-119">-SqlPoolName</span></span>
<span data-ttu-id="394e2-120">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="394e2-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e2-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="394e2-121">-SqlPoolObject</span></span>
<span data-ttu-id="394e2-122">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="394e2-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="394e2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="394e2-123">-WorkspaceName</span></span>
<span data-ttu-id="394e2-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="394e2-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394e2-125">CommonParameters</span></span>
<span data-ttu-id="394e2-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="394e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394e2-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="394e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394e2-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="394e2-128">INPUTS</span></span>

### <span data-ttu-id="394e2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="394e2-129">System.String</span></span>

### <span data-ttu-id="394e2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="394e2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="394e2-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="394e2-131">OUTPUTS</span></span>

### <span data-ttu-id="394e2-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="394e2-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="394e2-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="394e2-133">NOTES</span></span>

## <span data-ttu-id="394e2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="394e2-134">RELATED LINKS</span></span>
