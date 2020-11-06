---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: db85c1f8de00432b3f9213473c89728239099c0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543383"
---
# <span data-ttu-id="5c9db-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5c9db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c9db-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9db-103">Pobiera lub wyświetla listę grup pracy awaryjnej bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5c9db-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c9db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c9db-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c9db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c9db-105">DESCRIPTION</span></span>
<span data-ttu-id="5c9db-106">Pobiera określoną grupę usługi Azure failover dla bazy danych SQL lub wyświetla listę grup pracy awaryjnej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5c9db-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="5c9db-107">Do wykonania polecenia można użyć dowolnego serwera w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5c9db-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="5c9db-108">Zwracane wartości będą odzwierciedlać stan określonego serwera w odniesieniu do grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5c9db-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="5c9db-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c9db-109">EXAMPLES</span></span>

### <span data-ttu-id="5c9db-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c9db-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="5c9db-111">Lista wszystkich grup pracy awaryjnej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5c9db-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="5c9db-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5c9db-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="5c9db-113">Pobierz określoną grupę pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="5c9db-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="5c9db-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c9db-114">PARAMETERS</span></span>

### <span data-ttu-id="5c9db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9db-115">-DefaultProfile</span></span>
<span data-ttu-id="5c9db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5c9db-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c9db-117">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9db-117">-FailoverGroupName</span></span>
<span data-ttu-id="5c9db-118">Nazwa grupy trybu failover bazy danych SQL Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5c9db-118">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="5c9db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9db-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c9db-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c9db-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c9db-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5c9db-121">-ServerName</span></span>
<span data-ttu-id="5c9db-122">Nazwa serwera bazy danych SQL Azure, z którego ma zostać pobrana Grupa trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5c9db-122">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="5c9db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9db-123">CommonParameters</span></span>
<span data-ttu-id="5c9db-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c9db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9db-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c9db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9db-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c9db-126">INPUTS</span></span>

### <span data-ttu-id="5c9db-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5c9db-127">System.String</span></span>

## <span data-ttu-id="5c9db-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c9db-128">OUTPUTS</span></span>

### <span data-ttu-id="5c9db-129">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5c9db-129">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5c9db-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c9db-130">NOTES</span></span>

## <span data-ttu-id="5c9db-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c9db-131">RELATED LINKS</span></span>

[<span data-ttu-id="5c9db-132">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5c9db-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5c9db-134">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5c9db-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5c9db-136">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5c9db-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5c9db-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5c9db-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5c9db-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
