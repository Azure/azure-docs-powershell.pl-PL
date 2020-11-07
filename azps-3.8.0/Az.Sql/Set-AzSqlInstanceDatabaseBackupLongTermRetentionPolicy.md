---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895745"
---
# <span data-ttu-id="b7907-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7907-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b7907-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7907-102">SYNOPSIS</span></span>
<span data-ttu-id="b7907-103">Polecenie cmdlet **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** określa zasady przechowywania długoterminowych zarządzanych baz danych.</span><span class="sxs-lookup"><span data-stu-id="b7907-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="b7907-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7907-104">SYNTAX</span></span>

### <span data-ttu-id="b7907-105">WeeklyRetentionRequired (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7907-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7907-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b7907-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7907-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b7907-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7907-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b7907-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7907-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b7907-109">DESCRIPTION</span></span>
<span data-ttu-id="b7907-110">Polecenie cmdlet **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** ustawia zasady przechowywania terminów długoterminowych dla tej zarządzanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b7907-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="b7907-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7907-111">EXAMPLES</span></span>

### <span data-ttu-id="b7907-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7907-112">Example 1</span></span>
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

<span data-ttu-id="b7907-113">Umożliwia skonfigurowanie tygodniowej zasady przechowywania długoterminowej bazy danych do jednego tygodnia.</span><span class="sxs-lookup"><span data-stu-id="b7907-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="b7907-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b7907-114">Example 2</span></span>
```
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


<span data-ttu-id="b7907-115">To polecenie usuwa zasady przechowywania terminów długoterminowych z bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b7907-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="b7907-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7907-116">PARAMETERS</span></span>

### <span data-ttu-id="b7907-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7907-117">-DatabaseName</span></span>
<span data-ttu-id="b7907-118">Nazwa zarządzanej bazy danych platformy Azure do użycia.</span><span class="sxs-lookup"><span data-stu-id="b7907-118">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="b7907-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7907-119">-DefaultProfile</span></span>
<span data-ttu-id="b7907-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7907-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7907-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b7907-121">-InstanceName</span></span>
<span data-ttu-id="b7907-122">Nazwa wystąpienia zarządzanego na platformie Azure, do której należy baza danych.</span><span class="sxs-lookup"><span data-stu-id="b7907-122">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="b7907-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="b7907-123">-MonthlyRetention</span></span>
<span data-ttu-id="b7907-124">Miesięczna retencja.</span><span class="sxs-lookup"><span data-stu-id="b7907-124">The Monthly Retention.</span></span>
<span data-ttu-id="b7907-125">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="b7907-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b7907-126">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="b7907-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7907-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b7907-127">-RemovePolicy</span></span>
<span data-ttu-id="b7907-128">Jeśli ta zasada jest podana, zasady dotyczące bazy danych zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="b7907-128">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7907-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7907-129">-ResourceGroupName</span></span>
<span data-ttu-id="b7907-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7907-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7907-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="b7907-131">-WeeklyRetention</span></span>
<span data-ttu-id="b7907-132">Tygodniowe zatrzymanie.</span><span class="sxs-lookup"><span data-stu-id="b7907-132">The Weekly Retention.</span></span>
<span data-ttu-id="b7907-133">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="b7907-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b7907-134">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="b7907-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7907-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="b7907-135">-WeekOfYear</span></span>
<span data-ttu-id="b7907-136">Tydzień roku, od 1 do 52, aby zaoszczędzić na rocznych zatrzymań.</span><span class="sxs-lookup"><span data-stu-id="b7907-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7907-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="b7907-137">-YearlyRetention</span></span>
<span data-ttu-id="b7907-138">Roczny okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b7907-138">The Yearly Retention.</span></span>
<span data-ttu-id="b7907-139">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="b7907-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b7907-140">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="b7907-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7907-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7907-141">-Confirm</span></span>
<span data-ttu-id="b7907-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7907-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7907-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7907-143">-WhatIf</span></span>
<span data-ttu-id="b7907-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7907-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7907-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7907-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7907-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7907-146">CommonParameters</span></span>
<span data-ttu-id="b7907-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7907-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7907-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7907-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7907-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7907-149">INPUTS</span></span>

### <span data-ttu-id="b7907-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b7907-150">System.String</span></span>

### <span data-ttu-id="b7907-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b7907-151">System.Int32</span></span>

## <span data-ttu-id="b7907-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7907-152">OUTPUTS</span></span>

### <span data-ttu-id="b7907-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b7907-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b7907-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7907-154">NOTES</span></span>

## <span data-ttu-id="b7907-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7907-155">RELATED LINKS</span></span>

[<span data-ttu-id="b7907-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7907-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b7907-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b7907-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b7907-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b7907-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b7907-159">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b7907-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)