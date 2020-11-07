---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707874"
---
# <span data-ttu-id="640c1-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="640c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="640c1-102">SYNOPSIS</span></span>
<span data-ttu-id="640c1-103">Tworzy bazę danych lub elastyczną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="640c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="640c1-104">SYNTAX</span></span>

### <span data-ttu-id="640c1-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="640c1-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="640c1-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640c1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="640c1-107">DESCRIPTION</span></span>
<span data-ttu-id="640c1-108">Polecenie cmdlet **New-AzSqlDatabase** tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="640c1-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="640c1-109">Możesz również utworzyć elastyczną bazę danych, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="640c1-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="640c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="640c1-110">EXAMPLES</span></span>

### <span data-ttu-id="640c1-111">Przykład 1: Tworzenie bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="640c1-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="640c1-112">To polecenie tworzy bazę danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="640c1-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="640c1-113">Przykład 2: Tworzenie Elastic Database na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="640c1-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="640c1-114">To polecenie tworzy bazę danych o nazwie Database02 w puli elastycznej o nazwie ElasticPool01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="640c1-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="640c1-115">Przykład 3: Tworzenie bazy danych programu vCore na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="640c1-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="640c1-116">To polecenie tworzy bazę danych vCore o nazwie Database03 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="640c1-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="640c1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="640c1-117">PARAMETERS</span></span>

### <span data-ttu-id="640c1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="640c1-118">-AsJob</span></span>
<span data-ttu-id="640c1-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="640c1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="640c1-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="640c1-120">-CatalogCollation</span></span>
<span data-ttu-id="640c1-121">Określa nazwę sortowania wykazu bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="640c1-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="640c1-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="640c1-122">-CollationName</span></span>
<span data-ttu-id="640c1-123">Określa nazwę sortowania bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="640c1-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="640c1-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="640c1-124">-ComputeGeneration</span></span>
<span data-ttu-id="640c1-125">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="640c1-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="640c1-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="640c1-126">-DatabaseName</span></span>
<span data-ttu-id="640c1-127">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="640c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640c1-128">-DefaultProfile</span></span>
<span data-ttu-id="640c1-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="640c1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="640c1-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="640c1-130">-Edition</span></span>
<span data-ttu-id="640c1-131">Określa wydanie, które ma zostać przypisane do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="640c1-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="640c1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="640c1-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="640c1-133">None</span></span>
- <span data-ttu-id="640c1-134">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="640c1-134">Basic</span></span>
- <span data-ttu-id="640c1-135">Standard</span><span class="sxs-lookup"><span data-stu-id="640c1-135">Standard</span></span>
- <span data-ttu-id="640c1-136">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="640c1-136">Premium</span></span>
- <span data-ttu-id="640c1-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="640c1-137">DataWarehouse</span></span>
- <span data-ttu-id="640c1-138">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="640c1-138">Free</span></span>
- <span data-ttu-id="640c1-139">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="640c1-139">Stretch</span></span>
- <span data-ttu-id="640c1-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="640c1-140">GeneralPurpose</span></span>
- <span data-ttu-id="640c1-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="640c1-141">BusinessCritical</span></span>

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

### <span data-ttu-id="640c1-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="640c1-142">-ElasticPoolName</span></span>
<span data-ttu-id="640c1-143">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="640c1-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="640c1-144">-LicenseType</span></span>
<span data-ttu-id="640c1-145">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="640c1-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="640c1-146">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="640c1-146">Possible values are:</span></span>
- <span data-ttu-id="640c1-147">BasePrice — ceny usługi Azure hybrydowego (AHB) mają rabaty cenowe dla istniejących właścicieli licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="640c1-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="640c1-148">Cena bazy danych zostanie obniżona o istniejące właściciele licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="640c1-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="640c1-149">LicenseIncluded — ceny rabatu usługi Azure hybrydowego (AHB) dla istniejących właścicieli licencji programu SQL Server nie są stosowane.</span><span class="sxs-lookup"><span data-stu-id="640c1-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="640c1-150">Cena bazy danych będzie obejmować nowe koszty licencji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="640c1-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="640c1-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="640c1-151">-MaxSizeBytes</span></span>
<span data-ttu-id="640c1-152">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="640c1-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="640c1-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="640c1-153">-ReadScale</span></span>
<span data-ttu-id="640c1-154">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="640c1-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="640c1-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="640c1-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="640c1-156">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="640c1-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640c1-157">-ResourceGroupName</span></span>
<span data-ttu-id="640c1-158">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="640c1-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="640c1-159">-Samplename</span><span class="sxs-lookup"><span data-stu-id="640c1-159">-SampleName</span></span>
<span data-ttu-id="640c1-160">Nazwa przykładowego schematu, który ma zostać zastosowany podczas tworzenia tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="640c1-161">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="640c1-161">-ServerName</span></span>
<span data-ttu-id="640c1-162">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="640c1-163">-Tagi</span><span class="sxs-lookup"><span data-stu-id="640c1-163">-Tags</span></span>
<span data-ttu-id="640c1-164">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z nową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="640c1-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="640c1-165">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="640c1-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="640c1-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="640c1-166">-VCore</span></span>
<span data-ttu-id="640c1-167">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="640c1-167">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="640c1-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="640c1-168">-ZoneRedundant</span></span>
<span data-ttu-id="640c1-169">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="640c1-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="640c1-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="640c1-170">-Confirm</span></span>
<span data-ttu-id="640c1-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="640c1-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="640c1-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640c1-172">-WhatIf</span></span>
<span data-ttu-id="640c1-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="640c1-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="640c1-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="640c1-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="640c1-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640c1-175">CommonParameters</span></span>
<span data-ttu-id="640c1-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640c1-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640c1-177">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="640c1-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640c1-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="640c1-178">INPUTS</span></span>

### <span data-ttu-id="640c1-179">System. String</span><span class="sxs-lookup"><span data-stu-id="640c1-179">System.String</span></span>

## <span data-ttu-id="640c1-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="640c1-180">OUTPUTS</span></span>

### <span data-ttu-id="640c1-181">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="640c1-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="640c1-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="640c1-182">NOTES</span></span>

## <span data-ttu-id="640c1-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="640c1-183">RELATED LINKS</span></span>

[<span data-ttu-id="640c1-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="640c1-185">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="640c1-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="640c1-186">Nowe — AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="640c1-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="640c1-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="640c1-188">Życiorys — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="640c1-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="640c1-190">Suspend — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="640c1-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="640c1-191">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="640c1-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

