---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: b4238ff85a35bcf6a48016a005af8a1f889332cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718413"
---
# <span data-ttu-id="a3671-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a3671-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a3671-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3671-102">SYNOPSIS</span></span>
<span data-ttu-id="a3671-103">Wstrzymuje bazę danych hurtowni danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a3671-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3671-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3671-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3671-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3671-105">DESCRIPTION</span></span>
<span data-ttu-id="a3671-106">Polecenie cmdlet **Suspend-AzureRmSqlDatabase** wstrzymuje bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a3671-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a3671-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3671-107">EXAMPLES</span></span>

### <span data-ttu-id="a3671-108">Przykład 1. zawiesza bazę danych hurtowni danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a3671-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a3671-109">To polecenie zawiesza aktywną bazę danych hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a3671-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a3671-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3671-110">PARAMETERS</span></span>

### <span data-ttu-id="a3671-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3671-111">-AsJob</span></span>
<span data-ttu-id="a3671-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a3671-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="a3671-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a3671-113">-DatabaseName</span></span>
<span data-ttu-id="a3671-114">Określa nazwę bazy danych, która jest wstrzymywana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3671-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="a3671-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3671-115">-DefaultProfile</span></span>
<span data-ttu-id="a3671-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a3671-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3671-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3671-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3671-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="a3671-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a3671-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a3671-119">-ServerName</span></span>
<span data-ttu-id="a3671-120">Określa nazwę serwera, który hostuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a3671-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="a3671-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3671-121">-Confirm</span></span>
<span data-ttu-id="a3671-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3671-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3671-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3671-123">-WhatIf</span></span>
<span data-ttu-id="a3671-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3671-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3671-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3671-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3671-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3671-126">CommonParameters</span></span>
<span data-ttu-id="a3671-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3671-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3671-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3671-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3671-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3671-129">INPUTS</span></span>

### <span data-ttu-id="a3671-130">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a3671-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a3671-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3671-131">OUTPUTS</span></span>

### <span data-ttu-id="a3671-132">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a3671-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a3671-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3671-133">NOTES</span></span>
* <span data-ttu-id="a3671-134">Polecenie cmdlet **Suspend-AzureRmSqlDatabase** działa tylko w przypadku baz danych hurtowni danych usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a3671-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a3671-135">Ta operacja nie jest obsługiwana w przypadku usługi Azure SQL Database Basic, wersji Standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="a3671-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a3671-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3671-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3671-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a3671-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a3671-138">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a3671-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a3671-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a3671-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a3671-140">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a3671-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="a3671-141">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a3671-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a3671-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a3671-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


