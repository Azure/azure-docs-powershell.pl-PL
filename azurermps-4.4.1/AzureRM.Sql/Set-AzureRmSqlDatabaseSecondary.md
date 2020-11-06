---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 85dc7d386dc64f8c384f9aae7925379375b95a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542820"
---
# <span data-ttu-id="6ad68-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6ad68-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="6ad68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ad68-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad68-103">Przełącza pomocniczą bazę danych na podstawową w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="6ad68-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ad68-104">SYNTAX</span></span>

### <span data-ttu-id="6ad68-105">NoOptionsSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ad68-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad68-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="6ad68-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad68-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6ad68-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad68-108">Polecenie cmdlet **Set-AzureRmSqlDatabaseSecondary** przełącza pomocniczą bazę danych w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="6ad68-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="6ad68-109">To polecenie cmdlet jest przeznaczone do obsługi poleceń konfiguracji ogólnej, ale jest obecnie ograniczone do inicjowania pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="6ad68-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="6ad68-110">Określ parametr *AllowDataLoss* , aby zainicjować wymuszoną pracę awaryjną podczas awarii.</span><span class="sxs-lookup"><span data-stu-id="6ad68-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="6ad68-111">Nie trzeba określać tego parametru podczas wykonywania planowanej operacji, na przykład funkcji drążenia do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ad68-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="6ad68-112">W tym ostatnim przypadku pomocnicza baza danych jest synchronizowana z podstawowym, zanim zostanie przełączona.</span><span class="sxs-lookup"><span data-stu-id="6ad68-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="6ad68-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ad68-113">EXAMPLES</span></span>

## <span data-ttu-id="6ad68-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ad68-114">PARAMETERS</span></span>

### <span data-ttu-id="6ad68-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6ad68-115">-AllowDataLoss</span></span>
<span data-ttu-id="6ad68-116">Wskazuje, że ta operacja trybu failover umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="6ad68-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="6ad68-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ad68-117">-DatabaseName</span></span>
<span data-ttu-id="6ad68-118">Określa nazwę pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad68-118">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="6ad68-119">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="6ad68-119">-Failover</span></span>
<span data-ttu-id="6ad68-120">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="6ad68-120">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="6ad68-121">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad68-121">-PartnerResourceGroupName</span></span>
<span data-ttu-id="6ad68-122">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL partnera.</span><span class="sxs-lookup"><span data-stu-id="6ad68-122">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="6ad68-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad68-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ad68-124">Określa nazwę grupy zasobów, do której przypisano pomocnicza baza danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad68-124">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="6ad68-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6ad68-125">-ServerName</span></span>
<span data-ttu-id="6ad68-126">Określa nazwę serwera SQL obsługującego pomocniczą bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad68-126">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="6ad68-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ad68-127">-Confirm</span></span>
<span data-ttu-id="6ad68-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad68-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad68-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad68-129">-WhatIf</span></span>
<span data-ttu-id="6ad68-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad68-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad68-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ad68-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad68-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad68-132">-DefaultProfile</span></span>
<span data-ttu-id="6ad68-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad68-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad68-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad68-134">CommonParameters</span></span>
<span data-ttu-id="6ad68-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad68-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad68-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad68-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad68-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad68-137">INPUTS</span></span>

###  
<span data-ttu-id="6ad68-138">Możesz popotokować wystąpienia obiektu **bazy danych** dla pomocniczej bazy danych w celu przeprowadzenia awaryjnego przepełnienia i utworzyć podstawową bazę danych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad68-138">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="6ad68-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ad68-139">OUTPUTS</span></span>

###  
<span data-ttu-id="6ad68-140">To polecenie cmdlet zwraca **ReplicationLink**.</span><span class="sxs-lookup"><span data-stu-id="6ad68-140">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="6ad68-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ad68-141">NOTES</span></span>

## <span data-ttu-id="6ad68-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ad68-142">RELATED LINKS</span></span>

[<span data-ttu-id="6ad68-143">Nowe — AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6ad68-143">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="6ad68-144">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6ad68-144">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="6ad68-145">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6ad68-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
