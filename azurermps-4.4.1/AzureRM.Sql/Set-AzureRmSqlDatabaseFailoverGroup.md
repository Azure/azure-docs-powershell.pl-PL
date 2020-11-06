---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 05f2de37ebeb477d45f96c415759ead3080a9e60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544651"
---
# <span data-ttu-id="266ab-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="266ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="266ab-102">SYNOPSIS</span></span>
<span data-ttu-id="266ab-103">Modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="266ab-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="266ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="266ab-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="266ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="266ab-105">DESCRIPTION</span></span>
<span data-ttu-id="266ab-106">To polecenie modyfikuje konfigurację grupy trybu failover bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="266ab-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="266ab-107">Aby wykonać polecenie, należy użyć głównego serwera grupy pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="266ab-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="266ab-108">Aby sterować zestawem baz danych w grupie, użyj polecenia "Add-AzureRmSqlDatabaseToFailoverGroup" i "Remove-AzureRmSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="266ab-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="266ab-109">Podczas wyświetlania podglądu funkcji grup pracy awaryjnej w parametrze "-GracePeriodWithDataLossHours" są obsługiwane tylko wartości większe niż lub równe 1 godzina.</span><span class="sxs-lookup"><span data-stu-id="266ab-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="266ab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="266ab-110">EXAMPLES</span></span>

### <span data-ttu-id="266ab-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="266ab-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="266ab-112">Ustawia zasady przejęcia awaryjnego grupy trybu failover na wartość "automatycznie".</span><span class="sxs-lookup"><span data-stu-id="266ab-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="266ab-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="266ab-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="266ab-114">Ustawia zasady pracy awaryjnej grupy trybu failover jako "ręczna" przez potok w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="266ab-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="266ab-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="266ab-115">PARAMETERS</span></span>

### <span data-ttu-id="266ab-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="266ab-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="266ab-117">Informacja o tym, czy w przypadku dzieci na serwerze pomocniczym powinna być wyzwalana automatyczna praca awaryjna punktu końcowego tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="266ab-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="266ab-118">Ta funkcja nie jest jeszcze obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="266ab-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="266ab-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="266ab-119">-FailoverGroupName</span></span>
<span data-ttu-id="266ab-120">Nazwa grupy praca awaryjna bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="266ab-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="266ab-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="266ab-121">-FailoverPolicy</span></span>
<span data-ttu-id="266ab-122">Zasady przełączania awaryjnego grupy usługi Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="266ab-122">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="266ab-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="266ab-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="266ab-124">Interwał przed zainicjowaniem automatycznej pracy awaryjnej, jeśli na serwerze podstawowym wystąpi awaria i nie można ukończyć pracy awaryjnej bez utraty danych.</span><span class="sxs-lookup"><span data-stu-id="266ab-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="266ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="266ab-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="266ab-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="266ab-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="266ab-127">-ServerName</span></span>
<span data-ttu-id="266ab-128">Nazwa podstawowego serwera bazy danych SQL usługi Azure w grupie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="266ab-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="266ab-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266ab-129">-DefaultProfile</span></span>
<span data-ttu-id="266ab-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="266ab-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="266ab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266ab-131">CommonParameters</span></span>
<span data-ttu-id="266ab-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="266ab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266ab-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="266ab-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266ab-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="266ab-134">INPUTS</span></span>

### <span data-ttu-id="266ab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="266ab-135">System.String</span></span>

## <span data-ttu-id="266ab-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="266ab-136">OUTPUTS</span></span>

### <span data-ttu-id="266ab-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="266ab-137">System.Object</span></span>

## <span data-ttu-id="266ab-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="266ab-138">NOTES</span></span>

## <span data-ttu-id="266ab-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="266ab-139">RELATED LINKS</span></span>

[<span data-ttu-id="266ab-140">Nowe — AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-140">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="266ab-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="266ab-142">Dodaj-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-142">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="266ab-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="266ab-144">Przełącznik-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-144">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="266ab-145">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="266ab-145">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="266ab-146">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="266ab-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
