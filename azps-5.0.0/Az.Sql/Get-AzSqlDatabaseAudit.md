---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225660"
---
# <span data-ttu-id="706a9-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="706a9-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="706a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="706a9-102">SYNOPSIS</span></span>
<span data-ttu-id="706a9-103">Pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="706a9-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="706a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="706a9-104">SYNTAX</span></span>

### <span data-ttu-id="706a9-105">DatabaseParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="706a9-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="706a9-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="706a9-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="706a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="706a9-107">DESCRIPTION</span></span>
<span data-ttu-id="706a9-108">Polecenie cmdlet **Get-AzSqlDatabaseAudit** pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="706a9-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="706a9-109">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="706a9-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="706a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="706a9-110">EXAMPLES</span></span>

### <span data-ttu-id="706a9-111">Przykład 1: uzyskiwanie ustawień inspekcji bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="706a9-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="706a9-112">Przykład 2: uzyskiwanie, za pośrednictwem rurociągu, ustawienia inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="706a9-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="706a9-113">Przykład 3: uzyskiwanie ustawień inspekcji bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="706a9-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="706a9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="706a9-114">PARAMETERS</span></span>

### <span data-ttu-id="706a9-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="706a9-115">-DatabaseName</span></span>
<span data-ttu-id="706a9-116">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="706a9-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706a9-117">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="706a9-117">-DatabaseObject</span></span>
<span data-ttu-id="706a9-118">Obiekt bazy danych do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="706a9-118">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="706a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706a9-119">-DefaultProfile</span></span>
<span data-ttu-id="706a9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="706a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="706a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="706a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="706a9-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="706a9-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706a9-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="706a9-123">-ServerName</span></span>
<span data-ttu-id="706a9-124">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="706a9-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706a9-125">CommonParameters</span></span>
<span data-ttu-id="706a9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706a9-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="706a9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706a9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="706a9-128">INPUTS</span></span>

### <span data-ttu-id="706a9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="706a9-129">System.String</span></span>

### <span data-ttu-id="706a9-130">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="706a9-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="706a9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="706a9-131">OUTPUTS</span></span>

### <span data-ttu-id="706a9-132">Microsoft. Azure. Commands. SQL. Audit. model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="706a9-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="706a9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="706a9-133">NOTES</span></span>

## <span data-ttu-id="706a9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="706a9-134">RELATED LINKS</span></span>
