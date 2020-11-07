---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 825d6f367fb4fbace53fccdb8798d17a915fc2bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895797"
---
# <span data-ttu-id="e3484-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="e3484-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3484-102">SYNOPSIS</span></span>
<span data-ttu-id="e3484-103">Modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e3484-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="e3484-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3484-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3484-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3484-105">DESCRIPTION</span></span>
<span data-ttu-id="e3484-106">To polecenie modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e3484-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="e3484-107">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="e3484-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="e3484-108">Aby sterować zestawem baz danych w grupie, użyj polecenia "Add-AzSqlDatabaseToFailoverGroup" i "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="e3484-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="e3484-109">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="e3484-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="e3484-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3484-110">EXAMPLES</span></span>

### <span data-ttu-id="e3484-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3484-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="e3484-112">Ustawia zasady przejęcia awaryjnego grupy trybu failover na wartość "automatycznie".</span><span class="sxs-lookup"><span data-stu-id="e3484-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="e3484-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e3484-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="e3484-114">Ustawia zasady pracy awaryjnej grupy trybu failover jako "ręczna" przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e3484-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="e3484-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3484-115">PARAMETERS</span></span>

### <span data-ttu-id="e3484-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="e3484-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="e3484-117">Informacja o tym, czy w przypadku dzieci na serwerze pomocniczym powinna być wyzwalana automatyczna praca awaryjna punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="e3484-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="e3484-118">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="e3484-118">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3484-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3484-119">-DefaultProfile</span></span>
<span data-ttu-id="e3484-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e3484-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3484-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="e3484-121">-FailoverGroupName</span></span>
<span data-ttu-id="e3484-122">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e3484-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="e3484-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e3484-123">-FailoverPolicy</span></span>
<span data-ttu-id="e3484-124">Zasady przełączania awaryjnego grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="e3484-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3484-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="e3484-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="e3484-126">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria.</span><span class="sxs-lookup"><span data-stu-id="e3484-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="e3484-127">Oznacza to, że baza danych SQL Azure nie będzie inicjować automatycznej pracy awaryjnej przed upływem okresu prolongaty.</span><span class="sxs-lookup"><span data-stu-id="e3484-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="e3484-128">Pamiętaj, że operacja przełączania awaryjnego z opcją AllowDataLoss może spowodować utratę danych ze względu na charakter asynchronicznej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="e3484-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3484-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3484-129">-ResourceGroupName</span></span>
<span data-ttu-id="e3484-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3484-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3484-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e3484-131">-ServerName</span></span>
<span data-ttu-id="e3484-132">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e3484-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="e3484-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3484-133">CommonParameters</span></span>
<span data-ttu-id="e3484-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3484-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3484-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3484-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3484-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3484-136">INPUTS</span></span>

### <span data-ttu-id="e3484-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e3484-137">System.String</span></span>

## <span data-ttu-id="e3484-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3484-138">OUTPUTS</span></span>

### <span data-ttu-id="e3484-139">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e3484-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="e3484-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3484-140">NOTES</span></span>

## <span data-ttu-id="e3484-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3484-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3484-142">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-142">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e3484-143">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-143">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e3484-144">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-144">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="e3484-145">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-145">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="e3484-146">Przełącznik-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-146">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e3484-147">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e3484-147">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e3484-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e3484-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
