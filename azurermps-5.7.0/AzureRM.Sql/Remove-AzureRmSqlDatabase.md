---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 3da5093decdaea29d1a225db5c683d2f23f7115f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547859"
---
# <span data-ttu-id="4a38d-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a38d-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="4a38d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a38d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a38d-103">Usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4a38d-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a38d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a38d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a38d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a38d-105">DESCRIPTION</span></span>
<span data-ttu-id="4a38d-106">Polecenie cmdlet **Remove-AzureRmSqlDatabase** usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4a38d-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="4a38d-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4a38d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4a38d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a38d-108">EXAMPLES</span></span>

### <span data-ttu-id="4a38d-109">Przykład 1: Usuwanie bazy danych z programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="4a38d-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4a38d-110">To polecenie usuwa bazę danych o nazwie Database01 z serwera Server01.</span><span class="sxs-lookup"><span data-stu-id="4a38d-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="4a38d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a38d-111">PARAMETERS</span></span>

### <span data-ttu-id="4a38d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a38d-112">-DatabaseName</span></span>
<span data-ttu-id="4a38d-113">Określa nazwę bazy danych, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a38d-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a38d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a38d-114">-DefaultProfile</span></span>
<span data-ttu-id="4a38d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4a38d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a38d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4a38d-116">-Force</span></span>
<span data-ttu-id="4a38d-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4a38d-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a38d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a38d-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a38d-119">Określa nazwę grupy zasobów platformy Azure, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4a38d-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4a38d-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4a38d-120">-ServerName</span></span>
<span data-ttu-id="4a38d-121">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4a38d-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4a38d-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a38d-122">-Confirm</span></span>
<span data-ttu-id="4a38d-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a38d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a38d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a38d-124">-WhatIf</span></span>
<span data-ttu-id="4a38d-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a38d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a38d-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a38d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a38d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a38d-127">CommonParameters</span></span>
<span data-ttu-id="4a38d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a38d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a38d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a38d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a38d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a38d-130">INPUTS</span></span>

### <span data-ttu-id="4a38d-131">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4a38d-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4a38d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a38d-132">OUTPUTS</span></span>

### <span data-ttu-id="4a38d-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4a38d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4a38d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a38d-134">NOTES</span></span>

## <span data-ttu-id="4a38d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a38d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4a38d-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a38d-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="4a38d-137">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a38d-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="4a38d-138">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a38d-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="4a38d-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a38d-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="4a38d-140">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4a38d-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="4a38d-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4a38d-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


