---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527221"
---
# <span data-ttu-id="241db-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="241db-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="241db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="241db-102">SYNOPSIS</span></span>
<span data-ttu-id="241db-103">Tworzy bazę danych lub elastyczną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="241db-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="241db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="241db-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="241db-105">DESCRIPTION</span></span>
<span data-ttu-id="241db-106">Polecenie cmdlet **New-AzureRmSqlDatabase** tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="241db-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="241db-107">Możesz również utworzyć elastyczną bazę danych, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="241db-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="241db-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="241db-108">EXAMPLES</span></span>

### <span data-ttu-id="241db-109">Przykład 1: Tworzenie bazy danych na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="241db-109">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="241db-110">To polecenie tworzy bazę danych o nazwie Database01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="241db-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="241db-111">Przykład 2: Tworzenie Elastic Database na określonym serwerze</span><span class="sxs-lookup"><span data-stu-id="241db-111">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="241db-112">To polecenie tworzy bazę danych o nazwie Database01 w puli elastycznej o nazwie ElasticPool01 na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="241db-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="241db-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="241db-113">PARAMETERS</span></span>

### <span data-ttu-id="241db-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="241db-114">-CatalogCollation</span></span>
<span data-ttu-id="241db-115">Określa nazwę sortowania wykazu bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="241db-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="241db-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="241db-116">-CollationName</span></span>
<span data-ttu-id="241db-117">Określa nazwę sortowania bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="241db-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="241db-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="241db-118">-DatabaseName</span></span>
<span data-ttu-id="241db-119">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="241db-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="241db-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="241db-120">-Edition</span></span>
<span data-ttu-id="241db-121">Określa wydanie, które ma zostać przypisane do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="241db-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="241db-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="241db-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="241db-123">Domyślne</span><span class="sxs-lookup"><span data-stu-id="241db-123">Default</span></span>
- <span data-ttu-id="241db-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="241db-124">None</span></span>
- <span data-ttu-id="241db-125">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="241db-125">Premium</span></span>
- <span data-ttu-id="241db-126">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="241db-126">Basic</span></span>
- <span data-ttu-id="241db-127">Standard</span><span class="sxs-lookup"><span data-stu-id="241db-127">Standard</span></span>
- <span data-ttu-id="241db-128">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="241db-128">DataWarehouse</span></span>
- <span data-ttu-id="241db-129">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="241db-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241db-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="241db-130">-ElasticPoolName</span></span>
<span data-ttu-id="241db-131">Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych.</span><span class="sxs-lookup"><span data-stu-id="241db-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="241db-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="241db-132">-MaxSizeBytes</span></span>
<span data-ttu-id="241db-133">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="241db-133">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="241db-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="241db-134">-ReadScale</span></span>
<span data-ttu-id="241db-135">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="241db-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="241db-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="241db-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="241db-137">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="241db-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="241db-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241db-138">-ResourceGroupName</span></span>
<span data-ttu-id="241db-139">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="241db-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="241db-140">-Samplename</span><span class="sxs-lookup"><span data-stu-id="241db-140">-SampleName</span></span>
<span data-ttu-id="241db-141">Nazwa przykładowego schematu, który ma zostać zastosowany podczas tworzenia tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="241db-141">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="241db-142">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="241db-142">-ServerName</span></span>
<span data-ttu-id="241db-143">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="241db-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="241db-144">-Tagi</span><span class="sxs-lookup"><span data-stu-id="241db-144">-Tags</span></span>
<span data-ttu-id="241db-145">Określa słownik par klucz-wartość w postaci tabeli skrótów, która jest skojarzona z nową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="241db-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="241db-146">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="241db-146">For example:</span></span>

<span data-ttu-id="241db-147">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="241db-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="241db-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="241db-148">-Confirm</span></span>
<span data-ttu-id="241db-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241db-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="241db-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241db-150">-WhatIf</span></span>
<span data-ttu-id="241db-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241db-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241db-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="241db-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="241db-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241db-153">-DefaultProfile</span></span>
<span data-ttu-id="241db-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="241db-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="241db-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241db-155">CommonParameters</span></span>
<span data-ttu-id="241db-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241db-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241db-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241db-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241db-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="241db-158">INPUTS</span></span>

## <span data-ttu-id="241db-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="241db-159">OUTPUTS</span></span>

### <span data-ttu-id="241db-160">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="241db-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="241db-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="241db-161">NOTES</span></span>

## <span data-ttu-id="241db-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="241db-162">RELATED LINKS</span></span>

[<span data-ttu-id="241db-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="241db-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="241db-164">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="241db-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="241db-165">Nowe — AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="241db-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="241db-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="241db-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="241db-167">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="241db-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="241db-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="241db-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="241db-169">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="241db-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="241db-170">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="241db-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
