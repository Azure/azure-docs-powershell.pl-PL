---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549523"
---
# <span data-ttu-id="0b620-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b620-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="0b620-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b620-102">SYNOPSIS</span></span>
<span data-ttu-id="0b620-103">Tworzy bazę danych lub elastyczną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b620-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b620-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b620-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b620-105">DESCRIPTION</span></span>
<span data-ttu-id="0b620-106">Polecenie cmdlet **New-AzureRmSqlDatabase** tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0b620-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="0b620-107">Możesz również utworzyć elastyczną bazę danych, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="0b620-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="0b620-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b620-108">EXAMPLES</span></span>

### <span data-ttu-id="0b620-109">Przykład 1: Tworzenie bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="0b620-109">Example 1: Create a database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="0b620-110">To polecenie tworzy bazę danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="0b620-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="0b620-111">Przykład 2: Tworzenie Elastic Database na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="0b620-111">Example 2: Create an elastic database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="0b620-112">To polecenie tworzy bazę danych o nazwie Database01 w puli elastycznej o nazwie ElasticPool01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="0b620-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="0b620-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b620-113">PARAMETERS</span></span>

### <span data-ttu-id="0b620-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b620-114">-AsJob</span></span>
<span data-ttu-id="0b620-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0b620-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="0b620-116">-CatalogCollation</span></span>
<span data-ttu-id="0b620-117">Określa nazwę sortowania wykazu bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0b620-117">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="0b620-118">-CollationName</span></span>
<span data-ttu-id="0b620-119">Określa nazwę sortowania bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0b620-119">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b620-120">-DatabaseName</span></span>
<span data-ttu-id="0b620-121">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b620-122">-DefaultProfile</span></span>
<span data-ttu-id="0b620-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0b620-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-124">-Edition</span><span class="sxs-lookup"><span data-stu-id="0b620-124">-Edition</span></span>
<span data-ttu-id="0b620-125">Określa wydanie, które ma zostać przypisane do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="0b620-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b620-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b620-127">Domyślne</span><span class="sxs-lookup"><span data-stu-id="0b620-127">Default</span></span>
- <span data-ttu-id="0b620-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0b620-128">None</span></span>
- <span data-ttu-id="0b620-129">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="0b620-129">Premium</span></span>
- <span data-ttu-id="0b620-130">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="0b620-130">Basic</span></span>
- <span data-ttu-id="0b620-131">Standard</span><span class="sxs-lookup"><span data-stu-id="0b620-131">Standard</span></span>
- <span data-ttu-id="0b620-132">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0b620-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0b620-133">-ElasticPoolName</span></span>
<span data-ttu-id="0b620-134">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-134">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="0b620-135">-MaxSizeBytes</span></span>
<span data-ttu-id="0b620-136">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="0b620-136">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="0b620-137">-ReadScale</span></span>
<span data-ttu-id="0b620-138">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="0b620-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0b620-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="0b620-140">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-140">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b620-141">-ResourceGroupName</span></span>
<span data-ttu-id="0b620-142">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="0b620-142">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0b620-143">-Samplename</span><span class="sxs-lookup"><span data-stu-id="0b620-143">-SampleName</span></span>
<span data-ttu-id="0b620-144">Nazwa przykładowego schematu, który ma zostać zastosowany podczas tworzenia tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-145">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0b620-145">-ServerName</span></span>
<span data-ttu-id="0b620-146">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-146">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0b620-147">-Tagi</span><span class="sxs-lookup"><span data-stu-id="0b620-147">-Tags</span></span>
<span data-ttu-id="0b620-148">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z nową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="0b620-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="0b620-149">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0b620-149">For example:</span></span>

<span data-ttu-id="0b620-150">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0b620-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0b620-151">-ZoneRedundant</span></span>
<span data-ttu-id="0b620-152">Nadmiarowość strefy do skojarzenia z bazą danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0b620-152">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b620-153">-Confirm</span></span>
<span data-ttu-id="0b620-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b620-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b620-155">-WhatIf</span></span>
<span data-ttu-id="0b620-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b620-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b620-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b620-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b620-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b620-158">CommonParameters</span></span>
<span data-ttu-id="0b620-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b620-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b620-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b620-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b620-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b620-161">INPUTS</span></span>

### <span data-ttu-id="0b620-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0b620-162">None</span></span>
<span data-ttu-id="0b620-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0b620-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b620-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b620-164">OUTPUTS</span></span>

### <span data-ttu-id="0b620-165">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0b620-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0b620-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b620-166">NOTES</span></span>

## <span data-ttu-id="0b620-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b620-167">RELATED LINKS</span></span>

[<span data-ttu-id="0b620-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b620-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="0b620-169">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b620-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0b620-170">Nowe — AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="0b620-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="0b620-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b620-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="0b620-172">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b620-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="0b620-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b620-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="0b620-174">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b620-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="0b620-175">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0b620-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
