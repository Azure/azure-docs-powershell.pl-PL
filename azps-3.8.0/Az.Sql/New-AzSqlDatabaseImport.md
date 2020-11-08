---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: 8b898d401c9c20efdd25fd09b5a6eedaf3e2b422
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051439"
---
# <span data-ttu-id="f75c4-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="f75c4-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="f75c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f75c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f75c4-103">Importuje plik BACPAC i tworzy nową bazę danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f75c4-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="f75c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f75c4-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f75c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f75c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f75c4-106">Polecenie cmdlet **New-AzSqlDatabaseImport** importuje plik BACPAC z konta usługi Azure Storage do nowej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f75c4-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="f75c4-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f75c4-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="f75c4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f75c4-108">EXAMPLES</span></span>

### <span data-ttu-id="f75c4-109">Przykład 1. Tworzenie żądania importu pliku BACPAC</span><span class="sxs-lookup"><span data-stu-id="f75c4-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="f75c4-110">To polecenie tworzy żądanie importu w celu zaimportowania BACPAC do nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f75c4-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="f75c4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f75c4-111">PARAMETERS</span></span>

### <span data-ttu-id="f75c4-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="f75c4-112">-AdministratorLogin</span></span>
<span data-ttu-id="f75c4-113">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f75c4-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f75c4-115">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f75c4-116">-AuthenticationType</span></span>
<span data-ttu-id="f75c4-117">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="f75c4-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="f75c4-118">Ten parametr ma domyślnie wartość SQL, jeśli nie ustawiono typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="f75c4-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="f75c4-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f75c4-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f75c4-120">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="f75c4-120">SQL.</span></span>
<span data-ttu-id="f75c4-121">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-121">SQL authentication.</span></span>
<span data-ttu-id="f75c4-122">Ustaw parametry *AdministratorLogin* i *AdministratorLoginPassword* z nazwą użytkownika i hasłem administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="f75c4-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="f75c4-123">ADPassword.</span></span>
<span data-ttu-id="f75c4-124">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f75c4-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="f75c4-125">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f75c4-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="f75c4-126">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f75c4-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="f75c4-128">Określa maksymalny rozmiar nowo zaimportowanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f75c4-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f75c4-129">-DatabaseName</span></span>
<span data-ttu-id="f75c4-130">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75c4-131">-DefaultProfile</span></span>
<span data-ttu-id="f75c4-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f75c4-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f75c4-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="f75c4-133">-Edition</span></span>
<span data-ttu-id="f75c4-134">Określa wersję nowej bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f75c4-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="f75c4-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f75c4-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f75c4-136">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="f75c4-136">Premium</span></span>
- <span data-ttu-id="f75c4-137">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="f75c4-137">Basic</span></span>
- <span data-ttu-id="f75c4-138">Standard</span><span class="sxs-lookup"><span data-stu-id="f75c4-138">Standard</span></span>
- <span data-ttu-id="f75c4-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f75c4-139">DataWarehouse</span></span>
- <span data-ttu-id="f75c4-140">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="f75c4-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75c4-141">-ResourceGroupName</span></span>
<span data-ttu-id="f75c4-142">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="f75c4-143">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f75c4-143">-ServerName</span></span>
<span data-ttu-id="f75c4-144">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f75c4-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="f75c4-145">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="f75c4-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="f75c4-146">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f75c4-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f75c4-147">-StorageKey</span></span>
<span data-ttu-id="f75c4-148">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f75c4-148">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f75c4-149">-StorageKeyType</span></span>
<span data-ttu-id="f75c4-150">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f75c4-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="f75c4-151">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f75c4-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f75c4-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f75c4-152">StorageAccessKey.</span></span>
<span data-ttu-id="f75c4-153">Używa klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f75c4-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="f75c4-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f75c4-154">SharedAccessKey.</span></span>
<span data-ttu-id="f75c4-155">Używa klucza podpisu dostępu współdzielonego (SAS).</span><span class="sxs-lookup"><span data-stu-id="f75c4-155">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f75c4-156">-StorageUri</span></span>
<span data-ttu-id="f75c4-157">Określa identyfikator URI obiektu blob pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="f75c4-157">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f75c4-158">-Confirm</span></span>
<span data-ttu-id="f75c4-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75c4-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75c4-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75c4-160">-WhatIf</span></span>
<span data-ttu-id="f75c4-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75c4-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f75c4-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f75c4-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75c4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75c4-163">CommonParameters</span></span>
<span data-ttu-id="f75c4-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75c4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75c4-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f75c4-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75c4-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f75c4-166">INPUTS</span></span>

### <span data-ttu-id="f75c4-167">System. String</span><span class="sxs-lookup"><span data-stu-id="f75c4-167">System.String</span></span>

## <span data-ttu-id="f75c4-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f75c4-168">OUTPUTS</span></span>

### <span data-ttu-id="f75c4-169">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="f75c4-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="f75c4-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f75c4-170">NOTES</span></span>
* <span data-ttu-id="f75c4-171">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="f75c4-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f75c4-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f75c4-172">RELATED LINKS</span></span>

[<span data-ttu-id="f75c4-173">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="f75c4-173">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="f75c4-174">Nowe — AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="f75c4-174">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="f75c4-175">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f75c4-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

