---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 8fb320c2caa4993b7880ef719a3d9ea0e0e8c811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956586"
---
# <span data-ttu-id="54d1f-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="54d1f-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="54d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="54d1f-103">Tworzy nowy punkt przywracania, z którego można przywrócić bazę danych SQL.</span><span class="sxs-lookup"><span data-stu-id="54d1f-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="54d1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54d1f-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54d1f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="54d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="54d1f-106">Polecenie cmdlet **New-AzSqlDatabaseRestorePoint** tworzy nowy punkt przywracania, z którym można przywrócić magazyn danych języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="54d1f-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="54d1f-107">To polecenie cmdlet jest obecnie obsługiwane w usłudze Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="54d1f-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="54d1f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54d1f-108">EXAMPLES</span></span>

### <span data-ttu-id="54d1f-109">Przykład 1. Tworzenie punktu przywracania</span><span class="sxs-lookup"><span data-stu-id="54d1f-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="54d1f-110">To polecenie tworzy punkt przywracania dla usługi Azure SQL Data Warehouse i zwraca szczegóły punktu przywracania.</span><span class="sxs-lookup"><span data-stu-id="54d1f-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="54d1f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54d1f-111">PARAMETERS</span></span>

### <span data-ttu-id="54d1f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54d1f-112">-DatabaseName</span></span>
<span data-ttu-id="54d1f-113">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="54d1f-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="54d1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d1f-114">-DefaultProfile</span></span>
<span data-ttu-id="54d1f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="54d1f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54d1f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d1f-116">-ResourceGroupName</span></span>
<span data-ttu-id="54d1f-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="54d1f-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="54d1f-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="54d1f-118">-RestorePointLabel</span></span>
<span data-ttu-id="54d1f-119">Określa etykietę punktu przywracania w celu łatwej identyfikacji.</span><span class="sxs-lookup"><span data-stu-id="54d1f-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="54d1f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54d1f-120">-ServerName</span></span>
<span data-ttu-id="54d1f-121">Określa nazwę serwera AzureSQL, który hostuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="54d1f-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="54d1f-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54d1f-122">-Confirm</span></span>
<span data-ttu-id="54d1f-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="54d1f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d1f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d1f-124">-WhatIf</span></span>
<span data-ttu-id="54d1f-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d1f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54d1f-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="54d1f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d1f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d1f-127">CommonParameters</span></span>
<span data-ttu-id="54d1f-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d1f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d1f-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54d1f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d1f-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54d1f-130">INPUTS</span></span>

### <span data-ttu-id="54d1f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="54d1f-131">System.String</span></span>

## <span data-ttu-id="54d1f-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54d1f-132">OUTPUTS</span></span>

### <span data-ttu-id="54d1f-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="54d1f-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="54d1f-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54d1f-134">NOTES</span></span>

## <span data-ttu-id="54d1f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54d1f-135">RELATED LINKS</span></span>
