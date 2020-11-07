---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 9e0af4c5110fe0732782293eb9d8c67fb7d89600
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895765"
---
# <span data-ttu-id="56d1f-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56d1f-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="56d1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="56d1f-103">Przełącza pomocniczą bazę danych na podstawową w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="56d1f-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="56d1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56d1f-104">SYNTAX</span></span>

### <span data-ttu-id="56d1f-105">NoOptionsSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56d1f-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d1f-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="56d1f-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d1f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56d1f-107">DESCRIPTION</span></span>
<span data-ttu-id="56d1f-108">Polecenie cmdlet **Set-AzSqlDatabaseSecondary** przełącza pomocniczą bazę danych w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="56d1f-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="56d1f-109">To polecenie cmdlet jest przeznaczone do obsługi poleceń konfiguracji ogólnej, ale jest obecnie ograniczone do inicjowania pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="56d1f-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="56d1f-110">Określ parametr *AllowDataLoss* , aby zainicjować wymuszoną pracę awaryjną podczas awarii.</span><span class="sxs-lookup"><span data-stu-id="56d1f-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="56d1f-111">Nie trzeba określać tego parametru podczas wykonywania planowanej operacji, na przykład funkcji drążenia do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="56d1f-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="56d1f-112">W tym ostatnim przypadku pomocnicza baza danych jest synchronizowana z podstawowym, zanim zostanie przełączona.</span><span class="sxs-lookup"><span data-stu-id="56d1f-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="56d1f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56d1f-113">EXAMPLES</span></span>

### <span data-ttu-id="56d1f-114">1: Inicjowanie planowanego trybu failover</span><span class="sxs-lookup"><span data-stu-id="56d1f-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="56d1f-115">2: Inicjowanie wymuszonego przełączania awaryjnego (z potencjalną utratą danych)</span><span class="sxs-lookup"><span data-stu-id="56d1f-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="56d1f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56d1f-116">PARAMETERS</span></span>

### <span data-ttu-id="56d1f-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="56d1f-117">-AllowDataLoss</span></span>
<span data-ttu-id="56d1f-118">Wskazuje, że ta operacja trybu failover umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="56d1f-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d1f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56d1f-119">-AsJob</span></span>
<span data-ttu-id="56d1f-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="56d1f-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d1f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56d1f-121">-DatabaseName</span></span>
<span data-ttu-id="56d1f-122">Określa nazwę pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="56d1f-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="56d1f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d1f-123">-DefaultProfile</span></span>
<span data-ttu-id="56d1f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="56d1f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56d1f-125">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="56d1f-125">-Failover</span></span>
<span data-ttu-id="56d1f-126">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="56d1f-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d1f-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d1f-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="56d1f-128">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL partnera.</span><span class="sxs-lookup"><span data-stu-id="56d1f-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d1f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d1f-129">-ResourceGroupName</span></span>
<span data-ttu-id="56d1f-130">Określa nazwę grupy zasobów, do której przypisano pomocnicza baza danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="56d1f-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="56d1f-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="56d1f-131">-ServerName</span></span>
<span data-ttu-id="56d1f-132">Określa nazwę serwera SQL obsługującego pomocniczą bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="56d1f-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="56d1f-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56d1f-133">-Confirm</span></span>
<span data-ttu-id="56d1f-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d1f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d1f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d1f-135">-WhatIf</span></span>
<span data-ttu-id="56d1f-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d1f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d1f-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56d1f-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d1f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d1f-138">CommonParameters</span></span>
<span data-ttu-id="56d1f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d1f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d1f-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56d1f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d1f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56d1f-141">INPUTS</span></span>

### <span data-ttu-id="56d1f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="56d1f-142">System.String</span></span>

## <span data-ttu-id="56d1f-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56d1f-143">OUTPUTS</span></span>

### <span data-ttu-id="56d1f-144">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="56d1f-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="56d1f-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56d1f-145">NOTES</span></span>

## <span data-ttu-id="56d1f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56d1f-146">RELATED LINKS</span></span>

[<span data-ttu-id="56d1f-147">Nowe — AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56d1f-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="56d1f-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56d1f-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="56d1f-149">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="56d1f-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
