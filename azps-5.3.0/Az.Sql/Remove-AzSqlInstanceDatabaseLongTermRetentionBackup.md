---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374549"
---
# <span data-ttu-id="84610-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="84610-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="84610-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84610-102">SYNOPSIS</span></span>
<span data-ttu-id="84610-103">Usuwa kopię zapasową długotrwałego przechowywania.</span><span class="sxs-lookup"><span data-stu-id="84610-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="84610-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84610-104">SYNTAX</span></span>

### <span data-ttu-id="84610-105">RemoveBackupDefault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84610-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84610-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="84610-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84610-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="84610-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84610-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84610-108">DESCRIPTION</span></span>
<span data-ttu-id="84610-109">Polecenie cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** usuwa określoną kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="84610-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="84610-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84610-110">EXAMPLES</span></span>

### <span data-ttu-id="84610-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84610-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="84610-112">Usuwa kopię zapasową z nazwą 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="84610-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="84610-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84610-113">PARAMETERS</span></span>

### <span data-ttu-id="84610-114">-Backupname</span><span class="sxs-lookup"><span data-stu-id="84610-114">-BackupName</span></span>
<span data-ttu-id="84610-115">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="84610-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84610-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="84610-116">-DatabaseName</span></span>
<span data-ttu-id="84610-117">Nazwa zarządzanej bazy danych, z której pochodzi kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="84610-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84610-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84610-118">-DefaultProfile</span></span>
<span data-ttu-id="84610-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84610-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84610-120">-Force</span><span class="sxs-lookup"><span data-stu-id="84610-120">-Force</span></span>
<span data-ttu-id="84610-121">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="84610-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84610-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84610-122">-InputObject</span></span>
<span data-ttu-id="84610-123">Obiekt kopii zapasowej przechowywania długoterminowej bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="84610-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84610-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="84610-124">-InstanceName</span></span>
<span data-ttu-id="84610-125">Nazwa wystąpienia zarządzanego kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="84610-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84610-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="84610-126">-Location</span></span>
<span data-ttu-id="84610-127">Lokalizacja wystąpienia źródłowego zarządzanych kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="84610-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84610-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84610-128">-ResourceGroupName</span></span>
<span data-ttu-id="84610-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84610-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84610-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84610-130">-ResourceId</span></span>
<span data-ttu-id="84610-131">Identyfikator zasobu kopii zapasowej przechowywania długoterminowej bazy danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="84610-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84610-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84610-132">-Confirm</span></span>
<span data-ttu-id="84610-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84610-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84610-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84610-134">-WhatIf</span></span>
<span data-ttu-id="84610-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84610-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84610-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84610-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84610-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84610-137">CommonParameters</span></span>
<span data-ttu-id="84610-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84610-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84610-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84610-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84610-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84610-140">INPUTS</span></span>

### <span data-ttu-id="84610-141">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="84610-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="84610-142">System. String</span><span class="sxs-lookup"><span data-stu-id="84610-142">System.String</span></span>

## <span data-ttu-id="84610-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84610-143">OUTPUTS</span></span>

### <span data-ttu-id="84610-144">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="84610-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="84610-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84610-145">NOTES</span></span>

## <span data-ttu-id="84610-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84610-146">RELATED LINKS</span></span>

[<span data-ttu-id="84610-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="84610-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="84610-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="84610-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="84610-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="84610-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="84610-150">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="84610-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)