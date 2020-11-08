---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5fe99e867f4646edc55b2ab304f6549628955a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053254"
---
# <span data-ttu-id="45b9a-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="45b9a-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="45b9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="45b9a-103">Pobiera zasady przechowywania długoterminowych zarządzanych baz danych</span><span class="sxs-lookup"><span data-stu-id="45b9a-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="45b9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45b9a-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45b9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="45b9a-106">Polecenie cmdlet **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** pobiera długoterminowe zasady przechowywania zarejestrowane w tej zarządzanej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="45b9a-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="45b9a-107">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="45b9a-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="45b9a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45b9a-108">EXAMPLES</span></span>

### <span data-ttu-id="45b9a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45b9a-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="45b9a-110">Pobiera aktualną wersję zasad przechowywania długoterminowego dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="45b9a-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="45b9a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45b9a-111">PARAMETERS</span></span>

### <span data-ttu-id="45b9a-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45b9a-112">-DatabaseName</span></span>
<span data-ttu-id="45b9a-113">Nazwa zarządzanej bazy danych platformy Azure do użycia.</span><span class="sxs-lookup"><span data-stu-id="45b9a-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="45b9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b9a-114">-DefaultProfile</span></span>
<span data-ttu-id="45b9a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45b9a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="45b9a-116">-InstanceName</span></span>
<span data-ttu-id="45b9a-117">Nazwa wystąpienia zarządzanego na platformie Azure, do której należy baza danych.</span><span class="sxs-lookup"><span data-stu-id="45b9a-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="45b9a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b9a-118">-ResourceGroupName</span></span>
<span data-ttu-id="45b9a-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45b9a-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="45b9a-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45b9a-120">-Confirm</span></span>
<span data-ttu-id="45b9a-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b9a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b9a-122">-WhatIf</span></span>
<span data-ttu-id="45b9a-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b9a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b9a-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45b9a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b9a-125">CommonParameters</span></span>
<span data-ttu-id="45b9a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b9a-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b9a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b9a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b9a-128">INPUTS</span></span>

### <span data-ttu-id="45b9a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="45b9a-129">System.String</span></span>

## <span data-ttu-id="45b9a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45b9a-130">OUTPUTS</span></span>

### <span data-ttu-id="45b9a-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="45b9a-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="45b9a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45b9a-132">NOTES</span></span>

## <span data-ttu-id="45b9a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b9a-133">RELATED LINKS</span></span>

[<span data-ttu-id="45b9a-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="45b9a-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="45b9a-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="45b9a-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="45b9a-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="45b9a-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="45b9a-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="45b9a-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)