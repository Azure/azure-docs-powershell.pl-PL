---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b8284d4f2ac5b28baffed630e789fc002c2c7d9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015850"
---
# <span data-ttu-id="0ff84-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0ff84-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="0ff84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff84-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff84-103">Polecenie cmdlet **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** ustawia długoterminowe zasady przechowywania zarządzanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0ff84-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="0ff84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ff84-104">SYNTAX</span></span>

### <span data-ttu-id="0ff84-105">WeeklyRetentionRequired (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0ff84-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff84-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="0ff84-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff84-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="0ff84-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff84-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="0ff84-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ff84-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ff84-109">DESCRIPTION</span></span>
<span data-ttu-id="0ff84-110">Polecenie cmdlet **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** ustawia długoterminowe zasady przechowywania dla tej zarządzanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0ff84-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="0ff84-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ff84-111">EXAMPLES</span></span>

### <span data-ttu-id="0ff84-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ff84-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="0ff84-113">Konfiguruje tygodniowe zasady przechowywania długoterminowego bazy danych na jeden tydzień.</span><span class="sxs-lookup"><span data-stu-id="0ff84-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="0ff84-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0ff84-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="0ff84-115">To polecenie usuwa z bazy danych zasady przechowywania długoterminowych.</span><span class="sxs-lookup"><span data-stu-id="0ff84-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="0ff84-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0ff84-116">Example 3</span></span>

<span data-ttu-id="0ff84-117">Polecenie Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet ustawia długoterminowe zasady przechowywania zarządzanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0ff84-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="0ff84-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="0ff84-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="0ff84-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ff84-119">PARAMETERS</span></span>

### <span data-ttu-id="0ff84-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0ff84-120">-DatabaseName</span></span>
<span data-ttu-id="0ff84-121">Nazwa zarządzanej bazy danych Azure do użycia.</span><span class="sxs-lookup"><span data-stu-id="0ff84-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="0ff84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff84-122">-DefaultProfile</span></span>
<span data-ttu-id="0ff84-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff84-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ff84-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0ff84-124">-InstanceName</span></span>
<span data-ttu-id="0ff84-125">Nazwa zarządzanego wystąpienia platformy Azure, do którego należy baza danych.</span><span class="sxs-lookup"><span data-stu-id="0ff84-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="0ff84-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="0ff84-126">-MonthlyRetention</span></span>
<span data-ttu-id="0ff84-127">Miesięczne przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="0ff84-127">The Monthly Retention.</span></span>
<span data-ttu-id="0ff84-128">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.</span><span class="sxs-lookup"><span data-stu-id="0ff84-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="0ff84-129">Minimalna wartość to 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="0ff84-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff84-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="0ff84-130">-RemovePolicy</span></span>
<span data-ttu-id="0ff84-131">Jeśli zostanie to podane, zasady bazy danych zostaną wyczyszone.</span><span class="sxs-lookup"><span data-stu-id="0ff84-131">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff84-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff84-132">-ResourceGroupName</span></span>
<span data-ttu-id="0ff84-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ff84-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="0ff84-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="0ff84-134">-WeeklyRetention</span></span>
<span data-ttu-id="0ff84-135">Tygodniowe przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="0ff84-135">The Weekly Retention.</span></span>
<span data-ttu-id="0ff84-136">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.</span><span class="sxs-lookup"><span data-stu-id="0ff84-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="0ff84-137">Minimalna wartość to 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="0ff84-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff84-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="0ff84-138">-WeekOfYear</span></span>
<span data-ttu-id="0ff84-139">Tydzień roku, od 1 do 52, aby zapisać na przechowywanie co rok.</span><span class="sxs-lookup"><span data-stu-id="0ff84-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff84-140">- YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="0ff84-140">-YearlyRetention</span></span>
<span data-ttu-id="0ff84-141">Przechowywanie co rok.</span><span class="sxs-lookup"><span data-stu-id="0ff84-141">The Yearly Retention.</span></span>
<span data-ttu-id="0ff84-142">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.</span><span class="sxs-lookup"><span data-stu-id="0ff84-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="0ff84-143">Minimalna wartość to 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="0ff84-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff84-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ff84-144">-Confirm</span></span>
<span data-ttu-id="0ff84-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0ff84-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff84-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff84-146">-WhatIf</span></span>
<span data-ttu-id="0ff84-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff84-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff84-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0ff84-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff84-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff84-149">CommonParameters</span></span>
<span data-ttu-id="0ff84-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff84-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff84-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ff84-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff84-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ff84-152">INPUTS</span></span>

### <span data-ttu-id="0ff84-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0ff84-153">System.String</span></span>

### <span data-ttu-id="0ff84-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0ff84-154">System.Int32</span></span>

## <span data-ttu-id="0ff84-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ff84-155">OUTPUTS</span></span>

### <span data-ttu-id="0ff84-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0ff84-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="0ff84-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ff84-157">NOTES</span></span>

## <span data-ttu-id="0ff84-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ff84-158">RELATED LINKS</span></span>

[<span data-ttu-id="0ff84-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0ff84-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="0ff84-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0ff84-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="0ff84-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0ff84-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="0ff84-162">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0ff84-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)