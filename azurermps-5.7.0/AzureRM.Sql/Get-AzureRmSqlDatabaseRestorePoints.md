---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserestorepoints
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: fac0e279bb52ecf17246926875daea4392e23e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547928"
---
# <span data-ttu-id="6373f-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="6373f-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="6373f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6373f-102">SYNOPSIS</span></span>
<span data-ttu-id="6373f-103">Pobiera różne punkty przywracania, z których można przywrócić magazyn danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6373f-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6373f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6373f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6373f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6373f-105">DESCRIPTION</span></span>
<span data-ttu-id="6373f-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseRestorePoints** umożliwia pobranie różnych punktów przywracania, z których można przywrócić magazyn danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6373f-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="6373f-107">W przypadku bazy danych Azure SQL Database okno przywracanie jest ciągłe.</span><span class="sxs-lookup"><span data-stu-id="6373f-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="6373f-108">Oznacza to, że dowolny punkt w okresie przechowywania kopii zapasowej bazy danych może być wykorzystany jako punkt przywracania.</span><span class="sxs-lookup"><span data-stu-id="6373f-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="6373f-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6373f-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6373f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6373f-110">EXAMPLES</span></span>

### <span data-ttu-id="6373f-111">Przykład 1: uzyskiwanie wszystkich punktów przywracania</span><span class="sxs-lookup"><span data-stu-id="6373f-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="6373f-112">To polecenie zwraca wszystkie dostępne punkty przywracania dla bazy danych Azure SQL Database o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="6373f-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="6373f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6373f-113">PARAMETERS</span></span>

### <span data-ttu-id="6373f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6373f-114">-DatabaseName</span></span>
<span data-ttu-id="6373f-115">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6373f-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="6373f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6373f-116">-DefaultProfile</span></span>
<span data-ttu-id="6373f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6373f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6373f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6373f-118">-ResourceGroupName</span></span>
<span data-ttu-id="6373f-119">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6373f-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="6373f-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6373f-120">-ServerName</span></span>
<span data-ttu-id="6373f-121">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="6373f-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="6373f-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6373f-122">-Confirm</span></span>
<span data-ttu-id="6373f-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6373f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6373f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6373f-124">-WhatIf</span></span>
<span data-ttu-id="6373f-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6373f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6373f-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6373f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6373f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6373f-127">CommonParameters</span></span>
<span data-ttu-id="6373f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6373f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6373f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6373f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6373f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6373f-130">INPUTS</span></span>

### <span data-ttu-id="6373f-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6373f-131">None</span></span>
<span data-ttu-id="6373f-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6373f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6373f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6373f-133">OUTPUTS</span></span>

## <span data-ttu-id="6373f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6373f-134">NOTES</span></span>

## <span data-ttu-id="6373f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6373f-135">RELATED LINKS</span></span>
