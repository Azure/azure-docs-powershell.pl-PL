---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234255"
---
# <span data-ttu-id="50bfd-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="50bfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="50bfd-103">Modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="50bfd-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="50bfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50bfd-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50bfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="50bfd-106">To polecenie modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="50bfd-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="50bfd-107">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="50bfd-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="50bfd-108">Aby sterować zestawem baz danych w grupie, użyj polecenia "Add-AzSqlDatabaseToFailoverGroup" i "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="50bfd-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="50bfd-109">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="50bfd-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="50bfd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50bfd-110">EXAMPLES</span></span>

### <span data-ttu-id="50bfd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50bfd-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="50bfd-112">Ustawia zasady przejęcia awaryjnego grupy trybu failover na wartość "automatycznie".</span><span class="sxs-lookup"><span data-stu-id="50bfd-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="50bfd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="50bfd-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="50bfd-114">Ustawia zasady pracy awaryjnej grupy trybu failover jako "ręczna" przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="50bfd-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="50bfd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50bfd-115">PARAMETERS</span></span>

### <span data-ttu-id="50bfd-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="50bfd-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="50bfd-117">Informacja o tym, czy w przypadku dzieci na serwerze pomocniczym powinna być wyzwalana automatyczna praca awaryjna punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="50bfd-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="50bfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bfd-118">-DefaultProfile</span></span>
<span data-ttu-id="50bfd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="50bfd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50bfd-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="50bfd-120">-FailoverGroupName</span></span>
<span data-ttu-id="50bfd-121">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="50bfd-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="50bfd-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="50bfd-122">-FailoverPolicy</span></span>
<span data-ttu-id="50bfd-123">Zasady przełączania awaryjnego grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="50bfd-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="50bfd-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="50bfd-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="50bfd-125">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria.</span><span class="sxs-lookup"><span data-stu-id="50bfd-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="50bfd-126">Oznacza to, że baza danych SQL Azure nie będzie inicjować automatycznej pracy awaryjnej przed upływem okresu prolongaty.</span><span class="sxs-lookup"><span data-stu-id="50bfd-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="50bfd-127">Pamiętaj, że operacja przełączania awaryjnego z opcją AllowDataLoss może spowodować utratę danych ze względu na charakter asynchronicznej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="50bfd-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="50bfd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bfd-128">-ResourceGroupName</span></span>
<span data-ttu-id="50bfd-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50bfd-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="50bfd-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="50bfd-130">-ServerName</span></span>
<span data-ttu-id="50bfd-131">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="50bfd-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="50bfd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bfd-132">CommonParameters</span></span>
<span data-ttu-id="50bfd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bfd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bfd-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50bfd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bfd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50bfd-135">INPUTS</span></span>

### <span data-ttu-id="50bfd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="50bfd-136">System.String</span></span>

## <span data-ttu-id="50bfd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50bfd-137">OUTPUTS</span></span>

### <span data-ttu-id="50bfd-138">Microsoft. Azure. Commands. SQL. failover. model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="50bfd-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="50bfd-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50bfd-139">NOTES</span></span>

## <span data-ttu-id="50bfd-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50bfd-140">RELATED LINKS</span></span>

[<span data-ttu-id="50bfd-141">Nowe — AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50bfd-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50bfd-143">Dodaj-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="50bfd-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="50bfd-145">Przełącznik-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50bfd-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50bfd-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50bfd-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="50bfd-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
