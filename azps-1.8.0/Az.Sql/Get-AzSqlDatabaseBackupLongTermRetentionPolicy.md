---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: ce7bf498dc005f6cae8bfff28f0e470cacff71ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708009"
---
# <span data-ttu-id="7b400-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b400-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="7b400-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b400-102">SYNOPSIS</span></span>
<span data-ttu-id="7b400-103">Pobiera zasady przechowywania długoterminowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="7b400-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="7b400-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b400-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b400-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b400-105">DESCRIPTION</span></span>
<span data-ttu-id="7b400-106">Polecenie cmdlet **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** pobiera długoterminowe zasady przechowywania zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7b400-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="7b400-107">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7b400-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="7b400-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b400-108">EXAMPLES</span></span>

### <span data-ttu-id="7b400-109">Przykład 1: uzyskiwanie bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="7b400-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="7b400-110">To polecenie pobiera aktualną wersję zasad przechowywania długoterminowego dla database01</span><span class="sxs-lookup"><span data-stu-id="7b400-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="7b400-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b400-111">PARAMETERS</span></span>

### <span data-ttu-id="7b400-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7b400-112">-DatabaseName</span></span>
<span data-ttu-id="7b400-113">Nazwa bazy danych SQL Azure, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="7b400-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="7b400-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b400-114">-DefaultProfile</span></span>
<span data-ttu-id="7b400-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b400-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b400-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b400-116">-ResourceGroupName</span></span>
<span data-ttu-id="7b400-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b400-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b400-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7b400-118">-ServerName</span></span>
<span data-ttu-id="7b400-119">Nazwa programu Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="7b400-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="7b400-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b400-120">-Confirm</span></span>
<span data-ttu-id="7b400-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b400-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b400-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b400-122">-WhatIf</span></span>
<span data-ttu-id="7b400-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b400-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b400-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b400-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b400-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b400-125">CommonParameters</span></span>
<span data-ttu-id="7b400-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b400-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b400-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b400-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b400-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b400-128">INPUTS</span></span>

### <span data-ttu-id="7b400-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b400-129">System.String</span></span>

## <span data-ttu-id="7b400-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b400-130">OUTPUTS</span></span>

### <span data-ttu-id="7b400-131">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7b400-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="7b400-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b400-132">NOTES</span></span>

## <span data-ttu-id="7b400-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b400-133">RELATED LINKS</span></span>

[<span data-ttu-id="7b400-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7b400-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7b400-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7b400-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7b400-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b400-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7b400-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7b400-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)