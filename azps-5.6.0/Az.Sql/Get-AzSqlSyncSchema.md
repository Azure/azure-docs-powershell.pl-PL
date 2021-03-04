---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: e32f693b5f0bfc114f3ac40a4fc5761ec3a3ca70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999216"
---
# <span data-ttu-id="15ebc-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="15ebc-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="15ebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="15ebc-103">Zwraca informacje o schemacie synchronizacji bazy danych lub centrum danych członków.</span><span class="sxs-lookup"><span data-stu-id="15ebc-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="15ebc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15ebc-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15ebc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="15ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="15ebc-106">Polecenie **cmdlet Get-AzSqlSyncSchema** zwraca informacje o schemacie synchronizacji bazy danych członka lub bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="15ebc-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="15ebc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="15ebc-108">Przykład 1. Uzyskiwanie schematu synchronizacji bazy danych centrum</span><span class="sxs-lookup"><span data-stu-id="15ebc-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="15ebc-109">To polecenie pobiera schemat synchronizacji dla bazy danych centrum w grupie synchronizacji SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="15ebc-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="15ebc-110">Przykład 2. Uzyskaj schemat synchronizacji dla bazy danych centrum i rozwiń tabelę</span><span class="sxs-lookup"><span data-stu-id="15ebc-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="15ebc-111">To polecenie pobiera schemat synchronizacji dla bazy danych centrum w grupie synchronizacjiGroup01 i rozwija właściwość Tabele.</span><span class="sxs-lookup"><span data-stu-id="15ebc-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="15ebc-112">Przykład 3. Uzyskiwanie schematu synchronizacji dla bazy danych członka</span><span class="sxs-lookup"><span data-stu-id="15ebc-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="15ebc-113">To polecenie pobiera schemat synchronizacji dla bazy danych członków w pliku syncMember01 członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15ebc-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="15ebc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15ebc-114">PARAMETERS</span></span>

### <span data-ttu-id="15ebc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15ebc-115">-DatabaseName</span></span>
<span data-ttu-id="15ebc-116">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="15ebc-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="15ebc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ebc-117">-DefaultProfile</span></span>
<span data-ttu-id="15ebc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="15ebc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15ebc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15ebc-119">-ResourceGroupName</span></span>
<span data-ttu-id="15ebc-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15ebc-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="15ebc-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15ebc-121">-ServerName</span></span>
<span data-ttu-id="15ebc-122">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="15ebc-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="15ebc-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="15ebc-123">-SyncGroupName</span></span>
<span data-ttu-id="15ebc-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15ebc-124">The sync group name.</span></span>

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

### <span data-ttu-id="15ebc-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="15ebc-125">-SyncMemberName</span></span>
<span data-ttu-id="15ebc-126">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15ebc-126">The sync member name.</span></span>

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

### <span data-ttu-id="15ebc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ebc-127">CommonParameters</span></span>
<span data-ttu-id="15ebc-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15ebc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ebc-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15ebc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ebc-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15ebc-130">INPUTS</span></span>

### <span data-ttu-id="15ebc-131">System.String</span><span class="sxs-lookup"><span data-stu-id="15ebc-131">System.String</span></span>

## <span data-ttu-id="15ebc-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15ebc-132">OUTPUTS</span></span>

### <span data-ttu-id="15ebc-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="15ebc-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="15ebc-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15ebc-134">NOTES</span></span>

## <span data-ttu-id="15ebc-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15ebc-135">RELATED LINKS</span></span>
