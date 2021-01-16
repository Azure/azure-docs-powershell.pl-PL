---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336946"
---
# <span data-ttu-id="5ff6c-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="5ff6c-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="5ff6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ff6c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff6c-103">Dodaje przezroczysty certyfikat szyfrowania danych dla danego wystąpienia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="5ff6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ff6c-104">SYNTAX</span></span>

### <span data-ttu-id="5ff6c-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ff6c-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff6c-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ff6c-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff6c-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ff6c-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff6c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5ff6c-108">DESCRIPTION</span></span>
<span data-ttu-id="5ff6c-109">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate dodaje przezroczysty certyfikat szyfrowania danych dla danego wystąpienia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="5ff6c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ff6c-110">EXAMPLES</span></span>

### <span data-ttu-id="5ff6c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ff6c-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="5ff6c-112">Dodawanie certyfikatu TDE do programu SQL Server przy użyciu nazwy grupy zasobów i nazwy programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="5ff6c-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="5ff6c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5ff6c-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="5ff6c-114">Dodawanie certyfikatu TDE do serwerów za pomocą zasobu resourceId serwera</span><span class="sxs-lookup"><span data-stu-id="5ff6c-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="5ff6c-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5ff6c-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="5ff6c-116">Dodawanie certyfikatu TDE do wszystkich serwerów SQL w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="5ff6c-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="5ff6c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ff6c-117">PARAMETERS</span></span>

### <span data-ttu-id="5ff6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff6c-118">-DefaultProfile</span></span>
<span data-ttu-id="5ff6c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff6c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ff6c-120">-PassThru</span></span>
<span data-ttu-id="5ff6c-121">Po poprawnym wykonaniu zostanie zwrócony obiekt certyfikatu, który został dodany.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="5ff6c-122">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="5ff6c-122">-Password</span></span>
<span data-ttu-id="5ff6c-123">Hasło dla przezroczystego certyfikatu szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="5ff6c-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="5ff6c-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="5ff6c-124">-PrivateBlob</span></span>
<span data-ttu-id="5ff6c-125">Prywatny obiekt BLOB dla przezroczystego certyfikatu szyfrowania danych</span><span class="sxs-lookup"><span data-stu-id="5ff6c-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="5ff6c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff6c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ff6c-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5ff6c-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="5ff6c-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5ff6c-128">-ServerName</span></span>
<span data-ttu-id="5ff6c-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="5ff6c-129">The Server Name</span></span>

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

### <span data-ttu-id="5ff6c-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="5ff6c-130">-SqlServer</span></span>
<span data-ttu-id="5ff6c-131">Obiekt wejściowy programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="5ff6c-131">The sql server input object</span></span>

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

### <span data-ttu-id="5ff6c-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff6c-132">-SqlServerResourceId</span></span>
<span data-ttu-id="5ff6c-133">Identyfikator zasobu programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="5ff6c-133">The sql server resource id</span></span>

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

### <span data-ttu-id="5ff6c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ff6c-134">-Confirm</span></span>
<span data-ttu-id="5ff6c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff6c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff6c-136">-WhatIf</span></span>
<span data-ttu-id="5ff6c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff6c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff6c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff6c-139">CommonParameters</span></span>
<span data-ttu-id="5ff6c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff6c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff6c-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ff6c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff6c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ff6c-142">INPUTS</span></span>

### <span data-ttu-id="5ff6c-143">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5ff6c-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5ff6c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff6c-144">System.String</span></span>

## <span data-ttu-id="5ff6c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ff6c-145">OUTPUTS</span></span>

### <span data-ttu-id="5ff6c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ff6c-146">System.Boolean</span></span>

## <span data-ttu-id="5ff6c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ff6c-147">NOTES</span></span>

## <span data-ttu-id="5ff6c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ff6c-148">RELATED LINKS</span></span>
