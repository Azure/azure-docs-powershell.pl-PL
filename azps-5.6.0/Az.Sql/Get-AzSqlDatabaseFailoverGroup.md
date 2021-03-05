---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 7b23bd6082fc79ff6096f496117c0ff6b63fd134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967482"
---
# <span data-ttu-id="907d4-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="907d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="907d4-102">SYNOPSIS</span></span>
<span data-ttu-id="907d4-103">Pobiera lub wyświetla grupy trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="907d4-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="907d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="907d4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="907d4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="907d4-105">DESCRIPTION</span></span>
<span data-ttu-id="907d4-106">Pobiera określoną grupę trybu failover usługi Azure SQL Database lub wyświetla grupy trybu failover na serwerze.</span><span class="sxs-lookup"><span data-stu-id="907d4-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="907d4-107">Do wykonania polecenia może zostać użyty jeden z serwerów w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="907d4-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="907d4-108">Zwrócone wartości będą odzwierciedlać stan określonego serwera względem grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="907d4-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="907d4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="907d4-109">EXAMPLES</span></span>

### <span data-ttu-id="907d4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="907d4-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="907d4-111">Lista wszystkich grup trybu failover na serwerze.</span><span class="sxs-lookup"><span data-stu-id="907d4-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="907d4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="907d4-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="907d4-113">Pobierz konkretną grupę trybu failover.</span><span class="sxs-lookup"><span data-stu-id="907d4-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="907d4-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="907d4-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="907d4-115">Pobierz wszystkie grupy trybu failover na serwerze, które zaczynają się od "fg".</span><span class="sxs-lookup"><span data-stu-id="907d4-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="907d4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="907d4-116">PARAMETERS</span></span>

### <span data-ttu-id="907d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907d4-117">-DefaultProfile</span></span>
<span data-ttu-id="907d4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="907d4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="907d4-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="907d4-119">-FailoverGroupName</span></span>
<span data-ttu-id="907d4-120">Nazwa grupy trybu failover bazy danych Azure SQL Database do pobrania.</span><span class="sxs-lookup"><span data-stu-id="907d4-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907d4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907d4-121">-ResourceGroupName</span></span>
<span data-ttu-id="907d4-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="907d4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="907d4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="907d4-123">-ServerName</span></span>
<span data-ttu-id="907d4-124">Nazwa serwera azure SQL Database Server, z którego ma zostać pobrana grupa trybu failover.</span><span class="sxs-lookup"><span data-stu-id="907d4-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="907d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907d4-125">CommonParameters</span></span>
<span data-ttu-id="907d4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907d4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="907d4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907d4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="907d4-128">INPUTS</span></span>

### <span data-ttu-id="907d4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="907d4-129">System.String</span></span>

## <span data-ttu-id="907d4-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="907d4-130">OUTPUTS</span></span>

### <span data-ttu-id="907d4-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="907d4-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="907d4-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="907d4-132">NOTES</span></span>

## <span data-ttu-id="907d4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="907d4-133">RELATED LINKS</span></span>

[<span data-ttu-id="907d4-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="907d4-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="907d4-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="907d4-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="907d4-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="907d4-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="907d4-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="907d4-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="907d4-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
