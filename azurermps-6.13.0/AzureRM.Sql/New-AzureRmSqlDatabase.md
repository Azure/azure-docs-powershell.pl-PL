---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718575"
---
# <span data-ttu-id="a966f-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a966f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a966f-102">SYNOPSIS</span></span>
<span data-ttu-id="a966f-103">Tworzy bazę danych lub elastyczną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a966f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a966f-104">SYNTAX</span></span>

### <span data-ttu-id="a966f-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a966f-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a966f-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a966f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a966f-107">DESCRIPTION</span></span>
<span data-ttu-id="a966f-108">Polecenie cmdlet **New-AzureRmSqlDatabase** tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a966f-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="a966f-109">Możesz również utworzyć elastyczną bazę danych, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="a966f-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="a966f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a966f-110">EXAMPLES</span></span>

### <span data-ttu-id="a966f-111">Przykład 1: Tworzenie bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="a966f-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="a966f-112">To polecenie tworzy bazę danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="a966f-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="a966f-113">Przykład 2: Tworzenie Elastic Database na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="a966f-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="a966f-114">To polecenie tworzy bazę danych o nazwie Database02 w puli elastycznej o nazwie ElasticPool01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="a966f-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="a966f-115">Przykład 3: Tworzenie bazy danych programu vCore na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="a966f-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="a966f-116">To polecenie tworzy bazę danych vCore o nazwie Database03 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="a966f-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="a966f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a966f-117">PARAMETERS</span></span>

### <span data-ttu-id="a966f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a966f-118">-AsJob</span></span>
<span data-ttu-id="a966f-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a966f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a966f-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="a966f-120">-CatalogCollation</span></span>
<span data-ttu-id="a966f-121">Określa nazwę sortowania wykazu bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a966f-121">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="a966f-122">-CollationName</span></span>
<span data-ttu-id="a966f-123">Określa nazwę sortowania bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a966f-123">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a966f-124">-ComputeGeneration</span></span>
<span data-ttu-id="a966f-125">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="a966f-125">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a966f-126">-DatabaseName</span></span>
<span data-ttu-id="a966f-127">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-127">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a966f-128">-DefaultProfile</span></span>
<span data-ttu-id="a966f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a966f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a966f-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="a966f-130">-Edition</span></span>
<span data-ttu-id="a966f-131">Określa wydanie, które ma zostać przypisane do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="a966f-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a966f-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a966f-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a966f-133">None</span></span>
- <span data-ttu-id="a966f-134">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="a966f-134">Basic</span></span>
- <span data-ttu-id="a966f-135">Standard</span><span class="sxs-lookup"><span data-stu-id="a966f-135">Standard</span></span>
- <span data-ttu-id="a966f-136">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="a966f-136">Premium</span></span>
- <span data-ttu-id="a966f-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="a966f-137">DataWarehouse</span></span>
- <span data-ttu-id="a966f-138">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="a966f-138">Free</span></span>
- <span data-ttu-id="a966f-139">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="a966f-139">Stretch</span></span>
- <span data-ttu-id="a966f-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="a966f-140">GeneralPurpose</span></span>
- <span data-ttu-id="a966f-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="a966f-141">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a966f-142">-ElasticPoolName</span></span>
<span data-ttu-id="a966f-143">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-143">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a966f-144">-LicenseType</span></span>
<span data-ttu-id="a966f-145">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a966f-145">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="a966f-146">-MaxSizeBytes</span></span>
<span data-ttu-id="a966f-147">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="a966f-147">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="a966f-148">-ReadScale</span></span>
<span data-ttu-id="a966f-149">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="a966f-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a966f-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="a966f-151">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-151">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a966f-152">-ResourceGroupName</span></span>
<span data-ttu-id="a966f-153">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="a966f-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a966f-154">-Samplename</span><span class="sxs-lookup"><span data-stu-id="a966f-154">-SampleName</span></span>
<span data-ttu-id="a966f-155">Nazwa przykładowego schematu, który ma zostać zastosowany podczas tworzenia tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-155">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-156">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a966f-156">-ServerName</span></span>
<span data-ttu-id="a966f-157">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a966f-158">-Tagi</span><span class="sxs-lookup"><span data-stu-id="a966f-158">-Tags</span></span>
<span data-ttu-id="a966f-159">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z nową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="a966f-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="a966f-160">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a966f-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="a966f-161">-VCore</span></span>
<span data-ttu-id="a966f-162">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a966f-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a966f-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a966f-163">-ZoneRedundant</span></span>
<span data-ttu-id="a966f-164">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a966f-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="a966f-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a966f-165">-Confirm</span></span>
<span data-ttu-id="a966f-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a966f-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a966f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a966f-167">-WhatIf</span></span>
<span data-ttu-id="a966f-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a966f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a966f-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a966f-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a966f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a966f-170">CommonParameters</span></span>
<span data-ttu-id="a966f-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a966f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a966f-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a966f-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a966f-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a966f-173">INPUTS</span></span>

### <span data-ttu-id="a966f-174">System. String</span><span class="sxs-lookup"><span data-stu-id="a966f-174">System.String</span></span>

## <span data-ttu-id="a966f-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a966f-175">OUTPUTS</span></span>

### <span data-ttu-id="a966f-176">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a966f-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a966f-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a966f-177">NOTES</span></span>

## <span data-ttu-id="a966f-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a966f-178">RELATED LINKS</span></span>

[<span data-ttu-id="a966f-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a966f-180">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a966f-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a966f-181">Nowe — AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="a966f-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="a966f-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a966f-183">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="a966f-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a966f-185">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a966f-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="a966f-186">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a966f-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

