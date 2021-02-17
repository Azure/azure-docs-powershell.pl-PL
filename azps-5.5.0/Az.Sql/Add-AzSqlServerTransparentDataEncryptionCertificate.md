---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242035"
---
# <span data-ttu-id="48789-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="48789-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="48789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48789-102">SYNOPSIS</span></span>
<span data-ttu-id="48789-103">Dodaje certyfikat przezroczystego szyfrowania danych dla danego wystąpienia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48789-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="48789-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48789-104">SYNTAX</span></span>

### <span data-ttu-id="48789-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="48789-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48789-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48789-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48789-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48789-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48789-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="48789-108">DESCRIPTION</span></span>
<span data-ttu-id="48789-109">Ta Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate dodaje certyfikat przezroczystego szyfrowania danych dla danego wystąpienia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="48789-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="48789-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48789-110">EXAMPLES</span></span>

### <span data-ttu-id="48789-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48789-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="48789-112">Dodawanie certyfikatu TDE do serwera sql przy użyciu nazwy grupy zasobów i nazwy programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="48789-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="48789-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="48789-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="48789-114">Dodawanie certyfikatu TDE do serwerów przy użyciu server resourceId</span><span class="sxs-lookup"><span data-stu-id="48789-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="48789-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="48789-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="48789-116">Dodawanie certyfikatu TDE do wszystkich serwerów sql w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="48789-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="48789-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48789-117">PARAMETERS</span></span>

### <span data-ttu-id="48789-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48789-118">-DefaultProfile</span></span>
<span data-ttu-id="48789-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48789-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48789-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48789-120">-PassThru</span></span>
<span data-ttu-id="48789-121">Po pomyślnym wykonaniu zwraca dodany obiekt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="48789-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="48789-122">— Hasło</span><span class="sxs-lookup"><span data-stu-id="48789-122">-Password</span></span>
<span data-ttu-id="48789-123">Hasło do certyfikatu przezroczystego szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="48789-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48789-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="48789-124">-PrivateBlob</span></span>
<span data-ttu-id="48789-125">Prywatny obiekt blob dla certyfikatu szyfrowania przezroczystych danych</span><span class="sxs-lookup"><span data-stu-id="48789-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48789-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48789-126">-ResourceGroupName</span></span>
<span data-ttu-id="48789-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="48789-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48789-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48789-128">-ServerName</span></span>
<span data-ttu-id="48789-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="48789-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48789-130">— SqlServer</span><span class="sxs-lookup"><span data-stu-id="48789-130">-SqlServer</span></span>
<span data-ttu-id="48789-131">Obiekt wejściowy programu Sql Server</span><span class="sxs-lookup"><span data-stu-id="48789-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48789-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="48789-132">-SqlServerResourceId</span></span>
<span data-ttu-id="48789-133">Identyfikator zasobu programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="48789-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48789-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48789-134">-Confirm</span></span>
<span data-ttu-id="48789-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48789-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48789-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48789-136">-WhatIf</span></span>
<span data-ttu-id="48789-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48789-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48789-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="48789-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48789-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48789-139">CommonParameters</span></span>
<span data-ttu-id="48789-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48789-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48789-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48789-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48789-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48789-142">INPUTS</span></span>

### <span data-ttu-id="48789-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="48789-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="48789-144">System.String</span><span class="sxs-lookup"><span data-stu-id="48789-144">System.String</span></span>

## <span data-ttu-id="48789-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="48789-145">OUTPUTS</span></span>

### <span data-ttu-id="48789-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48789-146">System.Boolean</span></span>

## <span data-ttu-id="48789-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48789-147">NOTES</span></span>

## <span data-ttu-id="48789-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48789-148">RELATED LINKS</span></span>
