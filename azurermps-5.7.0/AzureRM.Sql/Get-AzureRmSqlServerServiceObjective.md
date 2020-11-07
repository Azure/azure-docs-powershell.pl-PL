---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5bcd5c6317688cc433d83b002cd3cb81ea790aaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716477"
---
# <span data-ttu-id="4d6b6-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="4d6b6-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="4d6b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6b6-103">Umożliwia pobieranie celów usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d6b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d6b6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d6b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d6b6-105">DESCRIPTION</span></span>
<span data-ttu-id="4d6b6-106">Polecenie cmdlet **Get-AzureRmSqlServerServiceObjective** Pobiera dostępne cele usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="4d6b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d6b6-107">EXAMPLES</span></span>

### <span data-ttu-id="4d6b6-108">Przykład 1: uzyskiwanie celów dotyczących usługi</span><span class="sxs-lookup"><span data-stu-id="4d6b6-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="4d6b6-109">To polecenie uzyskuje cele usługi dla serwera o nazwie Server01 oraz bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="4d6b6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d6b6-110">PARAMETERS</span></span>

### <span data-ttu-id="4d6b6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d6b6-111">-DatabaseName</span></span>
<span data-ttu-id="4d6b6-112">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-112">SQL Database name.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6b6-113">-DefaultProfile</span></span>
<span data-ttu-id="4d6b6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d6b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d6b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d6b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="4d6b6-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4d6b6-117">To polecenie cmdlet umożliwia pobieranie celów usługi dla serwera bazy danych SQL przypisanego do tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="4d6b6-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4d6b6-118">-ServerName</span></span>
<span data-ttu-id="4d6b6-119">Określa nazwę serwera bazy danych SQL bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="4d6b6-120">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="4d6b6-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="4d6b6-121">Określa nazwę celu usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="4d6b6-122">Dopuszczalne wartości tego parametru to: Basic, S0, S1, S2, P1, P2 i P3.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6b6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d6b6-123">-Confirm</span></span>
<span data-ttu-id="4d6b6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d6b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d6b6-125">-WhatIf</span></span>
<span data-ttu-id="4d6b6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d6b6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d6b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6b6-128">CommonParameters</span></span>
<span data-ttu-id="4d6b6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6b6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6b6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6b6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d6b6-131">INPUTS</span></span>

### <span data-ttu-id="4d6b6-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d6b6-132">None</span></span>
<span data-ttu-id="4d6b6-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4d6b6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d6b6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d6b6-134">OUTPUTS</span></span>

### <span data-ttu-id="4d6b6-135">Microsoft. Azure. Commands. SQL. serviceobject. model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="4d6b6-135">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="4d6b6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d6b6-136">NOTES</span></span>

## <span data-ttu-id="4d6b6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d6b6-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d6b6-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4d6b6-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


