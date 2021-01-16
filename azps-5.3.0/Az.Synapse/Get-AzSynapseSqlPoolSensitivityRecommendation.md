---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383817"
---
# <span data-ttu-id="cd3bf-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="cd3bf-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="cd3bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3bf-103">Pobiera Polecane typy informacji i etykiety wrażliwości kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="cd3bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd3bf-104">SYNTAX</span></span>

### <span data-ttu-id="cd3bf-105">SqlPoolObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd3bf-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd3bf-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd3bf-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3bf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd3bf-107">DESCRIPTION</span></span>
<span data-ttu-id="cd3bf-108">Polecenie cmdlet Get-AzSynapseSqlPoolSensitivityRecommendation zwraca Zalecane typy informacji oraz etykiety wrażliwości kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="cd3bf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd3bf-109">EXAMPLES</span></span>

### <span data-ttu-id="cd3bf-110">Przykład 1: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości puli platformy Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="cd3bf-111">Przykład 2: uzyskiwanie zalecanych typów informacji i etykiet wrażliwości puli usługi Azure Synapse SQL przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="cd3bf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd3bf-112">PARAMETERS</span></span>

### <span data-ttu-id="cd3bf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd3bf-113">-AsJob</span></span>
<span data-ttu-id="cd3bf-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cd3bf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd3bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3bf-115">-DefaultProfile</span></span>
<span data-ttu-id="cd3bf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd3bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd3bf-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-118">Resource group name.</span></span>

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

### <span data-ttu-id="cd3bf-119">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="cd3bf-119">-SqlPoolName</span></span>
<span data-ttu-id="cd3bf-120">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="cd3bf-121">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="cd3bf-121">-SqlPoolObject</span></span>
<span data-ttu-id="cd3bf-122">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cd3bf-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cd3bf-123">-WorkspaceName</span></span>
<span data-ttu-id="cd3bf-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cd3bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3bf-125">CommonParameters</span></span>
<span data-ttu-id="cd3bf-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3bf-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd3bf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3bf-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd3bf-128">INPUTS</span></span>

### <span data-ttu-id="cd3bf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3bf-129">System.String</span></span>

### <span data-ttu-id="cd3bf-130">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cd3bf-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cd3bf-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd3bf-131">OUTPUTS</span></span>

### <span data-ttu-id="cd3bf-132">Microsoft. Azure. Commands. Synapse. models. dataklasyfikacyjn. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="cd3bf-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="cd3bf-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd3bf-133">NOTES</span></span>

## <span data-ttu-id="cd3bf-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd3bf-134">RELATED LINKS</span></span>
