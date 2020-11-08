---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: 074261adf9c2f5501ca12753971fac08783ab36f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063129"
---
# <span data-ttu-id="2eb7c-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="2eb7c-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="2eb7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb7c-103">Importuje plik BACPAC i tworzy nową bazę danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="2eb7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eb7c-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2eb7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2eb7c-105">DESCRIPTION</span></span>
<span data-ttu-id="2eb7c-106">Polecenie cmdlet **New-AzSqlDatabaseImport** importuje plik BACPAC z konta usługi Azure Storage do nowej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="2eb7c-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="2eb7c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eb7c-108">EXAMPLES</span></span>

### <span data-ttu-id="2eb7c-109">Przykład 1. Tworzenie żądania importu pliku BACPAC</span><span class="sxs-lookup"><span data-stu-id="2eb7c-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="2eb7c-110">To polecenie tworzy żądanie importu w celu zaimportowania BACPAC do nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="2eb7c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eb7c-111">PARAMETERS</span></span>

### <span data-ttu-id="2eb7c-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="2eb7c-112">-AdministratorLogin</span></span>
<span data-ttu-id="2eb7c-113">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="2eb7c-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="2eb7c-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="2eb7c-115">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="2eb7c-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="2eb7c-116">-AuthenticationType</span></span>
<span data-ttu-id="2eb7c-117">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="2eb7c-118">Ten parametr ma domyślnie wartość SQL, jeśli nie ustawiono typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="2eb7c-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2eb7c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2eb7c-120">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-120">SQL.</span></span>
<span data-ttu-id="2eb7c-121">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-121">SQL authentication.</span></span>
<span data-ttu-id="2eb7c-122">Ustaw parametry *AdministratorLogin* i *AdministratorLoginPassword* z nazwą użytkownika i hasłem administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="2eb7c-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-123">ADPassword.</span></span>
<span data-ttu-id="2eb7c-124">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="2eb7c-125">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="2eb7c-126">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="2eb7c-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2eb7c-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="2eb7c-128">Określa maksymalny rozmiar nowo zaimportowanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="2eb7c-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2eb7c-129">-DatabaseName</span></span>
<span data-ttu-id="2eb7c-130">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="2eb7c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb7c-131">-DefaultProfile</span></span>
<span data-ttu-id="2eb7c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2eb7c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2eb7c-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="2eb7c-133">-Edition</span></span>
<span data-ttu-id="2eb7c-134">Określa wersję nowej bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="2eb7c-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2eb7c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2eb7c-136">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="2eb7c-136">Premium</span></span>
- <span data-ttu-id="2eb7c-137">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="2eb7c-137">Basic</span></span>
- <span data-ttu-id="2eb7c-138">Standard</span><span class="sxs-lookup"><span data-stu-id="2eb7c-138">Standard</span></span>
- <span data-ttu-id="2eb7c-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2eb7c-139">DataWarehouse</span></span>
- <span data-ttu-id="2eb7c-140">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="2eb7c-140">Free</span></span>

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

### <span data-ttu-id="2eb7c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb7c-141">-ResourceGroupName</span></span>
<span data-ttu-id="2eb7c-142">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="2eb7c-143">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2eb7c-143">-ServerName</span></span>
<span data-ttu-id="2eb7c-144">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="2eb7c-145">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="2eb7c-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="2eb7c-146">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2eb7c-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="2eb7c-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="2eb7c-148">Identyfikator zasobu programu SQL Server umożliwiający utworzenie prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="2eb7c-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="2eb7c-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="2eb7c-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="2eb7c-150">Identyfikator zasobu konta magazynu umożliwiający utworzenie prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="2eb7c-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="2eb7c-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="2eb7c-151">-StorageKey</span></span>
<span data-ttu-id="2eb7c-152">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="2eb7c-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="2eb7c-153">-StorageKeyType</span></span>
<span data-ttu-id="2eb7c-154">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="2eb7c-155">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2eb7c-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2eb7c-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-156">StorageAccessKey.</span></span>
<span data-ttu-id="2eb7c-157">Używa klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="2eb7c-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-158">SharedAccessKey.</span></span>
<span data-ttu-id="2eb7c-159">Używa klucza podpisu dostępu współdzielonego (SAS).</span><span class="sxs-lookup"><span data-stu-id="2eb7c-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="2eb7c-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="2eb7c-160">-StorageUri</span></span>
<span data-ttu-id="2eb7c-161">Określa identyfikator URI obiektu blob pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="2eb7c-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="2eb7c-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="2eb7c-163">Jeśli jest ustawiona, utworzy prywatne łącze dla konta magazynu i/lub programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="2eb7c-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb7c-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2eb7c-164">-Confirm</span></span>
<span data-ttu-id="2eb7c-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb7c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb7c-166">-WhatIf</span></span>
<span data-ttu-id="2eb7c-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb7c-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb7c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb7c-169">CommonParameters</span></span>
<span data-ttu-id="2eb7c-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb7c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb7c-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eb7c-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb7c-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eb7c-172">INPUTS</span></span>

### <span data-ttu-id="2eb7c-173">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb7c-173">System.String</span></span>

## <span data-ttu-id="2eb7c-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eb7c-174">OUTPUTS</span></span>

### <span data-ttu-id="2eb7c-175">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="2eb7c-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="2eb7c-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eb7c-176">NOTES</span></span>
* <span data-ttu-id="2eb7c-177">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2eb7c-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="2eb7c-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eb7c-178">RELATED LINKS</span></span>

[<span data-ttu-id="2eb7c-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="2eb7c-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="2eb7c-180">Nowe — AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="2eb7c-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="2eb7c-181">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2eb7c-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

