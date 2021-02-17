---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198579"
---
# <span data-ttu-id="a7192-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a7192-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="a7192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7192-102">SYNOPSIS</span></span>
<span data-ttu-id="a7192-103">Pobiera odrębne punkty przywracania, z których można przywrócić magazyn danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a7192-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="a7192-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7192-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7192-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7192-105">DESCRIPTION</span></span>
<span data-ttu-id="a7192-106">Polecenie **cmdlet Get-AzSqlDatabaseRestorePoint** pobiera odrębne punkty przywracania, z których można przywrócić magazyn danych języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a7192-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="a7192-107">W przypadku usługi Azure SQL Database okno przywracania jest ciągłe.</span><span class="sxs-lookup"><span data-stu-id="a7192-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="a7192-108">Oznacza to, że każdy punkt w czasie w okresie przechowywania kopii zapasowej bazy danych może być używany jako punkt przywracania.</span><span class="sxs-lookup"><span data-stu-id="a7192-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="a7192-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a7192-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a7192-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7192-110">EXAMPLES</span></span>

### <span data-ttu-id="a7192-111">Przykład 1. Uzyskiwanie wszystkich punktów przywracania</span><span class="sxs-lookup"><span data-stu-id="a7192-111">Example 1: Get all restore points</span></span>
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

<span data-ttu-id="a7192-112">To polecenie zwraca wszystkie dostępne punkty przywracania dla usługi Azure SQL Database o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="a7192-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="a7192-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7192-113">PARAMETERS</span></span>

### <span data-ttu-id="a7192-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7192-114">-DatabaseName</span></span>
<span data-ttu-id="a7192-115">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a7192-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="a7192-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7192-116">-DefaultProfile</span></span>
<span data-ttu-id="a7192-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a7192-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7192-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7192-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7192-119">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a7192-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="a7192-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7192-120">-ServerName</span></span>
<span data-ttu-id="a7192-121">Określa nazwę serwera AzureSQL, który hostuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a7192-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="a7192-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7192-122">-Confirm</span></span>
<span data-ttu-id="a7192-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7192-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7192-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7192-124">-WhatIf</span></span>
<span data-ttu-id="a7192-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7192-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7192-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a7192-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7192-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7192-127">CommonParameters</span></span>
<span data-ttu-id="a7192-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7192-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7192-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7192-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7192-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7192-130">INPUTS</span></span>

### <span data-ttu-id="a7192-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a7192-131">System.String</span></span>

## <span data-ttu-id="a7192-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7192-132">OUTPUTS</span></span>

### <span data-ttu-id="a7192-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="a7192-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="a7192-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7192-134">NOTES</span></span>

## <span data-ttu-id="a7192-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7192-135">RELATED LINKS</span></span>
