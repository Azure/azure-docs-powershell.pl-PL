---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368524"
---
# <span data-ttu-id="ea10b-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ea10b-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="ea10b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea10b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea10b-103">Pobiera bazę danych i jej rozwinięte wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="ea10b-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="ea10b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea10b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea10b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea10b-105">DESCRIPTION</span></span>
<span data-ttu-id="ea10b-106">Polecenie cmdlet **Get-AzSqlDatabaseExpanded** pobiera bazę danych i jej rozwinięte wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="ea10b-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="ea10b-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ea10b-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ea10b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea10b-108">EXAMPLES</span></span>

### <span data-ttu-id="ea10b-109">Przykład 1: uzyskiwanie obiektu bazy danych zawierającego informacje o klasyfikatorach warstw usług</span><span class="sxs-lookup"><span data-stu-id="ea10b-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ea10b-110">To polecenie zwraca bazę danych zawierającą rozszerzone właściwości zawierające informacje klasyfikatora dotyczące warstwy usług.</span><span class="sxs-lookup"><span data-stu-id="ea10b-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="ea10b-111">Przykład 2: Wyświetlanie obiektów bazy danych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="ea10b-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="ea10b-112">To polecenie zwraca rozwinięty obiekt bazy danych dla wszystkich baz danych w programie Server01, które zaczynają się od "bazy danych".</span><span class="sxs-lookup"><span data-stu-id="ea10b-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="ea10b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea10b-113">PARAMETERS</span></span>

### <span data-ttu-id="ea10b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea10b-114">-DatabaseName</span></span>
<span data-ttu-id="ea10b-115">Określa nazwę bazy danych, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="ea10b-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea10b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea10b-116">-DefaultProfile</span></span>
<span data-ttu-id="ea10b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ea10b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea10b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea10b-118">-ResourceGroupName</span></span>
<span data-ttu-id="ea10b-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="ea10b-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ea10b-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ea10b-120">-ServerName</span></span>
<span data-ttu-id="ea10b-121">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="ea10b-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ea10b-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea10b-122">-Confirm</span></span>
<span data-ttu-id="ea10b-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea10b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea10b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea10b-124">-WhatIf</span></span>
<span data-ttu-id="ea10b-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea10b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea10b-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea10b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea10b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea10b-127">CommonParameters</span></span>
<span data-ttu-id="ea10b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea10b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea10b-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea10b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea10b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea10b-130">INPUTS</span></span>

### <span data-ttu-id="ea10b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ea10b-131">System.String</span></span>

## <span data-ttu-id="ea10b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea10b-132">OUTPUTS</span></span>

### <span data-ttu-id="ea10b-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="ea10b-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="ea10b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea10b-134">NOTES</span></span>

## <span data-ttu-id="ea10b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea10b-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea10b-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ea10b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
