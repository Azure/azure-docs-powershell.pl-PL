---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 56749c265980fc40ee19b60261641f0c98c25da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546396"
---
# <span data-ttu-id="3de4e-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3de4e-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="3de4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3de4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3de4e-103">Przełącza pomocniczą bazę danych na podstawową w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3de4e-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3de4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3de4e-104">SYNTAX</span></span>

### <span data-ttu-id="3de4e-105">NoOptionsSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3de4e-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3de4e-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="3de4e-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de4e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3de4e-107">DESCRIPTION</span></span>
<span data-ttu-id="3de4e-108">Polecenie cmdlet **Set-AzureRmSqlDatabaseSecondary** przełącza pomocniczą bazę danych w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3de4e-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="3de4e-109">To polecenie cmdlet jest przeznaczone do obsługi poleceń konfiguracji ogólnej, ale jest obecnie ograniczone do inicjowania pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="3de4e-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="3de4e-110">Określ parametr *AllowDataLoss* , aby zainicjować wymuszoną pracę awaryjną podczas awarii.</span><span class="sxs-lookup"><span data-stu-id="3de4e-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="3de4e-111">Nie trzeba określać tego parametru podczas wykonywania planowanej operacji, na przykład funkcji drążenia do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3de4e-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="3de4e-112">W tym ostatnim przypadku pomocnicza baza danych jest synchronizowana z podstawowym, zanim zostanie przełączona.</span><span class="sxs-lookup"><span data-stu-id="3de4e-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="3de4e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3de4e-113">EXAMPLES</span></span>

## <span data-ttu-id="3de4e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3de4e-114">PARAMETERS</span></span>

### <span data-ttu-id="3de4e-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="3de4e-115">-AllowDataLoss</span></span>
<span data-ttu-id="3de4e-116">Wskazuje, że ta operacja trybu failover umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="3de4e-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="3de4e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3de4e-117">-AsJob</span></span>
<span data-ttu-id="3de4e-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3de4e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3de4e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3de4e-119">-DatabaseName</span></span>
<span data-ttu-id="3de4e-120">Określa nazwę pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3de4e-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="3de4e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de4e-121">-DefaultProfile</span></span>
<span data-ttu-id="3de4e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3de4e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3de4e-123">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="3de4e-123">-Failover</span></span>
<span data-ttu-id="3de4e-124">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3de4e-124">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="3de4e-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de4e-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="3de4e-126">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL partnera.</span><span class="sxs-lookup"><span data-stu-id="3de4e-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="3de4e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de4e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3de4e-128">Określa nazwę grupy zasobów, do której przypisano pomocnicza baza danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3de4e-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="3de4e-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3de4e-129">-ServerName</span></span>
<span data-ttu-id="3de4e-130">Określa nazwę serwera SQL obsługującego pomocniczą bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3de4e-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="3de4e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3de4e-131">-Confirm</span></span>
<span data-ttu-id="3de4e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de4e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de4e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de4e-133">-WhatIf</span></span>
<span data-ttu-id="3de4e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de4e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de4e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3de4e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de4e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de4e-136">CommonParameters</span></span>
<span data-ttu-id="3de4e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de4e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de4e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de4e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de4e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3de4e-139">INPUTS</span></span>

### <span data-ttu-id="3de4e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3de4e-140">System.String</span></span>

## <span data-ttu-id="3de4e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3de4e-141">OUTPUTS</span></span>

### <span data-ttu-id="3de4e-142">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="3de4e-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="3de4e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3de4e-143">NOTES</span></span>

## <span data-ttu-id="3de4e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3de4e-144">RELATED LINKS</span></span>

[<span data-ttu-id="3de4e-145">Nowe — AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3de4e-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="3de4e-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3de4e-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="3de4e-147">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3de4e-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
