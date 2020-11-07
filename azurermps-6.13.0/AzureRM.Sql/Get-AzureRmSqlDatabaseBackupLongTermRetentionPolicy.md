---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717360"
---
# <span data-ttu-id="214bb-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="214bb-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="214bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="214bb-102">SYNOPSIS</span></span>
<span data-ttu-id="214bb-103">Pobiera zasady przechowywania długoterminowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="214bb-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="214bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="214bb-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="214bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="214bb-105">DESCRIPTION</span></span>
<span data-ttu-id="214bb-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** pobiera długoterminowe zasady przechowywania zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="214bb-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="214bb-107">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="214bb-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="214bb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="214bb-108">EXAMPLES</span></span>

### <span data-ttu-id="214bb-109">Przykład 1: uzyskiwanie bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="214bb-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="214bb-110">To polecenie pobiera aktualną wersję zasad przechowywania długoterminowego dla database01</span><span class="sxs-lookup"><span data-stu-id="214bb-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="214bb-111">Przykład 2: uzyskiwanie starszej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="214bb-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="214bb-112">To polecenie pobiera starszą wersję zasad przechowywania długoterminowego dla database01</span><span class="sxs-lookup"><span data-stu-id="214bb-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="214bb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="214bb-113">PARAMETERS</span></span>

### <span data-ttu-id="214bb-114">-Bieżące</span><span class="sxs-lookup"><span data-stu-id="214bb-114">-Current</span></span>
<span data-ttu-id="214bb-115">Jeśli nie podano, polecenie zwróci starsze informacje o starszych zasadach przechowywania.</span><span class="sxs-lookup"><span data-stu-id="214bb-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="214bb-116">W przeciwnym razie polecenie zwróci bieżącą wersję zasad przechowywania długoterminowego.</span><span class="sxs-lookup"><span data-stu-id="214bb-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214bb-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="214bb-117">-DatabaseName</span></span>
<span data-ttu-id="214bb-118">Nazwa bazy danych SQL Azure, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="214bb-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="214bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214bb-119">-DefaultProfile</span></span>
<span data-ttu-id="214bb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="214bb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="214bb-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="214bb-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="214bb-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="214bb-123">-ServerName</span></span>
<span data-ttu-id="214bb-124">Nazwa programu Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="214bb-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="214bb-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="214bb-125">-Confirm</span></span>
<span data-ttu-id="214bb-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214bb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214bb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214bb-127">-WhatIf</span></span>
<span data-ttu-id="214bb-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214bb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214bb-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="214bb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214bb-130">CommonParameters</span></span>
<span data-ttu-id="214bb-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214bb-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214bb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214bb-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="214bb-133">INPUTS</span></span>

### <span data-ttu-id="214bb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="214bb-134">System.String</span></span>

## <span data-ttu-id="214bb-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="214bb-135">OUTPUTS</span></span>

### <span data-ttu-id="214bb-136">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="214bb-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="214bb-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="214bb-137">NOTES</span></span>

## <span data-ttu-id="214bb-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="214bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="214bb-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="214bb-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="214bb-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="214bb-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="214bb-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="214bb-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="214bb-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="214bb-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
