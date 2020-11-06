---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554191"
---
# <span data-ttu-id="16fbd-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16fbd-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="16fbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="16fbd-103">Usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="16fbd-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16fbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16fbd-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16fbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="16fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="16fbd-106">Polecenie cmdlet **Remove-AzureRmSqlDatabase** usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="16fbd-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="16fbd-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="16fbd-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="16fbd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16fbd-108">EXAMPLES</span></span>

### <span data-ttu-id="16fbd-109">Przykład 1: Usuwanie bazy danych z programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="16fbd-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="16fbd-110">To polecenie usuwa bazę danych o nazwie Database01 z serwera Server01.</span><span class="sxs-lookup"><span data-stu-id="16fbd-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="16fbd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16fbd-111">PARAMETERS</span></span>

### <span data-ttu-id="16fbd-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16fbd-112">-DatabaseName</span></span>
<span data-ttu-id="16fbd-113">Określa nazwę bazy danych, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16fbd-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16fbd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="16fbd-114">-Force</span></span>
<span data-ttu-id="16fbd-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="16fbd-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fbd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16fbd-116">-ResourceGroupName</span></span>
<span data-ttu-id="16fbd-117">Określa nazwę grupy zasobów platformy Azure, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="16fbd-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="16fbd-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="16fbd-118">-ServerName</span></span>
<span data-ttu-id="16fbd-119">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="16fbd-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="16fbd-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16fbd-120">-Confirm</span></span>
<span data-ttu-id="16fbd-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16fbd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16fbd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16fbd-122">-WhatIf</span></span>
<span data-ttu-id="16fbd-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16fbd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16fbd-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16fbd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16fbd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fbd-125">-DefaultProfile</span></span>
<span data-ttu-id="16fbd-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16fbd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16fbd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fbd-127">CommonParameters</span></span>
<span data-ttu-id="16fbd-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16fbd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fbd-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16fbd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fbd-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16fbd-130">INPUTS</span></span>

### <span data-ttu-id="16fbd-131">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="16fbd-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="16fbd-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16fbd-132">OUTPUTS</span></span>

### <span data-ttu-id="16fbd-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="16fbd-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="16fbd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16fbd-134">NOTES</span></span>

## <span data-ttu-id="16fbd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16fbd-135">RELATED LINKS</span></span>

[<span data-ttu-id="16fbd-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16fbd-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="16fbd-137">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16fbd-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="16fbd-138">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16fbd-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="16fbd-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16fbd-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="16fbd-140">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="16fbd-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="16fbd-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="16fbd-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


