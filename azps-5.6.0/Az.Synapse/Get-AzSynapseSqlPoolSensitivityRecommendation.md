---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985503"
---
# <span data-ttu-id="aa4b7-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="aa4b7-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="aa4b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4b7-103">Pobiera zalecane typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="aa4b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa4b7-104">SYNTAX</span></span>

### <span data-ttu-id="aa4b7-105">SqlPoolObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="aa4b7-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa4b7-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4b7-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa4b7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa4b7-107">DESCRIPTION</span></span>
<span data-ttu-id="aa4b7-108">Polecenie Get-AzSynapseSqlPoolSensitivityRecommendation zwraca zalecane typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="aa4b7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa4b7-109">EXAMPLES</span></span>

### <span data-ttu-id="aa4b7-110">Przykład 1. Uzyskaj zalecane typy informacji i etykiety wrażliwości puli języka SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="aa4b7-111">Przykład 2. Uzyskaj zalecane typy informacji i etykiety wrażliwości puli sql Azure Synapse przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="aa4b7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa4b7-112">PARAMETERS</span></span>

### <span data-ttu-id="aa4b7-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="aa4b7-113">-AsJob</span></span>
<span data-ttu-id="aa4b7-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="aa4b7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa4b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4b7-115">-DefaultProfile</span></span>
<span data-ttu-id="aa4b7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa4b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa4b7-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-118">Resource group name.</span></span>

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

### <span data-ttu-id="aa4b7-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="aa4b7-119">-SqlPoolName</span></span>
<span data-ttu-id="aa4b7-120">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="aa4b7-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="aa4b7-121">-SqlPoolObject</span></span>
<span data-ttu-id="aa4b7-122">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="aa4b7-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aa4b7-123">-WorkspaceName</span></span>
<span data-ttu-id="aa4b7-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="aa4b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4b7-125">CommonParameters</span></span>
<span data-ttu-id="aa4b7-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4b7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa4b7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4b7-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa4b7-128">INPUTS</span></span>

### <span data-ttu-id="aa4b7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="aa4b7-129">System.String</span></span>

### <span data-ttu-id="aa4b7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="aa4b7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="aa4b7-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa4b7-131">OUTPUTS</span></span>

### <span data-ttu-id="aa4b7-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="aa4b7-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="aa4b7-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa4b7-133">NOTES</span></span>

## <span data-ttu-id="aa4b7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa4b7-134">RELATED LINKS</span></span>
