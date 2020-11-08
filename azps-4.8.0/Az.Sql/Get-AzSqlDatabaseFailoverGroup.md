---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063171"
---
# <span data-ttu-id="f6263-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f6263-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6263-102">SYNOPSIS</span></span>
<span data-ttu-id="f6263-103">Pobiera lub wyświetla listę grup pracy awaryjnej bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f6263-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="f6263-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6263-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6263-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6263-105">DESCRIPTION</span></span>
<span data-ttu-id="f6263-106">Pobiera określoną grupę usługi Azure failover dla bazy danych SQL lub wyświetla listę grup pracy awaryjnej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f6263-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="f6263-107">Do wykonania polecenia można użyć dowolnego serwera w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f6263-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="f6263-108">Zwracane wartości będą odzwierciedlać stan określonego serwera w odniesieniu do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f6263-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="f6263-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6263-109">EXAMPLES</span></span>

### <span data-ttu-id="f6263-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6263-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="f6263-111">Lista wszystkich grup pracy awaryjnej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f6263-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="f6263-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f6263-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="f6263-113">Pobierz określoną grupę pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="f6263-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="f6263-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f6263-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="f6263-115">Pobierz wszystkie grupy trybu failover na serwerze rozpoczynającym się od "FG".</span><span class="sxs-lookup"><span data-stu-id="f6263-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="f6263-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6263-116">PARAMETERS</span></span>

### <span data-ttu-id="f6263-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6263-117">-DefaultProfile</span></span>
<span data-ttu-id="f6263-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f6263-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6263-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f6263-119">-FailoverGroupName</span></span>
<span data-ttu-id="f6263-120">Nazwa grupy trybu failover bazy danych SQL Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f6263-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="f6263-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6263-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6263-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6263-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6263-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f6263-123">-ServerName</span></span>
<span data-ttu-id="f6263-124">Nazwa serwera bazy danych SQL Azure, z którego ma zostać pobrana Grupa trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f6263-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="f6263-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6263-125">CommonParameters</span></span>
<span data-ttu-id="f6263-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6263-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6263-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6263-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6263-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6263-128">INPUTS</span></span>

### <span data-ttu-id="f6263-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f6263-129">System.String</span></span>

## <span data-ttu-id="f6263-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6263-130">OUTPUTS</span></span>

### <span data-ttu-id="f6263-131">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f6263-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f6263-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6263-132">NOTES</span></span>

## <span data-ttu-id="f6263-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6263-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6263-134">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f6263-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f6263-136">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f6263-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f6263-138">Przełącznik-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f6263-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f6263-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f6263-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f6263-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
