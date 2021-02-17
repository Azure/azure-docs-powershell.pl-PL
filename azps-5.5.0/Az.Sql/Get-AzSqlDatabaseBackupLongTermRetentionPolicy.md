---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197762"
---
# <span data-ttu-id="ba121-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba121-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="ba121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba121-102">SYNOPSIS</span></span>
<span data-ttu-id="ba121-103">Otrzymuje zasady przechowywania długoterminowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="ba121-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="ba121-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba121-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba121-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba121-105">DESCRIPTION</span></span>
<span data-ttu-id="ba121-106">Polecenie **cmdlet Get-AzSqlDatabaseBackupLongTermRetentionPolicy** pobiera do tej bazy danych zasady przechowywania przez długi czas.</span><span class="sxs-lookup"><span data-stu-id="ba121-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="ba121-107">Zasady są zasobem kopii zapasowej azure używanym do definiowania zasad przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ba121-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="ba121-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba121-108">EXAMPLES</span></span>

### <span data-ttu-id="ba121-109">Przykład 1. Uzyskiwanie bieżącej wersji zasad przechowywania długoterminowych</span><span class="sxs-lookup"><span data-stu-id="ba121-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="ba121-110">To polecenie pobiera bieżącą wersję zasad przechowywania długoterminowego dla bazy danych 01</span><span class="sxs-lookup"><span data-stu-id="ba121-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="ba121-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba121-111">PARAMETERS</span></span>

### <span data-ttu-id="ba121-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba121-112">-DatabaseName</span></span>
<span data-ttu-id="ba121-113">Nazwa bazy danych Azure SQL Database, która ma być używania.</span><span class="sxs-lookup"><span data-stu-id="ba121-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="ba121-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba121-114">-DefaultProfile</span></span>
<span data-ttu-id="ba121-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba121-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba121-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba121-116">-ResourceGroupName</span></span>
<span data-ttu-id="ba121-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba121-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba121-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba121-118">-ServerName</span></span>
<span data-ttu-id="ba121-119">Nazwa serwera Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="ba121-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="ba121-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba121-120">-Confirm</span></span>
<span data-ttu-id="ba121-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba121-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba121-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba121-122">-WhatIf</span></span>
<span data-ttu-id="ba121-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba121-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba121-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ba121-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba121-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba121-125">CommonParameters</span></span>
<span data-ttu-id="ba121-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba121-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba121-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba121-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba121-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba121-128">INPUTS</span></span>

### <span data-ttu-id="ba121-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ba121-129">System.String</span></span>

## <span data-ttu-id="ba121-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba121-130">OUTPUTS</span></span>

### <span data-ttu-id="ba121-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ba121-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="ba121-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba121-132">NOTES</span></span>

## <span data-ttu-id="ba121-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba121-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba121-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ba121-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ba121-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ba121-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ba121-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba121-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ba121-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ba121-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)