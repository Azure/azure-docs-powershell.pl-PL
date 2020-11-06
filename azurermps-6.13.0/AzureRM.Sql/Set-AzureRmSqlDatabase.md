---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 283b12ca63f92086369f273b1f04d5e3f0cd1716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527789"
---
# <span data-ttu-id="36db2-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="36db2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36db2-102">SYNOPSIS</span></span>
<span data-ttu-id="36db2-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="36db2-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36db2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36db2-104">SYNTAX</span></span>

### <span data-ttu-id="36db2-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="36db2-105">Update (Default)</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36db2-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-106">VcoreBasedDatabase</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36db2-107">Nazwy</span><span class="sxs-lookup"><span data-stu-id="36db2-107">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36db2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="36db2-108">DESCRIPTION</span></span>
<span data-ttu-id="36db2-109">Polecenie cmdlet **Set-AzureRmSqlDatabase** ustawia właściwości bazy danych w bazie danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="36db2-109">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="36db2-110">To polecenie cmdlet może zmodyfikować warstwę usług ( *wersja* ), poziom wydajności ( *RequestedServiceObjectiveName* ) i maksymalny rozmiar magazynu ( *MaxSizeBytes* ) bazy danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="36db2-111">Ponadto można określić parametr *ElasticPoolName* , aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="36db2-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="36db2-112">Jeśli baza danych znajduje się już w puli elastycznej, można użyć parametru *RequestedServiceObjectiveName* , aby przenieść bazę danych poza elastyczną pulę i na poziom wydajności dla pojedynczych baz danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="36db2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36db2-113">EXAMPLES</span></span>

### <span data-ttu-id="36db2-114">Przykład 1: aktualizowanie bazy danych do standardowej S2 bazy danych</span><span class="sxs-lookup"><span data-stu-id="36db2-114">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="36db2-115">To polecenie aktualizuje bazę danych o nazwie Database01 do standardowej S2 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="36db2-115">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="36db2-116">Przykład 2: Dodawanie bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="36db2-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="36db2-117">To polecenie dodaje bazę danych o nazwie Database01 do puli elastycznej o nazwie ElasticPool01 hostowanej na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="36db2-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="36db2-118">Przykład 3: modyfikowanie maksymalnego rozmiaru przestrzeni dyskowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="36db2-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="36db2-119">To polecenie aktualizuje bazę danych o nazwie Database01, aby ustawić jej maksymalny rozmiar na 1 TB.</span><span class="sxs-lookup"><span data-stu-id="36db2-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="36db2-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36db2-120">PARAMETERS</span></span>

### <span data-ttu-id="36db2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36db2-121">-AsJob</span></span>
<span data-ttu-id="36db2-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="36db2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36db2-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="36db2-123">-ComputeGeneration</span></span>
<span data-ttu-id="36db2-124">Generowanie obliczeń do przypisania.</span><span class="sxs-lookup"><span data-stu-id="36db2-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36db2-125">-DatabaseName</span></span>
<span data-ttu-id="36db2-126">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-126">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36db2-127">-DefaultProfile</span></span>
<span data-ttu-id="36db2-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="36db2-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36db2-129">-Edition</span><span class="sxs-lookup"><span data-stu-id="36db2-129">-Edition</span></span>
<span data-ttu-id="36db2-130">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="36db2-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="36db2-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36db2-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="36db2-132">None</span></span>
- <span data-ttu-id="36db2-133">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="36db2-133">Basic</span></span>
- <span data-ttu-id="36db2-134">Standard</span><span class="sxs-lookup"><span data-stu-id="36db2-134">Standard</span></span>
- <span data-ttu-id="36db2-135">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="36db2-135">Premium</span></span>
- <span data-ttu-id="36db2-136">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="36db2-136">DataWarehouse</span></span>
- <span data-ttu-id="36db2-137">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="36db2-137">Free</span></span>
- <span data-ttu-id="36db2-138">Rozciąga</span><span class="sxs-lookup"><span data-stu-id="36db2-138">Stretch</span></span>
- <span data-ttu-id="36db2-139">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="36db2-139">GeneralPurpose</span></span>
- <span data-ttu-id="36db2-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="36db2-140">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="36db2-141">-ElasticPoolName</span></span>
<span data-ttu-id="36db2-142">Określa nazwę puli elastycznej, w której ma zostać przeniesiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-142">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="36db2-143">-LicenseType</span></span>
<span data-ttu-id="36db2-144">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="36db2-144">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-145">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="36db2-145">-MaxSizeBytes</span></span>
<span data-ttu-id="36db2-146">Maksymalny rozmiar bazy danych SQL Azure w bajtach.</span><span class="sxs-lookup"><span data-stu-id="36db2-146">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-147">-NewName</span><span class="sxs-lookup"><span data-stu-id="36db2-147">-NewName</span></span>
<span data-ttu-id="36db2-148">Nowa nazwa, do której ma zostać zmieniona baza danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-148">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-149">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="36db2-149">-ReadScale</span></span>
<span data-ttu-id="36db2-150">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="36db2-150">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-151">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="36db2-151">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="36db2-152">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-152">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="36db2-153">Aby uzyskać informacje na temat celów usługi, zobacz [warstwy usług Azure SQL Database i poziomy wydajności](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="36db2-153">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36db2-154">-ResourceGroupName</span></span>
<span data-ttu-id="36db2-155">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="36db2-155">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="36db2-156">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="36db2-156">-ServerName</span></span>
<span data-ttu-id="36db2-157">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="36db2-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="36db2-158">-Tagi</span><span class="sxs-lookup"><span data-stu-id="36db2-158">-Tags</span></span>
<span data-ttu-id="36db2-159">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="36db2-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36db2-160">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="36db2-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="36db2-161">-VCore</span></span>
<span data-ttu-id="36db2-162">Numer vCore bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="36db2-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="36db2-163">-ZoneRedundant</span></span>
<span data-ttu-id="36db2-164">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="36db2-164">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36db2-165">-Confirm</span></span>
<span data-ttu-id="36db2-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36db2-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36db2-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36db2-167">-WhatIf</span></span>
<span data-ttu-id="36db2-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36db2-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36db2-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36db2-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36db2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36db2-170">CommonParameters</span></span>
<span data-ttu-id="36db2-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36db2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36db2-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36db2-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36db2-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36db2-173">INPUTS</span></span>

### <span data-ttu-id="36db2-174">System. String</span><span class="sxs-lookup"><span data-stu-id="36db2-174">System.String</span></span>

## <span data-ttu-id="36db2-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36db2-175">OUTPUTS</span></span>

### <span data-ttu-id="36db2-176">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="36db2-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="36db2-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36db2-177">NOTES</span></span>

## <span data-ttu-id="36db2-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36db2-178">RELATED LINKS</span></span>

[<span data-ttu-id="36db2-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="36db2-180">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-180">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="36db2-181">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-181">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="36db2-182">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-182">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="36db2-183">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36db2-183">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="36db2-184">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="36db2-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
