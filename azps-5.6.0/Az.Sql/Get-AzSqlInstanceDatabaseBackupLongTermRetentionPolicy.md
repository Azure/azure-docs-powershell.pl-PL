---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 3b1c2865e6e5084f3108409d9afae0979ae635b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999473"
---
# <span data-ttu-id="7719e-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7719e-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="7719e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7719e-102">SYNOPSIS</span></span>
<span data-ttu-id="7719e-103">Pobiera długoterminowe zasady przechowywania zarządzanej bazy danych</span><span class="sxs-lookup"><span data-stu-id="7719e-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="7719e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7719e-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7719e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7719e-105">DESCRIPTION</span></span>
<span data-ttu-id="7719e-106">Polecenie **cmdlet Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** pobiera zasady przechowywania danych długoterminowych zarejestrowane w tej zarządzanej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7719e-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="7719e-107">Zasady są zasobem kopii zapasowej azure używanym do definiowania zasad przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7719e-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="7719e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7719e-108">EXAMPLES</span></span>

### <span data-ttu-id="7719e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7719e-109">Example 1</span></span>
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

<span data-ttu-id="7719e-110">Pobiera bieżącą wersję długoterminowych zasad przechowywania dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="7719e-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="7719e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7719e-111">PARAMETERS</span></span>

### <span data-ttu-id="7719e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7719e-112">-DatabaseName</span></span>
<span data-ttu-id="7719e-113">Nazwa zarządzanej bazy danych Azure do użycia.</span><span class="sxs-lookup"><span data-stu-id="7719e-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="7719e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7719e-114">-DefaultProfile</span></span>
<span data-ttu-id="7719e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7719e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7719e-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7719e-116">-InstanceName</span></span>
<span data-ttu-id="7719e-117">Nazwa zarządzanego wystąpienia platformy Azure, do którego należy baza danych.</span><span class="sxs-lookup"><span data-stu-id="7719e-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="7719e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7719e-118">-ResourceGroupName</span></span>
<span data-ttu-id="7719e-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7719e-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="7719e-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7719e-120">-Confirm</span></span>
<span data-ttu-id="7719e-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7719e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7719e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7719e-122">-WhatIf</span></span>
<span data-ttu-id="7719e-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7719e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7719e-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7719e-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7719e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7719e-125">CommonParameters</span></span>
<span data-ttu-id="7719e-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7719e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7719e-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7719e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7719e-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7719e-128">INPUTS</span></span>

### <span data-ttu-id="7719e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7719e-129">System.String</span></span>

## <span data-ttu-id="7719e-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7719e-130">OUTPUTS</span></span>

### <span data-ttu-id="7719e-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7719e-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="7719e-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7719e-132">NOTES</span></span>

## <span data-ttu-id="7719e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7719e-133">RELATED LINKS</span></span>

[<span data-ttu-id="7719e-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7719e-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7719e-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7719e-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7719e-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7719e-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7719e-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7719e-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)