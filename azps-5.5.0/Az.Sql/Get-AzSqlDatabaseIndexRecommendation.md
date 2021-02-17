---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188099"
---
# <span data-ttu-id="ab232-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ab232-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="ab232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab232-102">SYNOPSIS</span></span>
<span data-ttu-id="ab232-103">Pobiera zalecane operacje indeksowania dla serwera lub bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab232-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="ab232-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab232-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab232-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab232-105">DESCRIPTION</span></span>
<span data-ttu-id="ab232-106">Polecenie **cmdlet Get-AzSqlDatabaseIndexRecommendation** pobiera zalecane operacje indeksowania dla serwera lub bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ab232-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="ab232-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab232-107">EXAMPLES</span></span>

### <span data-ttu-id="ab232-108">Przykład 1. Uzyskiwanie zaleceń dotyczących indeksu dla wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="ab232-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="ab232-109">To polecenie zwraca zalecenia dotyczące indeksu dla wszystkich baz danych na serwerze server01.</span><span class="sxs-lookup"><span data-stu-id="ab232-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="ab232-110">Przykład 2. Uzyskiwanie zaleceń dotyczących indeksu dla określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="ab232-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ab232-111">To polecenie zwraca zalecenia dotyczące indeksu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab232-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="ab232-112">Przykład 3. Uzyskiwanie zalecenia dotyczącego pojedynczego indeksu według nazwy</span><span class="sxs-lookup"><span data-stu-id="ab232-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ab232-113">To polecenie zwraca zalecenia dotyczące pojedynczego indeksu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ab232-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="ab232-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab232-114">PARAMETERS</span></span>

### <span data-ttu-id="ab232-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab232-115">-DatabaseName</span></span>
<span data-ttu-id="ab232-116">Określa nazwę bazy danych, dla której to polecenie cmdlet otrzymuje zalecenia dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="ab232-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="ab232-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab232-117">-DefaultProfile</span></span>
<span data-ttu-id="ab232-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ab232-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab232-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ab232-119">-IndexRecommendationName</span></span>
<span data-ttu-id="ab232-120">Określa nazwę indeksu, do których ma trafić to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab232-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ab232-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab232-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab232-122">Określa nazwę grupy zasobów, do których jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="ab232-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="ab232-123">To polecenie cmdlet pobiera zalecenia dotyczące indeksu dla bazy danych hostowanej przez ten serwer.</span><span class="sxs-lookup"><span data-stu-id="ab232-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="ab232-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ab232-124">-ServerName</span></span>
<span data-ttu-id="ab232-125">Określa serwer hostowany bazę danych, dla której to polecenie cmdlet otrzymuje zalecenia dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="ab232-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="ab232-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="ab232-126">-TableName</span></span>
<span data-ttu-id="ab232-127">Określa nazwę tabeli Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ab232-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="ab232-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab232-128">-Confirm</span></span>
<span data-ttu-id="ab232-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab232-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab232-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab232-130">-WhatIf</span></span>
<span data-ttu-id="ab232-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab232-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab232-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ab232-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab232-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab232-133">CommonParameters</span></span>
<span data-ttu-id="ab232-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab232-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab232-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab232-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab232-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab232-136">INPUTS</span></span>

### <span data-ttu-id="ab232-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ab232-137">System.String</span></span>

## <span data-ttu-id="ab232-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab232-138">OUTPUTS</span></span>

### <span data-ttu-id="ab232-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ab232-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ab232-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab232-140">NOTES</span></span>

## <span data-ttu-id="ab232-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab232-141">RELATED LINKS</span></span>

[<span data-ttu-id="ab232-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ab232-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ab232-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ab232-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
