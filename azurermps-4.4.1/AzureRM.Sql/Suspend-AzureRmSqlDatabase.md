---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552308"
---
# <span data-ttu-id="12bd2-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="12bd2-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="12bd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="12bd2-103">Wstrzymuje bazę danych hurtowni danych SQL.</span><span class="sxs-lookup"><span data-stu-id="12bd2-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12bd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12bd2-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12bd2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="12bd2-106">Polecenie cmdlet **Suspend-AzureRmSqlDatabase** wstrzymuje bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="12bd2-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="12bd2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="12bd2-108">Przykład 1. zawiesza bazę danych hurtowni danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="12bd2-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="12bd2-109">To polecenie zawiesza aktywną bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="12bd2-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="12bd2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="12bd2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12bd2-111">-DatabaseName</span></span>
<span data-ttu-id="12bd2-112">Określa nazwę bazy danych, która jest wstrzymywana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12bd2-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="12bd2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12bd2-113">-ResourceGroupName</span></span>
<span data-ttu-id="12bd2-114">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="12bd2-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="12bd2-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="12bd2-115">-ServerName</span></span>
<span data-ttu-id="12bd2-116">Określa nazwę serwera, który hostuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="12bd2-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="12bd2-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12bd2-117">-Confirm</span></span>
<span data-ttu-id="12bd2-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12bd2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12bd2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12bd2-119">-WhatIf</span></span>
<span data-ttu-id="12bd2-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12bd2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12bd2-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12bd2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12bd2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12bd2-122">-DefaultProfile</span></span>
<span data-ttu-id="12bd2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12bd2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12bd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bd2-124">CommonParameters</span></span>
<span data-ttu-id="12bd2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12bd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bd2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12bd2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bd2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12bd2-127">INPUTS</span></span>

### <span data-ttu-id="12bd2-128">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="12bd2-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="12bd2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12bd2-129">OUTPUTS</span></span>

### <span data-ttu-id="12bd2-130">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="12bd2-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="12bd2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12bd2-131">NOTES</span></span>
* <span data-ttu-id="12bd2-132">Polecenie cmdlet **Suspend-AzureRmSqlDatabase** działa tylko w przypadku baz danych hurtowni danych usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="12bd2-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="12bd2-133">Ta operacja nie jest obsługiwana w przypadku usługi Azure SQL Database Basic, wersji Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="12bd2-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="12bd2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12bd2-134">RELATED LINKS</span></span>

[<span data-ttu-id="12bd2-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="12bd2-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="12bd2-136">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="12bd2-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="12bd2-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="12bd2-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="12bd2-138">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="12bd2-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="12bd2-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="12bd2-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="12bd2-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="12bd2-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


