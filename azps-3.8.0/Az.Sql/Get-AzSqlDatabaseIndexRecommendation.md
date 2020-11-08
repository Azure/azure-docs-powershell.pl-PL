---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050508"
---
# <span data-ttu-id="2c60c-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="2c60c-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="2c60c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c60c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c60c-103">Pobiera zalecane operacje indeksowania dla serwera lub bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c60c-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="2c60c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c60c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c60c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c60c-105">DESCRIPTION</span></span>
<span data-ttu-id="2c60c-106">Polecenie cmdlet **Get-AzSqlDatabaseIndexRecommendation** pobiera zalecane operacje indeksowania dla serwera bazy danych Azure SQL lub bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c60c-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="2c60c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c60c-107">EXAMPLES</span></span>

### <span data-ttu-id="2c60c-108">Przykład 1: Uzyskaj zalecenia dotyczące indeksu dla wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="2c60c-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="2c60c-109">To polecenie zwraca zalecenia dotyczące indeksu dla wszystkich baz danych na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="2c60c-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="2c60c-110">Przykład 2: uzyskiwanie rekomendacji dotyczących indeksu dla konkretnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="2c60c-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="2c60c-111">To polecenie zwraca zalecenia dotyczące indeksu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c60c-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="2c60c-112">Przykład 3: uzyskiwanie jednego zalecenia dotyczącego indeksu według nazwy</span><span class="sxs-lookup"><span data-stu-id="2c60c-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="2c60c-113">To polecenie zwraca zalecenie dotyczące pojedynczego indeksu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2c60c-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="2c60c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c60c-114">PARAMETERS</span></span>

### <span data-ttu-id="2c60c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c60c-115">-DatabaseName</span></span>
<span data-ttu-id="2c60c-116">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera zalecenia dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="2c60c-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="2c60c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c60c-117">-DefaultProfile</span></span>
<span data-ttu-id="2c60c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2c60c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c60c-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="2c60c-119">-IndexRecommendationName</span></span>
<span data-ttu-id="2c60c-120">Określa nazwę zalecenia dotyczącego indeksu, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c60c-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2c60c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c60c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2c60c-122">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="2c60c-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="2c60c-123">To polecenie cmdlet umożliwia indeksowanie rekomendacji dla bazy danych hostowanej przez ten serwer.</span><span class="sxs-lookup"><span data-stu-id="2c60c-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="2c60c-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2c60c-124">-ServerName</span></span>
<span data-ttu-id="2c60c-125">Określa serwer, na którym znajduje się baza danych, dla której to polecenie cmdlet pobiera zalecenia dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="2c60c-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="2c60c-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="2c60c-126">-TableName</span></span>
<span data-ttu-id="2c60c-127">Określa nazwę tabeli SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c60c-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="2c60c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c60c-128">-Confirm</span></span>
<span data-ttu-id="2c60c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c60c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c60c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c60c-130">-WhatIf</span></span>
<span data-ttu-id="2c60c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c60c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c60c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c60c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c60c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c60c-133">CommonParameters</span></span>
<span data-ttu-id="2c60c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c60c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c60c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c60c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c60c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c60c-136">INPUTS</span></span>

### <span data-ttu-id="2c60c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2c60c-137">System.String</span></span>

## <span data-ttu-id="2c60c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c60c-138">OUTPUTS</span></span>

### <span data-ttu-id="2c60c-139">Microsoft. Azure. Commands. SQL. model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="2c60c-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="2c60c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c60c-140">NOTES</span></span>

## <span data-ttu-id="2c60c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c60c-141">RELATED LINKS</span></span>

[<span data-ttu-id="2c60c-142">Start — AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="2c60c-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="2c60c-143">Zatrzymaj — AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="2c60c-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
