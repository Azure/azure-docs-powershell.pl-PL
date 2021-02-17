---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: ab1fcfa9b050f795a464488df51768b95996eb8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188074"
---
# <span data-ttu-id="d6845-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="d6845-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="d6845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6845-102">SYNOPSIS</span></span>
<span data-ttu-id="d6845-103">Importuje plik bacpac i tworzy nową bazę danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="d6845-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="d6845-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6845-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6845-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6845-105">DESCRIPTION</span></span>
<span data-ttu-id="d6845-106">Polecenie cmdlet **New-AzSqlDatabaseImport** importuje plik bacpac z konta magazynu platformy Azure do nowej bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d6845-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="d6845-107">Żądanie pobrania importowej bazy danych może zostać wysłane w celu pobrania informacji o stanie dla tego żądania.</span><span class="sxs-lookup"><span data-stu-id="d6845-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="d6845-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6845-108">EXAMPLES</span></span>

### <span data-ttu-id="d6845-109">Przykład 1. Tworzenie żądania importu pliku bacpac</span><span class="sxs-lookup"><span data-stu-id="d6845-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="d6845-110">To polecenie tworzy żądanie importu w celu zaimportowania pliku bacpac do nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d6845-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="d6845-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6845-111">PARAMETERS</span></span>

### <span data-ttu-id="d6845-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="d6845-112">-AdministratorLogin</span></span>
<span data-ttu-id="d6845-113">Określa nazwę administratora języka SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="d6845-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d6845-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d6845-115">Określa hasło administratora języka SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="d6845-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d6845-116">-AuthenticationType</span></span>
<span data-ttu-id="d6845-117">Określa typ uwierzytelniania używanego do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="d6845-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="d6845-118">Ten parametr domyślnie ma wartość SQL, jeśli nie ustawiono typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="d6845-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="d6845-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6845-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6845-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-120">SQL.</span></span>
<span data-ttu-id="d6845-121">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-121">SQL authentication.</span></span>
<span data-ttu-id="d6845-122">Ustaw parametry *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="d6845-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="d6845-123">ADPassword.</span></span>
<span data-ttu-id="d6845-124">Uwierzytelnianie w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d6845-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="d6845-125">Ustaw *hasło AdministratorLogin* i *AdministratorLoginPassword na* nazwę użytkownika i hasło administratora usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d6845-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="d6845-126">Ten parametr jest dostępny tylko na serwerach sql database w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="d6845-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="d6845-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="d6845-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="d6845-128">Określa maksymalny rozmiar nowo zaimportowanych baz danych.</span><span class="sxs-lookup"><span data-stu-id="d6845-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="d6845-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6845-129">-DatabaseName</span></span>
<span data-ttu-id="d6845-130">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="d6845-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6845-131">-DefaultProfile</span></span>
<span data-ttu-id="d6845-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d6845-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6845-133">— wersja</span><span class="sxs-lookup"><span data-stu-id="d6845-133">-Edition</span></span>
<span data-ttu-id="d6845-134">Określa wersję nowej bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="d6845-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="d6845-135">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6845-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6845-136">Premium</span><span class="sxs-lookup"><span data-stu-id="d6845-136">Premium</span></span>
- <span data-ttu-id="d6845-137">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="d6845-137">Basic</span></span>
- <span data-ttu-id="d6845-138">Standardowe</span><span class="sxs-lookup"><span data-stu-id="d6845-138">Standard</span></span>
- <span data-ttu-id="d6845-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="d6845-139">DataWarehouse</span></span>
- <span data-ttu-id="d6845-140">Bezpłatne</span><span class="sxs-lookup"><span data-stu-id="d6845-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6845-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6845-141">-ResourceGroupName</span></span>
<span data-ttu-id="d6845-142">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="d6845-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6845-143">-ServerName</span></span>
<span data-ttu-id="d6845-144">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d6845-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="d6845-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d6845-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="d6845-146">Określa nazwę celu usługi, który ma zostać przypisany do usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d6845-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d6845-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="d6845-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="d6845-148">Identyfikator zasobu programu Sql Server do utworzenia linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d6845-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="d6845-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="d6845-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="d6845-150">Identyfikator zasobu konta magazynu do utworzenia linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d6845-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="d6845-151">- KluczDazydzydów</span><span class="sxs-lookup"><span data-stu-id="d6845-151">-StorageKey</span></span>
<span data-ttu-id="d6845-152">Określa klucz dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d6845-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="d6845-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d6845-153">-StorageKeyType</span></span>
<span data-ttu-id="d6845-154">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d6845-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="d6845-155">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6845-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6845-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d6845-156">StorageAccessKey.</span></span>
<span data-ttu-id="d6845-157">Używa klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d6845-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="d6845-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d6845-158">SharedAccessKey.</span></span>
<span data-ttu-id="d6845-159">Używa klawisza SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="d6845-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="d6845-160">— StorageUri</span><span class="sxs-lookup"><span data-stu-id="d6845-160">-StorageUri</span></span>
<span data-ttu-id="d6845-161">Określa URI obiektu blob pliku bacpac.</span><span class="sxs-lookup"><span data-stu-id="d6845-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="d6845-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="d6845-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="d6845-163">Jeśli jest ustawiona, spowoduje utworzenie linku prywatnego dla konta magazynu i/lub serwera SQL</span><span class="sxs-lookup"><span data-stu-id="d6845-163">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="d6845-164">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6845-164">-Confirm</span></span>
<span data-ttu-id="d6845-165">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6845-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6845-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6845-166">-WhatIf</span></span>
<span data-ttu-id="d6845-167">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6845-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6845-168">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6845-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6845-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6845-169">CommonParameters</span></span>
<span data-ttu-id="d6845-170">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6845-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6845-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6845-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6845-172">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6845-172">INPUTS</span></span>

### <span data-ttu-id="d6845-173">System.String</span><span class="sxs-lookup"><span data-stu-id="d6845-173">System.String</span></span>

## <span data-ttu-id="d6845-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6845-174">OUTPUTS</span></span>

### <span data-ttu-id="d6845-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="d6845-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="d6845-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6845-176">NOTES</span></span>
* <span data-ttu-id="d6845-177">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="d6845-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d6845-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6845-178">RELATED LINKS</span></span>

[<span data-ttu-id="d6845-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="d6845-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="d6845-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="d6845-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="d6845-181">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d6845-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

