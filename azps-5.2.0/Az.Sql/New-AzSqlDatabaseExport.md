---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 737b7170b774be712fb316f5c76b95d326e22fdb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345001"
---
# <span data-ttu-id="3d2bc-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="3d2bc-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="3d2bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2bc-103">Eksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="3d2bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d2bc-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d2bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="3d2bc-106">Polecenie cmdlet **New-AzSqlDatabaseExport** wyeksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="3d2bc-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych — eksport.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="3d2bc-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d2bc-109">Aby móc korzystać z tego polecenia cmdlet, Zapora w usłudze Azure SQL Server musi być skonfigurowana tak, aby można było uzyskać dostęp do tego serwera za pomocą usług platformy Azure i zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="3d2bc-110">Jeśli nie zostanie to skonfigurowane, będą występować błędy GatewayTimeout.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="3d2bc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d2bc-111">EXAMPLES</span></span>

### <span data-ttu-id="3d2bc-112">Przykład 1. Tworzenie żądania eksportu bazy danych</span><span class="sxs-lookup"><span data-stu-id="3d2bc-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="3d2bc-113">To polecenie tworzy żądanie eksportu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="3d2bc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d2bc-114">PARAMETERS</span></span>

### <span data-ttu-id="3d2bc-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="3d2bc-115">-AdministratorLogin</span></span>
<span data-ttu-id="3d2bc-116">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="3d2bc-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3d2bc-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3d2bc-118">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="3d2bc-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3d2bc-119">-AuthenticationType</span></span>
<span data-ttu-id="3d2bc-120">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="3d2bc-121">Wartość domyślna to SQL, jeśli nie jest ustawiony typ uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="3d2bc-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3d2bc-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d2bc-123">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-123">Sql.</span></span>
<span data-ttu-id="3d2bc-124">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-124">SQL authentication.</span></span>
<span data-ttu-id="3d2bc-125">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="3d2bc-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-126">ADPassword.</span></span>
<span data-ttu-id="3d2bc-127">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="3d2bc-128">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="3d2bc-129">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="3d2bc-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d2bc-130">-DatabaseName</span></span>
<span data-ttu-id="3d2bc-131">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-131">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d2bc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2bc-132">-DefaultProfile</span></span>
<span data-ttu-id="3d2bc-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3d2bc-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d2bc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d2bc-134">-ResourceGroupName</span></span>
<span data-ttu-id="3d2bc-135">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="3d2bc-136">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3d2bc-136">-ServerName</span></span>
<span data-ttu-id="3d2bc-137">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="3d2bc-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="3d2bc-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="3d2bc-139">Identyfikator zasobu programu SQL Server umożliwiający utworzenie prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="3d2bc-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="3d2bc-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="3d2bc-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="3d2bc-141">Identyfikator zasobu konta magazynu umożliwiający utworzenie prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="3d2bc-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="3d2bc-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3d2bc-142">-StorageKey</span></span>
<span data-ttu-id="3d2bc-143">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3d2bc-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3d2bc-144">-StorageKeyType</span></span>
<span data-ttu-id="3d2bc-145">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="3d2bc-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3d2bc-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d2bc-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-147">StorageAccessKey.</span></span>
<span data-ttu-id="3d2bc-148">Ta wartość korzysta z klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="3d2bc-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-149">SharedAccessKey.</span></span>
<span data-ttu-id="3d2bc-150">Ta wartość używa klucza (SAS) (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="3d2bc-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="3d2bc-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3d2bc-151">-StorageUri</span></span>
<span data-ttu-id="3d2bc-152">Określa łącze obiektu BLOB jako adres URL pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="3d2bc-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="3d2bc-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="3d2bc-154">Jeśli jest ustawiona, utworzy prywatne łącze dla konta magazynu i/lub programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="3d2bc-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="3d2bc-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d2bc-155">-Confirm</span></span>
<span data-ttu-id="3d2bc-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d2bc-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d2bc-157">-WhatIf</span></span>
<span data-ttu-id="3d2bc-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d2bc-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d2bc-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2bc-160">CommonParameters</span></span>
<span data-ttu-id="3d2bc-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2bc-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d2bc-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2bc-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d2bc-163">INPUTS</span></span>

### <span data-ttu-id="3d2bc-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3d2bc-164">System.String</span></span>

## <span data-ttu-id="3d2bc-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d2bc-165">OUTPUTS</span></span>

### <span data-ttu-id="3d2bc-166">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="3d2bc-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="3d2bc-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d2bc-167">NOTES</span></span>
* <span data-ttu-id="3d2bc-168">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="3d2bc-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3d2bc-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d2bc-169">RELATED LINKS</span></span>

[<span data-ttu-id="3d2bc-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="3d2bc-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="3d2bc-171">Nowe — AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="3d2bc-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="3d2bc-172">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3d2bc-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
