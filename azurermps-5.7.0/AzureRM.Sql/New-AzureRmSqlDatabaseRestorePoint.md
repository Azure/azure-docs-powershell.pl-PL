---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718007"
---
# <span data-ttu-id="07d8a-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="07d8a-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="07d8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="07d8a-103">Tworzy nowy punkt przywracania, z którego można przywrócić bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="07d8a-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07d8a-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07d8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="07d8a-106">Polecenie cmdlet **New-AzureRmSqlDatabaseRestorePoint** tworzy nowy punkt przywracania, z którego można przywrócić bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="07d8a-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="07d8a-107">To polecenie cmdlet jest obecnie obsługiwane przez usługę hurtowni danych programu SQL Server w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="07d8a-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="07d8a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07d8a-108">EXAMPLES</span></span>

### <span data-ttu-id="07d8a-109">Przykład 1. Tworzenie punktu przywracania</span><span class="sxs-lookup"><span data-stu-id="07d8a-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="07d8a-110">To polecenie tworzy punkt przywracania bazy danych Azure SQL Database i zwraca szczegóły punktu przywracania.</span><span class="sxs-lookup"><span data-stu-id="07d8a-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="07d8a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07d8a-111">PARAMETERS</span></span>

### <span data-ttu-id="07d8a-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="07d8a-112">-DatabaseName</span></span>
<span data-ttu-id="07d8a-113">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="07d8a-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d8a-114">-DefaultProfile</span></span>
<span data-ttu-id="07d8a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="07d8a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07d8a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d8a-116">-ResourceGroupName</span></span>
<span data-ttu-id="07d8a-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="07d8a-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="07d8a-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="07d8a-118">-RestorePointLabel</span></span>
<span data-ttu-id="07d8a-119">Określa etykietę punktu przywracania w celu łatwego identyfikowania.</span><span class="sxs-lookup"><span data-stu-id="07d8a-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="07d8a-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="07d8a-120">-ServerName</span></span>
<span data-ttu-id="07d8a-121">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="07d8a-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="07d8a-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07d8a-122">-Confirm</span></span>
<span data-ttu-id="07d8a-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07d8a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07d8a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d8a-124">-WhatIf</span></span>
<span data-ttu-id="07d8a-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07d8a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d8a-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07d8a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07d8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d8a-127">CommonParameters</span></span>
<span data-ttu-id="07d8a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d8a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d8a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d8a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07d8a-130">INPUTS</span></span>

## <span data-ttu-id="07d8a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07d8a-131">OUTPUTS</span></span>

## <span data-ttu-id="07d8a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07d8a-132">NOTES</span></span>

## <span data-ttu-id="07d8a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07d8a-133">RELATED LINKS</span></span>
