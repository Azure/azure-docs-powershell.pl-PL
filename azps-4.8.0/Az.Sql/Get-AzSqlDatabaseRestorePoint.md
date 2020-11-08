---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063158"
---
# <span data-ttu-id="44cb8-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="44cb8-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="44cb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="44cb8-103">Pobiera różne punkty przywracania, z których można przywrócić magazyn danych SQL.</span><span class="sxs-lookup"><span data-stu-id="44cb8-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="44cb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44cb8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44cb8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="44cb8-106">Polecenie cmdlet **Get-AzSqlDatabaseRestorePoint** umożliwia pobranie różnych punktów przywracania, z których można przywrócić magazyn danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44cb8-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="44cb8-107">W przypadku bazy danych Azure SQL Database okno przywracanie jest ciągłe.</span><span class="sxs-lookup"><span data-stu-id="44cb8-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="44cb8-108">Oznacza to, że dowolny punkt w okresie przechowywania kopii zapasowej bazy danych może być wykorzystany jako punkt przywracania.</span><span class="sxs-lookup"><span data-stu-id="44cb8-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="44cb8-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="44cb8-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="44cb8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44cb8-110">EXAMPLES</span></span>

### <span data-ttu-id="44cb8-111">Przykład 1: uzyskiwanie wszystkich punktów przywracania</span><span class="sxs-lookup"><span data-stu-id="44cb8-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="44cb8-112">To polecenie zwraca wszystkie dostępne punkty przywracania dla bazy danych Azure SQL Database o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="44cb8-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="44cb8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44cb8-113">PARAMETERS</span></span>

### <span data-ttu-id="44cb8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="44cb8-114">-DatabaseName</span></span>
<span data-ttu-id="44cb8-115">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="44cb8-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="44cb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cb8-116">-DefaultProfile</span></span>
<span data-ttu-id="44cb8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="44cb8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44cb8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cb8-118">-ResourceGroupName</span></span>
<span data-ttu-id="44cb8-119">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="44cb8-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="44cb8-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="44cb8-120">-ServerName</span></span>
<span data-ttu-id="44cb8-121">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="44cb8-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="44cb8-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44cb8-122">-Confirm</span></span>
<span data-ttu-id="44cb8-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cb8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44cb8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44cb8-124">-WhatIf</span></span>
<span data-ttu-id="44cb8-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cb8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44cb8-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44cb8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44cb8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cb8-127">CommonParameters</span></span>
<span data-ttu-id="44cb8-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cb8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cb8-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44cb8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cb8-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44cb8-130">INPUTS</span></span>

### <span data-ttu-id="44cb8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="44cb8-131">System.String</span></span>

## <span data-ttu-id="44cb8-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44cb8-132">OUTPUTS</span></span>

### <span data-ttu-id="44cb8-133">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="44cb8-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="44cb8-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44cb8-134">NOTES</span></span>

## <span data-ttu-id="44cb8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44cb8-135">RELATED LINKS</span></span>
