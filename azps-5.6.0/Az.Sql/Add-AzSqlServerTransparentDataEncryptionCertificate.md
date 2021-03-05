---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961450"
---
# <span data-ttu-id="bcab9-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="bcab9-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="bcab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcab9-102">SYNOPSIS</span></span>
<span data-ttu-id="bcab9-103">Dodaje certyfikat przezroczystego szyfrowania danych dla danego wystąpienia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bcab9-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="bcab9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bcab9-104">SYNTAX</span></span>

### <span data-ttu-id="bcab9-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bcab9-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcab9-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcab9-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcab9-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcab9-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcab9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bcab9-108">DESCRIPTION</span></span>
<span data-ttu-id="bcab9-109">Ta Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate dodaje certyfikat przezroczystego szyfrowania danych dla danego wystąpienia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="bcab9-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="bcab9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bcab9-110">EXAMPLES</span></span>

### <span data-ttu-id="bcab9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bcab9-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="bcab9-112">Dodawanie certyfikatu TDE do serwera sql przy użyciu nazwy grupy zasobów i nazwy programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="bcab9-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="bcab9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bcab9-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="bcab9-114">Dodawanie certyfikatu TDE do serwerów przy użyciu server resourceId</span><span class="sxs-lookup"><span data-stu-id="bcab9-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="bcab9-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="bcab9-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="bcab9-116">Dodawanie certyfikatu TDE do wszystkich serwerów sql w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="bcab9-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="bcab9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcab9-117">PARAMETERS</span></span>

### <span data-ttu-id="bcab9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcab9-118">-DefaultProfile</span></span>
<span data-ttu-id="bcab9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcab9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcab9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcab9-120">-PassThru</span></span>
<span data-ttu-id="bcab9-121">Po pomyślnym wykonaniu zwraca dodany obiekt certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bcab9-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="bcab9-122">— Hasło</span><span class="sxs-lookup"><span data-stu-id="bcab9-122">-Password</span></span>
<span data-ttu-id="bcab9-123">Hasło do certyfikatu przezroczystego szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="bcab9-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="bcab9-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="bcab9-124">-PrivateBlob</span></span>
<span data-ttu-id="bcab9-125">Prywatny obiekt blob dla certyfikatu szyfrowania przezroczystych danych</span><span class="sxs-lookup"><span data-stu-id="bcab9-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="bcab9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcab9-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcab9-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bcab9-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="bcab9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bcab9-128">-ServerName</span></span>
<span data-ttu-id="bcab9-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="bcab9-129">The Server Name</span></span>

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

### <span data-ttu-id="bcab9-130">— SqlServer</span><span class="sxs-lookup"><span data-stu-id="bcab9-130">-SqlServer</span></span>
<span data-ttu-id="bcab9-131">Obiekt wejściowy programu Sql Server</span><span class="sxs-lookup"><span data-stu-id="bcab9-131">The sql server input object</span></span>

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

### <span data-ttu-id="bcab9-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="bcab9-132">-SqlServerResourceId</span></span>
<span data-ttu-id="bcab9-133">Identyfikator zasobu programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="bcab9-133">The sql server resource id</span></span>

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

### <span data-ttu-id="bcab9-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcab9-134">-Confirm</span></span>
<span data-ttu-id="bcab9-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bcab9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcab9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcab9-136">-WhatIf</span></span>
<span data-ttu-id="bcab9-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcab9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcab9-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bcab9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcab9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcab9-139">CommonParameters</span></span>
<span data-ttu-id="bcab9-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcab9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcab9-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcab9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcab9-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcab9-142">INPUTS</span></span>

### <span data-ttu-id="bcab9-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="bcab9-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="bcab9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bcab9-144">System.String</span></span>

## <span data-ttu-id="bcab9-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcab9-145">OUTPUTS</span></span>

### <span data-ttu-id="bcab9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bcab9-146">System.Boolean</span></span>

## <span data-ttu-id="bcab9-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bcab9-147">NOTES</span></span>

## <span data-ttu-id="bcab9-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcab9-148">RELATED LINKS</span></span>
