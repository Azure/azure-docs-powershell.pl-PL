---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 56254dc295b650012cdff321f4f6e77054614186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553745"
---
# <span data-ttu-id="1fe55-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="1fe55-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="1fe55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fe55-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe55-103">Pobiera bazę danych i jej rozwinięte wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="1fe55-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fe55-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1fe55-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe55-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseExpanded** pobiera bazę danych i jej rozwinięte wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="1fe55-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="1fe55-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe55-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1fe55-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fe55-108">EXAMPLES</span></span>

### <span data-ttu-id="1fe55-109">Przykład 1: uzyskiwanie obiektu bazy danych zawierającego informacje o klasyfikatorach warstw usług</span><span class="sxs-lookup"><span data-stu-id="1fe55-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1fe55-110">To polecenie zwraca bazę danych zawierającą rozszerzone właściwości zawierające informacje klasyfikatora dotyczące warstwy usług.</span><span class="sxs-lookup"><span data-stu-id="1fe55-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="1fe55-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fe55-111">PARAMETERS</span></span>

### <span data-ttu-id="1fe55-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fe55-112">-DatabaseName</span></span>
<span data-ttu-id="1fe55-113">Określa nazwę bazy danych, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="1fe55-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="1fe55-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe55-114">-ResourceGroupName</span></span>
<span data-ttu-id="1fe55-115">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="1fe55-115">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1fe55-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1fe55-116">-ServerName</span></span>
<span data-ttu-id="1fe55-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="1fe55-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1fe55-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fe55-118">-Confirm</span></span>
<span data-ttu-id="1fe55-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe55-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe55-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe55-120">-WhatIf</span></span>
<span data-ttu-id="1fe55-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe55-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe55-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1fe55-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe55-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe55-123">-DefaultProfile</span></span>
<span data-ttu-id="1fe55-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe55-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe55-125">CommonParameters</span></span>
<span data-ttu-id="1fe55-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe55-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe55-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe55-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fe55-128">INPUTS</span></span>

## <span data-ttu-id="1fe55-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fe55-129">OUTPUTS</span></span>

## <span data-ttu-id="1fe55-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fe55-130">NOTES</span></span>

## <span data-ttu-id="1fe55-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fe55-131">RELATED LINKS</span></span>

[<span data-ttu-id="1fe55-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1fe55-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
