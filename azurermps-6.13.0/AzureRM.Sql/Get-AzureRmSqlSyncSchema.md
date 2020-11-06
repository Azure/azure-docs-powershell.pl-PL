---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 38e56102ba544bc56384f0d3ff59bdc8091bdd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552024"
---
# <span data-ttu-id="675c4-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="675c4-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="675c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="675c4-102">SYNOPSIS</span></span>
<span data-ttu-id="675c4-103">Zwraca informacje o schemacie synchronizacji bazy danych członka lub centralnej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="675c4-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="675c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="675c4-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="675c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="675c4-105">DESCRIPTION</span></span>
<span data-ttu-id="675c4-106">Polecenie cmdlet **Get-AzureRmSqlSyncSchema** zwraca informacje o schemacie synchronizacji bazy danych członka lub centralnej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="675c4-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="675c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="675c4-107">EXAMPLES</span></span>

### <span data-ttu-id="675c4-108">Przykład 1,1: uzyskiwanie schematu synchronizacji dla bazy danych centrum</span><span class="sxs-lookup"><span data-stu-id="675c4-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="675c4-109">To polecenie pobiera schemat synchronizacji dla bazy danych centrum w grupie Sync syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="675c4-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="675c4-110">Przykład 1,2: uzyskiwanie schematu synchronizacji dla bazy danych centrum i rozszerzanie tabel</span><span class="sxs-lookup"><span data-stu-id="675c4-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="675c4-111">To polecenie pobiera schemat synchronizacji dla bazy danych centrum w właściwości Group Sync syncGroup01 i expand Tables.</span><span class="sxs-lookup"><span data-stu-id="675c4-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="675c4-112">Przykład 2: uzyskiwanie schematu synchronizacji dla bazy danych członka</span><span class="sxs-lookup"><span data-stu-id="675c4-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="675c4-113">To polecenie pobiera schemat synchronizacji dla bazy danych elementu członkowskiego w synchronizowanej członku syncMember01.</span><span class="sxs-lookup"><span data-stu-id="675c4-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="675c4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="675c4-114">PARAMETERS</span></span>

### <span data-ttu-id="675c4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="675c4-115">-DatabaseName</span></span>
<span data-ttu-id="675c4-116">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="675c4-116">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675c4-117">-DefaultProfile</span></span>
<span data-ttu-id="675c4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="675c4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="675c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="675c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="675c4-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="675c4-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675c4-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="675c4-121">-ServerName</span></span>
<span data-ttu-id="675c4-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="675c4-122">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675c4-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="675c4-123">-SyncGroupName</span></span>
<span data-ttu-id="675c4-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="675c4-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675c4-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="675c4-125">-SyncMemberName</span></span>
<span data-ttu-id="675c4-126">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="675c4-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675c4-127">CommonParameters</span></span>
<span data-ttu-id="675c4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="675c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675c4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="675c4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675c4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="675c4-130">INPUTS</span></span>

### <span data-ttu-id="675c4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="675c4-131">System.String</span></span>

## <span data-ttu-id="675c4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="675c4-132">OUTPUTS</span></span>

### <span data-ttu-id="675c4-133">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="675c4-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="675c4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="675c4-134">NOTES</span></span>

## <span data-ttu-id="675c4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="675c4-135">RELATED LINKS</span></span>
