---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 91c23a32fd25c184e46249424b439375caed6ac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886725"
---
# <span data-ttu-id="aa256-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="aa256-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="aa256-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa256-102">SYNOPSIS</span></span>
<span data-ttu-id="aa256-103">Pobiera stan operacji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="aa256-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="aa256-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa256-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa256-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa256-105">DESCRIPTION</span></span>
<span data-ttu-id="aa256-106">Polecenie cmdlet **Get-AzSqlDatabaseActivity** Pobiera stan operacji bazy danych w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="aa256-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="aa256-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa256-107">EXAMPLES</span></span>

### <span data-ttu-id="aa256-108">Przykład 1: uzyskiwanie statusu dla wszystkich wystąpień bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="aa256-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="aa256-109">To polecenie zwraca stan operacji wszystkich wystąpień bazy danych SQL w puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="aa256-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="aa256-110">Przykład 2: uzyskiwanie statusu dla wszystkich operacji bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="aa256-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="aa256-111">To polecenie zwraca stan wszystkich operacji bazy danych SQL w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="aa256-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="aa256-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa256-112">PARAMETERS</span></span>

### <span data-ttu-id="aa256-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa256-113">-DatabaseName</span></span>
<span data-ttu-id="aa256-114">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="aa256-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="aa256-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa256-115">-DefaultProfile</span></span>
<span data-ttu-id="aa256-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa256-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa256-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="aa256-117">-ElasticPoolName</span></span>
<span data-ttu-id="aa256-118">Określa nazwę puli Elastic Database, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="aa256-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="aa256-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="aa256-119">-OperationId</span></span>
<span data-ttu-id="aa256-120">Określa identyfikator operacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa256-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aa256-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa256-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa256-122">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="aa256-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="aa256-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="aa256-123">-ServerName</span></span>
<span data-ttu-id="aa256-124">Określa nazwę programu Microsoft SQL Server, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="aa256-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="aa256-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa256-125">-Confirm</span></span>
<span data-ttu-id="aa256-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa256-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa256-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa256-127">-WhatIf</span></span>
<span data-ttu-id="aa256-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa256-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa256-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa256-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa256-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa256-130">CommonParameters</span></span>
<span data-ttu-id="aa256-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa256-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa256-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa256-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa256-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa256-133">INPUTS</span></span>

### <span data-ttu-id="aa256-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aa256-134">System.String</span></span>

### <span data-ttu-id="aa256-135">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aa256-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aa256-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa256-136">OUTPUTS</span></span>

### <span data-ttu-id="aa256-137">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="aa256-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="aa256-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa256-138">NOTES</span></span>

## <span data-ttu-id="aa256-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa256-139">RELATED LINKS</span></span>
