---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718681"
---
# <span data-ttu-id="0214f-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="0214f-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="0214f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0214f-102">SYNOPSIS</span></span>
<span data-ttu-id="0214f-103">Umożliwia pobieranie celów usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0214f-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0214f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0214f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0214f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0214f-105">DESCRIPTION</span></span>
<span data-ttu-id="0214f-106">Polecenie cmdlet **Get-AzureRmSqlServerServiceObjective** Pobiera dostępne cele usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0214f-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="0214f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0214f-107">EXAMPLES</span></span>

### <span data-ttu-id="0214f-108">Przykład 1: uzyskiwanie celów dotyczących usługi</span><span class="sxs-lookup"><span data-stu-id="0214f-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="0214f-109">To polecenie uzyskuje cele usługi dla serwera o nazwie Server01 oraz bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="0214f-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="0214f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0214f-110">PARAMETERS</span></span>

### <span data-ttu-id="0214f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0214f-111">-DatabaseName</span></span>
<span data-ttu-id="0214f-112">Określa nazwę bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0214f-112">Specifies the name of an Azure SQL Database.</span></span>

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

### <span data-ttu-id="0214f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0214f-113">-ResourceGroupName</span></span>
<span data-ttu-id="0214f-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0214f-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0214f-115">To polecenie cmdlet umożliwia pobieranie celów usługi dla serwera bazy danych SQL przypisanego do tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="0214f-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="0214f-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0214f-116">-ServerName</span></span>
<span data-ttu-id="0214f-117">Określa nazwę serwera bazy danych SQL bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0214f-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="0214f-118">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="0214f-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="0214f-119">Określa nazwę celu usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0214f-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="0214f-120">Dopuszczalne wartości tego parametru to: Basic, S0, S1, S2, P1, P2 i P3.</span><span class="sxs-lookup"><span data-stu-id="0214f-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="0214f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0214f-121">-Confirm</span></span>
<span data-ttu-id="0214f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0214f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0214f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0214f-123">-WhatIf</span></span>
<span data-ttu-id="0214f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0214f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0214f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0214f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0214f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0214f-126">-DefaultProfile</span></span>
<span data-ttu-id="0214f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0214f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0214f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0214f-128">CommonParameters</span></span>
<span data-ttu-id="0214f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0214f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0214f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0214f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0214f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0214f-131">INPUTS</span></span>

## <span data-ttu-id="0214f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0214f-132">OUTPUTS</span></span>

### <span data-ttu-id="0214f-133">Microsoft. Azure. Commands. SQL. serviceobject. model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="0214f-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="0214f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0214f-134">NOTES</span></span>

## <span data-ttu-id="0214f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0214f-135">RELATED LINKS</span></span>

[<span data-ttu-id="0214f-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0214f-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


