---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: e5452ef5b6d8b2e5535c5388d5d42698aa7c261f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542156"
---
# <span data-ttu-id="82271-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="82271-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82271-102">SYNOPSIS</span></span>
<span data-ttu-id="82271-103">Modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="82271-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82271-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82271-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82271-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82271-105">DESCRIPTION</span></span>
<span data-ttu-id="82271-106">To polecenie modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="82271-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="82271-107">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="82271-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="82271-108">Aby sterować zestawem baz danych w grupie, użyj polecenia "Add-AzureRmSqlDatabaseToFailoverGroup" i "Remove-AzureRmSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="82271-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="82271-109">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="82271-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="82271-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82271-110">EXAMPLES</span></span>

### <span data-ttu-id="82271-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="82271-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="82271-112">Ustawia zasady przejęcia awaryjnego grupy trybu failover na wartość "automatycznie".</span><span class="sxs-lookup"><span data-stu-id="82271-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="82271-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="82271-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="82271-114">Ustawia zasady pracy awaryjnej grupy trybu failover jako "ręczna" przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="82271-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="82271-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82271-115">PARAMETERS</span></span>

### <span data-ttu-id="82271-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="82271-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="82271-117">Informacja o tym, czy w przypadku dzieci na serwerze pomocniczym powinna być wyzwalana automatyczna praca awaryjna punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="82271-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="82271-118">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="82271-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82271-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82271-119">-DefaultProfile</span></span>
<span data-ttu-id="82271-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="82271-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82271-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="82271-121">-FailoverGroupName</span></span>
<span data-ttu-id="82271-122">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="82271-122">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82271-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="82271-123">-FailoverPolicy</span></span>
<span data-ttu-id="82271-124">Zasady przełączania awaryjnego grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="82271-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82271-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="82271-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="82271-126">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria.</span><span class="sxs-lookup"><span data-stu-id="82271-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="82271-127">Oznacza to, że baza danych SQL Azure nie będzie inicjować automatycznej pracy awaryjnej przed upływem okresu prolongaty.</span><span class="sxs-lookup"><span data-stu-id="82271-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="82271-128">Pamiętaj, że operacja przełączania awaryjnego z opcją AllowDataLoss może spowodować utratę danych ze względu na charakter asynchronicznej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="82271-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82271-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82271-129">-ResourceGroupName</span></span>
<span data-ttu-id="82271-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="82271-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82271-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="82271-131">-ServerName</span></span>
<span data-ttu-id="82271-132">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="82271-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82271-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82271-133">CommonParameters</span></span>
<span data-ttu-id="82271-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82271-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82271-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82271-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82271-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82271-136">INPUTS</span></span>

### <span data-ttu-id="82271-137">System. String</span><span class="sxs-lookup"><span data-stu-id="82271-137">System.String</span></span>

## <span data-ttu-id="82271-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82271-138">OUTPUTS</span></span>

### <span data-ttu-id="82271-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="82271-139">System.Object</span></span>

## <span data-ttu-id="82271-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82271-140">NOTES</span></span>

## <span data-ttu-id="82271-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82271-141">RELATED LINKS</span></span>

[<span data-ttu-id="82271-142">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="82271-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="82271-144">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="82271-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="82271-146">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="82271-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82271-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="82271-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="82271-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
