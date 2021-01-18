---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 6b07ba5e31ab8e301d94b50170aca3869f9dea65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501349"
---
# <span data-ttu-id="a2d11-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a2d11-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="a2d11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2d11-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d11-103">Pobiera ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2d11-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="a2d11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2d11-104">SYNTAX</span></span>

### <span data-ttu-id="a2d11-105">ServerParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2d11-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d11-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d11-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2d11-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a2d11-107">DESCRIPTION</span></span>
<span data-ttu-id="a2d11-108">Polecenie cmdlet **Get-AzSqlServerAudit** pobiera ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2d11-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="a2d11-109">Określ parametry *ResourceGroupName* i *nazwa_serwera* identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="a2d11-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="a2d11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2d11-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d11-111">Przykład 1: uzyskiwanie ustawień inspekcji usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2d11-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="a2d11-112">Przykład 2: Get, za pośrednictwem rurociągu — ustawienia inspekcji programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2d11-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="a2d11-113">Przykład 3: uzyskiwanie ustawień inspekcji dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2d11-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="a2d11-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2d11-114">PARAMETERS</span></span>

### <span data-ttu-id="a2d11-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2d11-115">-AsJob</span></span>
<span data-ttu-id="a2d11-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a2d11-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2d11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d11-117">-DefaultProfile</span></span>
<span data-ttu-id="a2d11-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d11-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d11-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d11-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2d11-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2d11-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d11-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a2d11-121">-ServerName</span></span>
<span data-ttu-id="a2d11-122">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="a2d11-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d11-123">-Serverobject</span><span class="sxs-lookup"><span data-stu-id="a2d11-123">-ServerObject</span></span>
<span data-ttu-id="a2d11-124">Obiekt serwera do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="a2d11-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d11-125">CommonParameters</span></span>
<span data-ttu-id="a2d11-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d11-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2d11-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d11-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2d11-128">INPUTS</span></span>

### <span data-ttu-id="a2d11-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d11-129">System.String</span></span>

### <span data-ttu-id="a2d11-130">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a2d11-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a2d11-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2d11-131">OUTPUTS</span></span>

### <span data-ttu-id="a2d11-132">Microsoft. Azure. Commands. SQL. Audit. model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="a2d11-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="a2d11-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2d11-133">NOTES</span></span>

## <span data-ttu-id="a2d11-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2d11-134">RELATED LINKS</span></span>
