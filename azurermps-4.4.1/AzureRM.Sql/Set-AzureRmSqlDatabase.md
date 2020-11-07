---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717147"
---
# <span data-ttu-id="4249f-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4249f-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="4249f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4249f-102">SYNOPSIS</span></span>
<span data-ttu-id="4249f-103">Ustawia właściwości bazy danych lub przenosi istniejącą bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="4249f-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4249f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4249f-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4249f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4249f-105">DESCRIPTION</span></span>
<span data-ttu-id="4249f-106">Polecenie cmdlet **Set-AzureRmSqlDatabase** ustawia właściwości dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4249f-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="4249f-107">Ponadto można określić parametr *ElasticPoolName* , aby przenieść bazę danych do puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="4249f-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="4249f-108">Jeśli baza danych znajduje się już w puli elastycznej, można użyć parametru *RequestedServiceObjectiveName* , aby przypisać poziom wydajności.</span><span class="sxs-lookup"><span data-stu-id="4249f-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="4249f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4249f-109">EXAMPLES</span></span>

### <span data-ttu-id="4249f-110">Przykład 1: aktualizowanie bazy danych do standardowej S2 bazy danych</span><span class="sxs-lookup"><span data-stu-id="4249f-110">Example 1: Update a database to a Standard S2 database</span></span>
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

<span data-ttu-id="4249f-111">To polecenie aktualizuje bazę danych o nazwie Database01 do standardowej S2 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4249f-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="4249f-112">Przykład 2: Dodawanie bazy danych do puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="4249f-112">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="4249f-113">To polecenie dodaje bazę danych o nazwie Database01 do puli elastycznej o nazwie ElasticPool01 hostowanej na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4249f-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="4249f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4249f-114">PARAMETERS</span></span>

### <span data-ttu-id="4249f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4249f-115">-DatabaseName</span></span>
<span data-ttu-id="4249f-116">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4249f-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="4249f-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="4249f-117">-Edition</span></span>
<span data-ttu-id="4249f-118">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4249f-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="4249f-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4249f-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4249f-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4249f-120">None</span></span>
- <span data-ttu-id="4249f-121">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="4249f-121">Premium</span></span>
- <span data-ttu-id="4249f-122">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="4249f-122">Basic</span></span>
- <span data-ttu-id="4249f-123">Standard</span><span class="sxs-lookup"><span data-stu-id="4249f-123">Standard</span></span>
- <span data-ttu-id="4249f-124">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="4249f-124">DataWarehouse</span></span>
- <span data-ttu-id="4249f-125">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="4249f-125">Free</span></span>

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

### <span data-ttu-id="4249f-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4249f-126">-ElasticPoolName</span></span>
<span data-ttu-id="4249f-127">Określa nazwę puli elastycznej, w której ma zostać przeniesiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="4249f-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="4249f-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="4249f-128">-MaxSizeBytes</span></span>
<span data-ttu-id="4249f-129">Określa nowy maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="4249f-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="4249f-130">Możesz określić ten parametr lub *MaxSizeGB*.</span><span class="sxs-lookup"><span data-stu-id="4249f-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="4249f-131">Zapoznaj się z parametrem *MaxSizeGB* , aby uzyskać dopuszczalne wartości dla wersji.</span><span class="sxs-lookup"><span data-stu-id="4249f-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="4249f-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="4249f-132">-ReadScale</span></span>
<span data-ttu-id="4249f-133">Opcja Skala odczytu umożliwiająca przypisanie do bazy danych SQL Azure. (Włączone/wyłączone)</span><span class="sxs-lookup"><span data-stu-id="4249f-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="4249f-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4249f-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="4249f-135">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4249f-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="4249f-136">Aby uzyskać informacje na temat celów usługi, zobacz [warstwy usług Azure SQL Database i poziomy wydajności](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="4249f-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="4249f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4249f-137">-ResourceGroupName</span></span>
<span data-ttu-id="4249f-138">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="4249f-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4249f-139">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4249f-139">-ServerName</span></span>
<span data-ttu-id="4249f-140">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4249f-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4249f-141">-Tagi</span><span class="sxs-lookup"><span data-stu-id="4249f-141">-Tags</span></span>
<span data-ttu-id="4249f-142">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4249f-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4249f-143">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="4249f-143">For example:</span></span>

<span data-ttu-id="4249f-144">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4249f-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4249f-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4249f-145">-Confirm</span></span>
<span data-ttu-id="4249f-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4249f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4249f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4249f-147">-WhatIf</span></span>
<span data-ttu-id="4249f-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4249f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4249f-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4249f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4249f-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4249f-150">-DefaultProfile</span></span>
<span data-ttu-id="4249f-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4249f-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4249f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4249f-152">CommonParameters</span></span>
<span data-ttu-id="4249f-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4249f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4249f-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4249f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4249f-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4249f-155">INPUTS</span></span>

## <span data-ttu-id="4249f-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4249f-156">OUTPUTS</span></span>

### <span data-ttu-id="4249f-157">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4249f-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4249f-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4249f-158">NOTES</span></span>

## <span data-ttu-id="4249f-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4249f-159">RELATED LINKS</span></span>

[<span data-ttu-id="4249f-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4249f-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="4249f-161">Nowe — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4249f-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="4249f-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4249f-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="4249f-163">Życiorys — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4249f-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="4249f-164">Suspend — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4249f-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="4249f-165">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4249f-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
