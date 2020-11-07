---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c0a917d2f5e10bb499ecf6fc698bee9a84d64363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718082"
---
# <span data-ttu-id="c0797-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="c0797-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="c0797-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0797-102">SYNOPSIS</span></span>
<span data-ttu-id="c0797-103">Pobiera wskazówki dotyczące warstwy cenowej dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c0797-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0797-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0797-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0797-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0797-105">DESCRIPTION</span></span>
<span data-ttu-id="c0797-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej umożliwiające uaktualnienie bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c0797-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="c0797-107">Bazy danych, które nadal znajdują się w warstwach cenowych w sieci Web i w firmie, uzyskują wskazówkę umożliwiającą uaktualnienie nowych warstw cenowych podstawowych, standardowych i Premium.</span><span class="sxs-lookup"><span data-stu-id="c0797-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>

<span data-ttu-id="c0797-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c0797-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c0797-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0797-109">EXAMPLES</span></span>

### <span data-ttu-id="c0797-110">Przykład 1: uzyskiwanie rekomendacji dla wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="c0797-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c0797-111">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="c0797-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="c0797-112">Przykład 2: uzyskiwanie rekomendacji dla konkretnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="c0797-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c0797-113">To polecenie zwraca wskazówki dotyczące uaktualniania dla konkretnej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c0797-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="c0797-114">Przykład 3: uzyskiwanie rekomendacji dla wszystkich baz danych, które nie należą do puli Elastic Database</span><span class="sxs-lookup"><span data-stu-id="c0797-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="c0797-115">To polecenie zwraca wskazówki dotyczące uaktualniania dla wszystkich baz danych, które nie należą do puli Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="c0797-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="c0797-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0797-116">PARAMETERS</span></span>

### <span data-ttu-id="c0797-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0797-117">-DatabaseName</span></span>
<span data-ttu-id="c0797-118">Określa nazwę bazy danych SQL, dla której to polecenie cmdlet pobiera wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="c0797-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="c0797-119">Jeśli baza danych nie zostanie określona, to polecenie cmdlet będzie pobierać wskazówki dotyczące wszystkich baz danych na serwerze logicznym.</span><span class="sxs-lookup"><span data-stu-id="c0797-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0797-120">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="c0797-120">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="c0797-121">Wskazuje, czy bazy danych w pulach Elastic Database są wykluczone z zwróconych rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="c0797-121">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0797-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0797-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0797-123">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="c0797-123">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c0797-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c0797-124">-ServerName</span></span>
<span data-ttu-id="c0797-125">Określa nazwę serwera obsługującego bazę danych, dla której ten aplet polecenia uzyskuje wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="c0797-125">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="c0797-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0797-126">-Confirm</span></span>
<span data-ttu-id="c0797-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0797-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0797-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0797-128">-WhatIf</span></span>
<span data-ttu-id="c0797-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0797-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0797-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0797-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0797-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0797-131">-DefaultProfile</span></span>
<span data-ttu-id="c0797-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0797-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0797-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0797-133">CommonParameters</span></span>
<span data-ttu-id="c0797-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0797-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0797-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0797-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0797-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0797-136">INPUTS</span></span>

## <span data-ttu-id="c0797-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0797-137">OUTPUTS</span></span>

## <span data-ttu-id="c0797-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0797-138">NOTES</span></span>

## <span data-ttu-id="c0797-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0797-139">RELATED LINKS</span></span>

[<span data-ttu-id="c0797-140">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="c0797-140">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="c0797-141">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="c0797-141">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


