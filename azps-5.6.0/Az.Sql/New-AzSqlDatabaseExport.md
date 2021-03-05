---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 198692c73609f6e3e88be0ccbe270c60bc679020
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979210"
---
# <span data-ttu-id="5f1c1-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="5f1c1-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="5f1c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1c1-103">Eksportuje bazę danych Azure SQL Database jako plik bacpac do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="5f1c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f1c1-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f1c1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f1c1-105">DESCRIPTION</span></span>
<span data-ttu-id="5f1c1-106">Polecenie **cmdlet New-AzSqlDatabaseExport** eksportuje bazę danych Azure SQL Database jako plik bacpac do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="5f1c1-107">Żądanie pobrania bazy danych eksportu może zostać wysłane w celu pobrania informacji o stanie dla tego żądania.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="5f1c1-108">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f1c1-109">Aby użyć tego polecenia cmdlet, zapora na serwerze Azure SQL Server musi być skonfigurowana tak, aby zezwalała usługom i zasobom platformy Azure na dostęp do tego serwera".</span><span class="sxs-lookup"><span data-stu-id="5f1c1-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="5f1c1-110">Jeśli ta konfiguracja nie jest skonfigurowana, będą wystąpić błędy GatewayTimeout.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="5f1c1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f1c1-111">EXAMPLES</span></span>

### <span data-ttu-id="5f1c1-112">Przykład 1. Tworzenie żądania eksportu bazy danych</span><span class="sxs-lookup"><span data-stu-id="5f1c1-112">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="5f1c1-113">To polecenie tworzy żądanie eksportu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="5f1c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f1c1-114">PARAMETERS</span></span>

### <span data-ttu-id="5f1c1-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="5f1c1-115">-AdministratorLogin</span></span>
<span data-ttu-id="5f1c1-116">Określa nazwę administratora języka SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="5f1c1-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5f1c1-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5f1c1-118">Określa hasło administratora języka SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="5f1c1-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="5f1c1-119">-AuthenticationType</span></span>
<span data-ttu-id="5f1c1-120">Określa typ uwierzytelniania używanego do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="5f1c1-121">Jeśli nie ustawiono typu uwierzytelniania, wartością domyślną jest język SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="5f1c1-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5f1c1-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5f1c1-123">Sql.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-123">Sql.</span></span>
<span data-ttu-id="5f1c1-124">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-124">SQL authentication.</span></span>
<span data-ttu-id="5f1c1-125">Ustaw ustawienia *AdministratorLogin* i *AdministratorLoginPassword na* nazwę użytkownika i hasło administratora JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="5f1c1-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-126">ADPassword.</span></span>
<span data-ttu-id="5f1c1-127">Uwierzytelnianie w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="5f1c1-128">Ustaw *hasło administratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="5f1c1-129">Ten parametr jest dostępny tylko na serwerach sql database w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="5f1c1-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f1c1-130">-DatabaseName</span></span>
<span data-ttu-id="5f1c1-131">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="5f1c1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f1c1-132">-DefaultProfile</span></span>
<span data-ttu-id="5f1c1-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5f1c1-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f1c1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f1c1-134">-ResourceGroupName</span></span>
<span data-ttu-id="5f1c1-135">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="5f1c1-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5f1c1-136">-ServerName</span></span>
<span data-ttu-id="5f1c1-137">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="5f1c1-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="5f1c1-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="5f1c1-139">Identyfikator zasobu programu Sql Server do utworzenia linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="5f1c1-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="5f1c1-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="5f1c1-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="5f1c1-141">Identyfikator zasobu konta magazynu do utworzenia linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="5f1c1-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="5f1c1-142">- KluczDazydzydów</span><span class="sxs-lookup"><span data-stu-id="5f1c1-142">-StorageKey</span></span>
<span data-ttu-id="5f1c1-143">Określa klucz dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="5f1c1-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="5f1c1-144">-StorageKeyType</span></span>
<span data-ttu-id="5f1c1-145">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="5f1c1-146">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5f1c1-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5f1c1-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-147">StorageAccessKey.</span></span>
<span data-ttu-id="5f1c1-148">Ta wartość korzysta z klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="5f1c1-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-149">SharedAccessKey.</span></span>
<span data-ttu-id="5f1c1-150">Ta wartość korzysta z klucza sygnatury SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="5f1c1-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="5f1c1-151">— StorageUri</span><span class="sxs-lookup"><span data-stu-id="5f1c1-151">-StorageUri</span></span>
<span data-ttu-id="5f1c1-152">Określa link obiektu blob (jako adres URL) do pliku bacpac.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="5f1c1-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="5f1c1-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="5f1c1-154">Jeśli jest ustawiona, spowoduje utworzenie linku prywatnego dla konta magazynu i/lub serwera SQL</span><span class="sxs-lookup"><span data-stu-id="5f1c1-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="5f1c1-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f1c1-155">-Confirm</span></span>
<span data-ttu-id="5f1c1-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f1c1-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f1c1-157">-WhatIf</span></span>
<span data-ttu-id="5f1c1-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f1c1-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f1c1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1c1-160">CommonParameters</span></span>
<span data-ttu-id="5f1c1-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f1c1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1c1-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f1c1-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1c1-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f1c1-163">INPUTS</span></span>

### <span data-ttu-id="5f1c1-164">System.String</span><span class="sxs-lookup"><span data-stu-id="5f1c1-164">System.String</span></span>

## <span data-ttu-id="5f1c1-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f1c1-165">OUTPUTS</span></span>

### <span data-ttu-id="5f1c1-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="5f1c1-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="5f1c1-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f1c1-167">NOTES</span></span>
* <span data-ttu-id="5f1c1-168">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="5f1c1-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="5f1c1-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f1c1-169">RELATED LINKS</span></span>

[<span data-ttu-id="5f1c1-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="5f1c1-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="5f1c1-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="5f1c1-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="5f1c1-172">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5f1c1-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
