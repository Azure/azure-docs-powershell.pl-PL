---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524813"
---
# <span data-ttu-id="fdea5-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="fdea5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdea5-102">SYNOPSIS</span></span>
<span data-ttu-id="fdea5-103">To polecenie powoduje utworzenie nowej grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fdea5-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdea5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdea5-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdea5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fdea5-105">DESCRIPTION</span></span>
<span data-ttu-id="fdea5-106">Umożliwia utworzenie nowej grupy trybu failover bazy danych SQL Azure dla określonych serwerów.</span><span class="sxs-lookup"><span data-stu-id="fdea5-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="fdea5-107">Dwa punkty końcowe TDS bazy danych Azure SQL Database są tworzone w witrynie FailoverGroupName. SqlDatabaseDnsSuffix (na przykład FailoverGroupName.database.windows.net) i FailoverGroupName. pomocnicze SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="fdea5-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="fdea5-108">Te punkty końcowe mogą być używane do łączenia się z serwerami podstawowymi i pomocniczymi w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="fdea5-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="fdea5-109">Jeśli na serwerze podstawowym wpłynie awaria, automatyczna praca awaryjna punktów końcowych i baz danych zostanie wyzwolona jako podyktowana przez zasady pracy awaryjnej grupy trybu failover i okres prolongaty.</span><span class="sxs-lookup"><span data-stu-id="fdea5-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="fdea5-110">Nowo utworzone grupy pracy awaryjnej nie zawierają żadnych baz danych.</span><span class="sxs-lookup"><span data-stu-id="fdea5-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="fdea5-111">Aby sterować zestawem baz danych w grupie trybu failover, Użyj poleceń cmdlet "Add-AzureRmSqlDatabaseToFailoverGroup" i "Remove-AzureRmSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="fdea5-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="fdea5-112">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="fdea5-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="fdea5-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdea5-113">EXAMPLES</span></span>

### <span data-ttu-id="fdea5-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fdea5-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="fdea5-115">To polecenie tworzy nową grupę pracy awaryjnej z zasadami pracy awaryjnej dla dwóch serwerów w tej samej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fdea5-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="fdea5-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fdea5-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="fdea5-117">To polecenie tworzy nową grupę trybu failover z zasadami pracy awaryjnej dla dwóch serwerów w różnych grupach zasobów.</span><span class="sxs-lookup"><span data-stu-id="fdea5-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="fdea5-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdea5-118">PARAMETERS</span></span>

### <span data-ttu-id="fdea5-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="fdea5-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="fdea5-120">Czy awaria na serwerze pomocniczym powinna wyzwalać automatyczną pracę awaryjną punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="fdea5-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="fdea5-121">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="fdea5-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="fdea5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdea5-122">-DefaultProfile</span></span>
<span data-ttu-id="fdea5-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fdea5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdea5-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="fdea5-124">-FailoverGroupName</span></span>
<span data-ttu-id="fdea5-125">Nazwa grupy trybu failover bazy danych SQL Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="fdea5-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea5-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="fdea5-126">-FailoverPolicy</span></span>
<span data-ttu-id="fdea5-127">Zasady przełączania awaryjnego grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="fdea5-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="fdea5-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="fdea5-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="fdea5-129">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria i nie można ukończyć pracy awaryjnej bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="fdea5-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="fdea5-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdea5-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="fdea5-131">Nazwa grupy pomocniczej zasobu w grupie praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fdea5-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea5-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="fdea5-132">-PartnerServerName</span></span>
<span data-ttu-id="fdea5-133">Nazwa serwera pomocniczego grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fdea5-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdea5-134">-ResourceGroupName</span></span>
<span data-ttu-id="fdea5-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fdea5-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdea5-136">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fdea5-136">-ServerName</span></span>
<span data-ttu-id="fdea5-137">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="fdea5-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="fdea5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdea5-138">CommonParameters</span></span>
<span data-ttu-id="fdea5-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdea5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdea5-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdea5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdea5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdea5-141">INPUTS</span></span>

### <span data-ttu-id="fdea5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fdea5-142">System.String</span></span>

## <span data-ttu-id="fdea5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdea5-143">OUTPUTS</span></span>

### <span data-ttu-id="fdea5-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="fdea5-144">System.Object</span></span>

## <span data-ttu-id="fdea5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdea5-145">NOTES</span></span>

## <span data-ttu-id="fdea5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdea5-146">RELATED LINKS</span></span>

[<span data-ttu-id="fdea5-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdea5-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdea5-149">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="fdea5-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="fdea5-151">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdea5-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdea5-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdea5-153">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fdea5-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)