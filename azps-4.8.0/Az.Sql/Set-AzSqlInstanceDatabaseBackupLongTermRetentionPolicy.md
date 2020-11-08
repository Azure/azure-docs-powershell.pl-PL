---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220258"
---
# <span data-ttu-id="4ce92-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4ce92-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="4ce92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ce92-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce92-103">Polecenie cmdlet **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** określa zasady przechowywania długoterminowych zarządzanych baz danych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="4ce92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ce92-104">SYNTAX</span></span>

### <span data-ttu-id="4ce92-105">WeeklyRetentionRequired (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4ce92-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce92-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce92-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce92-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="4ce92-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce92-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="4ce92-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce92-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4ce92-109">DESCRIPTION</span></span>
<span data-ttu-id="4ce92-110">Polecenie cmdlet **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** ustawia zasady przechowywania terminów długoterminowych dla tej zarządzanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="4ce92-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ce92-111">EXAMPLES</span></span>

### <span data-ttu-id="4ce92-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ce92-112">Example 1</span></span>
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

<span data-ttu-id="4ce92-113">Umożliwia skonfigurowanie tygodniowej zasady przechowywania długoterminowej bazy danych do jednego tygodnia.</span><span class="sxs-lookup"><span data-stu-id="4ce92-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="4ce92-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4ce92-114">Example 2</span></span>
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

<span data-ttu-id="4ce92-115">To polecenie usuwa zasady przechowywania terminów długoterminowych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="4ce92-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4ce92-116">Example 3</span></span>

<span data-ttu-id="4ce92-117">Polecenie cmdlet Set-AzSqlInstanceDatabaseLongTermRetentionBackup określa zasady przechowywania długoterminowych zarządzanych baz danych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="4ce92-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="4ce92-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="4ce92-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ce92-119">PARAMETERS</span></span>

### <span data-ttu-id="4ce92-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ce92-120">-DatabaseName</span></span>
<span data-ttu-id="4ce92-121">Nazwa zarządzanej bazy danych platformy Azure do użycia.</span><span class="sxs-lookup"><span data-stu-id="4ce92-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="4ce92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce92-122">-DefaultProfile</span></span>
<span data-ttu-id="4ce92-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce92-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce92-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4ce92-124">-InstanceName</span></span>
<span data-ttu-id="4ce92-125">Nazwa wystąpienia zarządzanego na platformie Azure, do której należy baza danych.</span><span class="sxs-lookup"><span data-stu-id="4ce92-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="4ce92-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="4ce92-126">-MonthlyRetention</span></span>
<span data-ttu-id="4ce92-127">Miesięczna retencja.</span><span class="sxs-lookup"><span data-stu-id="4ce92-127">The Monthly Retention.</span></span>
<span data-ttu-id="4ce92-128">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="4ce92-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="4ce92-129">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="4ce92-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="4ce92-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce92-130">-RemovePolicy</span></span>
<span data-ttu-id="4ce92-131">Jeśli ta zasada jest podana, zasady dotyczące bazy danych zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="4ce92-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="4ce92-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce92-132">-ResourceGroupName</span></span>
<span data-ttu-id="4ce92-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ce92-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ce92-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="4ce92-134">-WeeklyRetention</span></span>
<span data-ttu-id="4ce92-135">Tygodniowe zatrzymanie.</span><span class="sxs-lookup"><span data-stu-id="4ce92-135">The Weekly Retention.</span></span>
<span data-ttu-id="4ce92-136">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="4ce92-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="4ce92-137">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="4ce92-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="4ce92-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="4ce92-138">-WeekOfYear</span></span>
<span data-ttu-id="4ce92-139">Tydzień roku, od 1 do 52, aby zaoszczędzić na rocznych zatrzymań.</span><span class="sxs-lookup"><span data-stu-id="4ce92-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="4ce92-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="4ce92-140">-YearlyRetention</span></span>
<span data-ttu-id="4ce92-141">Roczny okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="4ce92-141">The Yearly Retention.</span></span>
<span data-ttu-id="4ce92-142">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="4ce92-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="4ce92-143">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="4ce92-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="4ce92-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ce92-144">-Confirm</span></span>
<span data-ttu-id="4ce92-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce92-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce92-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce92-146">-WhatIf</span></span>
<span data-ttu-id="4ce92-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce92-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce92-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ce92-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce92-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce92-149">CommonParameters</span></span>
<span data-ttu-id="4ce92-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce92-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce92-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ce92-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce92-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ce92-152">INPUTS</span></span>

### <span data-ttu-id="4ce92-153">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce92-153">System.String</span></span>

### <span data-ttu-id="4ce92-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4ce92-154">System.Int32</span></span>

## <span data-ttu-id="4ce92-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ce92-155">OUTPUTS</span></span>

### <span data-ttu-id="4ce92-156">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4ce92-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="4ce92-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ce92-157">NOTES</span></span>

## <span data-ttu-id="4ce92-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ce92-158">RELATED LINKS</span></span>

[<span data-ttu-id="4ce92-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4ce92-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4ce92-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4ce92-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4ce92-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4ce92-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4ce92-162">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4ce92-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)