---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseindexrecommendations
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: 6e9622565017f71c8b73e70e7aa4d0c3528bc254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524850"
---
# <span data-ttu-id="91244-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="91244-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="91244-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91244-102">SYNOPSIS</span></span>
<span data-ttu-id="91244-103">Pobiera zalecane operacje indeksowania dla serwera lub bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91244-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91244-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91244-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91244-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91244-105">DESCRIPTION</span></span>
<span data-ttu-id="91244-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseIndexRecommendations** pobiera zalecane operacje indeksowania dla serwera bazy danych Azure SQL lub bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91244-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="91244-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91244-107">EXAMPLES</span></span>

### <span data-ttu-id="91244-108">Przykład 1: Uzyskaj zalecenia dotyczące indeksu dla wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="91244-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="91244-109">To polecenie zwraca zalecenia dotyczące indeksu dla wszystkich baz danych na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="91244-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="91244-110">Przykład 2: uzyskiwanie rekomendacji dotyczących indeksu dla konkretnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="91244-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="91244-111">To polecenie zwraca zalecenia dotyczące indeksu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="91244-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="91244-112">Przykład 3: uzyskiwanie jednego zalecenia dotyczącego indeksu według nazwy</span><span class="sxs-lookup"><span data-stu-id="91244-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="91244-113">To polecenie zwraca zalecenie dotyczące pojedynczego indeksu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="91244-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="91244-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91244-114">PARAMETERS</span></span>

### <span data-ttu-id="91244-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91244-115">-DatabaseName</span></span>
<span data-ttu-id="91244-116">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera zalecenia dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="91244-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91244-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91244-117">-DefaultProfile</span></span>
<span data-ttu-id="91244-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="91244-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91244-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="91244-119">-IndexRecommendationName</span></span>
<span data-ttu-id="91244-120">Określa nazwę zalecenia dotyczącego indeksu, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91244-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91244-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91244-121">-ResourceGroupName</span></span>
<span data-ttu-id="91244-122">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="91244-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="91244-123">To polecenie cmdlet umożliwia indeksowanie rekomendacji dla bazy danych hostowanej przez ten serwer.</span><span class="sxs-lookup"><span data-stu-id="91244-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="91244-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="91244-124">-ServerName</span></span>
<span data-ttu-id="91244-125">Określa serwer, na którym znajduje się baza danych, dla której to polecenie cmdlet pobiera zalecenia dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="91244-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91244-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="91244-126">-TableName</span></span>
<span data-ttu-id="91244-127">Określa nazwę tabeli SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="91244-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91244-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91244-128">-Confirm</span></span>
<span data-ttu-id="91244-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91244-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91244-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91244-130">-WhatIf</span></span>
<span data-ttu-id="91244-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91244-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91244-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91244-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91244-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91244-133">CommonParameters</span></span>
<span data-ttu-id="91244-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91244-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91244-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91244-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91244-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91244-136">INPUTS</span></span>

### <span data-ttu-id="91244-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="91244-137">None</span></span>
<span data-ttu-id="91244-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="91244-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91244-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91244-139">OUTPUTS</span></span>

## <span data-ttu-id="91244-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91244-140">NOTES</span></span>

## <span data-ttu-id="91244-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91244-141">RELATED LINKS</span></span>

[<span data-ttu-id="91244-142">Start — AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="91244-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="91244-143">Zatrzymaj — AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="91244-143">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)