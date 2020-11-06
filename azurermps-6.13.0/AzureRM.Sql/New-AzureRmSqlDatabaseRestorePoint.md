---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: dad714b617f6b3c493d19b2275dcf7eeef14a2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547347"
---
# <span data-ttu-id="a7d54-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a7d54-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="a7d54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7d54-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d54-103">Tworzy nowy punkt przywracania, z którego można przywrócić bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a7d54-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7d54-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7d54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7d54-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d54-106">Polecenie cmdlet **New-AzureRmSqlDatabaseRestorePoint** tworzy nowy punkt przywracania, z którego można przywrócić magazyn danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d54-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="a7d54-107">To polecenie cmdlet jest obecnie obsługiwane w przypadku hurtowni danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d54-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="a7d54-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7d54-108">EXAMPLES</span></span>

### <span data-ttu-id="a7d54-109">Przykład 1. Tworzenie punktu przywracania</span><span class="sxs-lookup"><span data-stu-id="a7d54-109">Example 1: Create a restore point</span></span>
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

<span data-ttu-id="a7d54-110">To polecenie tworzy punkt przywracania dla hurtowni danych SQL Azure i zwraca szczegóły punktu przywracania.</span><span class="sxs-lookup"><span data-stu-id="a7d54-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="a7d54-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7d54-111">PARAMETERS</span></span>

### <span data-ttu-id="a7d54-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7d54-112">-DatabaseName</span></span>
<span data-ttu-id="a7d54-113">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a7d54-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d54-114">-DefaultProfile</span></span>
<span data-ttu-id="a7d54-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a7d54-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7d54-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d54-116">-ResourceGroupName</span></span>
<span data-ttu-id="a7d54-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a7d54-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="a7d54-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="a7d54-118">-RestorePointLabel</span></span>
<span data-ttu-id="a7d54-119">Określa etykietę punktu przywracania w celu łatwego identyfikowania.</span><span class="sxs-lookup"><span data-stu-id="a7d54-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="a7d54-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a7d54-120">-ServerName</span></span>
<span data-ttu-id="a7d54-121">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="a7d54-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="a7d54-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7d54-122">-Confirm</span></span>
<span data-ttu-id="a7d54-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d54-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d54-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d54-124">-WhatIf</span></span>
<span data-ttu-id="a7d54-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d54-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7d54-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7d54-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d54-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d54-127">CommonParameters</span></span>
<span data-ttu-id="a7d54-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d54-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d54-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d54-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d54-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7d54-130">INPUTS</span></span>

### <span data-ttu-id="a7d54-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d54-131">System.String</span></span>

## <span data-ttu-id="a7d54-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7d54-132">OUTPUTS</span></span>

### <span data-ttu-id="a7d54-133">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="a7d54-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="a7d54-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7d54-134">NOTES</span></span>

## <span data-ttu-id="a7d54-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7d54-135">RELATED LINKS</span></span>
