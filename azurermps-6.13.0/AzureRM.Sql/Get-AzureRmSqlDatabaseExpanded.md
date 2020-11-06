---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: f2ee19834cdb4144c8f207ae8ff10a90a733bece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544792"
---
# <span data-ttu-id="fddc5-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="fddc5-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="fddc5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fddc5-102">SYNOPSIS</span></span>
<span data-ttu-id="fddc5-103">Pobiera bazę danych i jej rozwinięte wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="fddc5-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fddc5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fddc5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fddc5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fddc5-105">DESCRIPTION</span></span>
<span data-ttu-id="fddc5-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseExpanded** pobiera bazę danych i jej rozwinięte wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="fddc5-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="fddc5-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fddc5-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fddc5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fddc5-108">EXAMPLES</span></span>

### <span data-ttu-id="fddc5-109">Przykład 1: uzyskiwanie obiektu bazy danych zawierającego informacje o klasyfikatorach warstw usług</span><span class="sxs-lookup"><span data-stu-id="fddc5-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fddc5-110">To polecenie zwraca bazę danych zawierającą rozszerzone właściwości zawierające informacje klasyfikatora dotyczące warstwy usług.</span><span class="sxs-lookup"><span data-stu-id="fddc5-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="fddc5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fddc5-111">PARAMETERS</span></span>

### <span data-ttu-id="fddc5-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fddc5-112">-DatabaseName</span></span>
<span data-ttu-id="fddc5-113">Określa nazwę bazy danych, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="fddc5-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="fddc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddc5-114">-DefaultProfile</span></span>
<span data-ttu-id="fddc5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fddc5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fddc5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fddc5-116">-ResourceGroupName</span></span>
<span data-ttu-id="fddc5-117">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="fddc5-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fddc5-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fddc5-118">-ServerName</span></span>
<span data-ttu-id="fddc5-119">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="fddc5-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fddc5-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fddc5-120">-Confirm</span></span>
<span data-ttu-id="fddc5-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fddc5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fddc5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fddc5-122">-WhatIf</span></span>
<span data-ttu-id="fddc5-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fddc5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fddc5-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fddc5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fddc5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddc5-125">CommonParameters</span></span>
<span data-ttu-id="fddc5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fddc5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddc5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fddc5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddc5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fddc5-128">INPUTS</span></span>

### <span data-ttu-id="fddc5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fddc5-129">System.String</span></span>

## <span data-ttu-id="fddc5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fddc5-130">OUTPUTS</span></span>

### <span data-ttu-id="fddc5-131">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="fddc5-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="fddc5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fddc5-132">NOTES</span></span>

## <span data-ttu-id="fddc5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fddc5-133">RELATED LINKS</span></span>

[<span data-ttu-id="fddc5-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fddc5-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
