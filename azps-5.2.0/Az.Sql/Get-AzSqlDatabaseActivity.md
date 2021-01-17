---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361893"
---
# <span data-ttu-id="77d1e-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="77d1e-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="77d1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="77d1e-103">Pobiera stan operacji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="77d1e-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="77d1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77d1e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77d1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="77d1e-106">Polecenie cmdlet **Get-AzSqlDatabaseActivity** Pobiera stan operacji bazy danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="77d1e-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="77d1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="77d1e-108">Przykład 1: uzyskiwanie statusu dla wszystkich wystąpień bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="77d1e-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="77d1e-109">To polecenie zwraca stan operacji wszystkich wystąpień bazy danych SQL w puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="77d1e-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="77d1e-110">Przykład 2: uzyskiwanie statusu dla wszystkich operacji bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="77d1e-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="77d1e-111">To polecenie zwraca stan wszystkich operacji bazy danych SQL w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="77d1e-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="77d1e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77d1e-112">PARAMETERS</span></span>

### <span data-ttu-id="77d1e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77d1e-113">-DatabaseName</span></span>
<span data-ttu-id="77d1e-114">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="77d1e-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="77d1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d1e-115">-DefaultProfile</span></span>
<span data-ttu-id="77d1e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77d1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77d1e-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="77d1e-117">-ElasticPoolName</span></span>
<span data-ttu-id="77d1e-118">Określa nazwę puli Elastic Database, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="77d1e-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="77d1e-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="77d1e-119">-OperationId</span></span>
<span data-ttu-id="77d1e-120">Określa identyfikator operacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77d1e-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="77d1e-122">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="77d1e-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="77d1e-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="77d1e-123">-ServerName</span></span>
<span data-ttu-id="77d1e-124">Określa nazwę programu Microsoft SQL Server, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="77d1e-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="77d1e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77d1e-125">-Confirm</span></span>
<span data-ttu-id="77d1e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77d1e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77d1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d1e-127">-WhatIf</span></span>
<span data-ttu-id="77d1e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77d1e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77d1e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77d1e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77d1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d1e-130">CommonParameters</span></span>
<span data-ttu-id="77d1e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d1e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77d1e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d1e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d1e-133">INPUTS</span></span>

### <span data-ttu-id="77d1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="77d1e-134">System.String</span></span>

### <span data-ttu-id="77d1e-135">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77d1e-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="77d1e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77d1e-136">OUTPUTS</span></span>

### <span data-ttu-id="77d1e-137">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="77d1e-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="77d1e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77d1e-138">NOTES</span></span>

## <span data-ttu-id="77d1e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77d1e-139">RELATED LINKS</span></span>
