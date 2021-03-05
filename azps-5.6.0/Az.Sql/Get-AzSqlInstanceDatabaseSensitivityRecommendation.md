---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 0d40e03b26481b5e974b294533566549646ba628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999402"
---
# <span data-ttu-id="067bf-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="067bf-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="067bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="067bf-102">SYNOPSIS</span></span>
<span data-ttu-id="067bf-103">Pobiera zalecane typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="067bf-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="067bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="067bf-104">SYNTAX</span></span>

### <span data-ttu-id="067bf-105">DatabaseObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="067bf-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="067bf-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="067bf-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="067bf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="067bf-107">DESCRIPTION</span></span>
<span data-ttu-id="067bf-108">Polecenie Get-AzSqlInstanceDatabaseSensitivityRecommendation zwraca zalecane typy informacji i etykiety wrażliwości kolumn w bazie danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="067bf-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="067bf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="067bf-109">EXAMPLES</span></span>

### <span data-ttu-id="067bf-110">Przykład 1. Uzyskaj zalecane typy informacji i etykiety wrażliwości bazy danych azure SQL managed instance.</span><span class="sxs-lookup"><span data-stu-id="067bf-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

### <span data-ttu-id="067bf-111">Przykład 2. Uzyskaj zalecane typy informacji i etykiety wrażliwości bazy danych azure SQL managed instance przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="067bf-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

## <span data-ttu-id="067bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="067bf-112">PARAMETERS</span></span>

### <span data-ttu-id="067bf-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="067bf-113">-AsJob</span></span>
<span data-ttu-id="067bf-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="067bf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="067bf-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="067bf-115">-DatabaseName</span></span>
<span data-ttu-id="067bf-116">Nazwa bazy danych azure SQL managed instance database.</span><span class="sxs-lookup"><span data-stu-id="067bf-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067bf-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="067bf-117">-DatabaseObject</span></span>
<span data-ttu-id="067bf-118">Obiekt bazy danych zarządzanych wystąpień sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="067bf-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="067bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067bf-119">-DefaultProfile</span></span>
<span data-ttu-id="067bf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="067bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="067bf-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="067bf-121">-InstanceName</span></span>
<span data-ttu-id="067bf-122">Nazwa zarządzanego wystąpienia języka SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="067bf-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="067bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="067bf-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="067bf-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067bf-125">CommonParameters</span></span>
<span data-ttu-id="067bf-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="067bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067bf-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="067bf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067bf-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="067bf-128">INPUTS</span></span>

### <span data-ttu-id="067bf-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="067bf-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="067bf-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="067bf-130">OUTPUTS</span></span>

### <span data-ttu-id="067bf-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="067bf-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="067bf-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="067bf-132">NOTES</span></span>

## <span data-ttu-id="067bf-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="067bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="067bf-134">Dowiedz się więcej o odnajdowania i klasyfikacji danych usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="067bf-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
