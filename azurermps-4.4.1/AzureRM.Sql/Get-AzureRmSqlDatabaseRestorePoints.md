---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: 002b248195840cb7453757e92f9269e7a61d9fda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548283"
---
# <span data-ttu-id="49eb0-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="49eb0-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="49eb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="49eb0-103">Pobiera różne punkty przywracania, z których można przywrócić magazyn danych SQL.</span><span class="sxs-lookup"><span data-stu-id="49eb0-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49eb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49eb0-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49eb0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="49eb0-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseRestorePoints** umożliwia pobranie różnych punktów przywracania, z których można przywrócić magazyn danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49eb0-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="49eb0-107">W przypadku bazy danych Azure SQL Database okno przywracanie jest ciągłe.</span><span class="sxs-lookup"><span data-stu-id="49eb0-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="49eb0-108">Oznacza to, że dowolny punkt w okresie przechowywania kopii zapasowej bazy danych może być wykorzystany jako punkt przywracania.</span><span class="sxs-lookup"><span data-stu-id="49eb0-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="49eb0-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="49eb0-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="49eb0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49eb0-110">EXAMPLES</span></span>

### <span data-ttu-id="49eb0-111">Przykład 1: uzyskiwanie wszystkich punktów przywracania</span><span class="sxs-lookup"><span data-stu-id="49eb0-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
```

<span data-ttu-id="49eb0-112">To polecenie zwraca wszystkie dostępne punkty przywracania dla bazy danych Azure SQL Database o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="49eb0-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="49eb0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49eb0-113">PARAMETERS</span></span>

### <span data-ttu-id="49eb0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49eb0-114">-DatabaseName</span></span>
<span data-ttu-id="49eb0-115">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="49eb0-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="49eb0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49eb0-116">-ResourceGroupName</span></span>
<span data-ttu-id="49eb0-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="49eb0-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="49eb0-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="49eb0-118">-ServerName</span></span>
<span data-ttu-id="49eb0-119">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="49eb0-119">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="49eb0-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49eb0-120">-Confirm</span></span>
<span data-ttu-id="49eb0-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49eb0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49eb0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49eb0-122">-WhatIf</span></span>
<span data-ttu-id="49eb0-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49eb0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49eb0-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49eb0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49eb0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49eb0-125">-DefaultProfile</span></span>
<span data-ttu-id="49eb0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49eb0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49eb0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49eb0-127">CommonParameters</span></span>
<span data-ttu-id="49eb0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49eb0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49eb0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49eb0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49eb0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49eb0-130">INPUTS</span></span>

## <span data-ttu-id="49eb0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49eb0-131">OUTPUTS</span></span>

## <span data-ttu-id="49eb0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49eb0-132">NOTES</span></span>

## <span data-ttu-id="49eb0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49eb0-133">RELATED LINKS</span></span>

