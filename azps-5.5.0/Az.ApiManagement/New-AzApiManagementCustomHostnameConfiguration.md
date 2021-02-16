---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176499"
---
# <span data-ttu-id="a25ad-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a25ad-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="a25ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a25ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a25ad-103">Tworzy `PsApiManagementCustomHostNameConfiguration` wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="a25ad-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="a25ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a25ad-104">SYNTAX</span></span>

### <span data-ttu-id="a25ad-105">NoChangeCertificate (Default)</span><span class="sxs-lookup"><span data-stu-id="a25ad-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a25ad-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="a25ad-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a25ad-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="a25ad-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a25ad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a25ad-108">DESCRIPTION</span></span>
<span data-ttu-id="a25ad-109">Polecenie cmdlet **New-AzApiManagementCustomHostnameConfiguration** jest poleceniem pomocy, które tworzy wystąpienie **polecenia PsApiManagementCustomHostNameConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="a25ad-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="a25ad-110">To polecenie jest używane z poleceniem cmdlet New-AzApiManagement i Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25ad-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="a25ad-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a25ad-111">EXAMPLES</span></span>

### <span data-ttu-id="a25ad-112">Przykład 1. Tworzenie i inicjowanie wystąpienia parametru PsApiManagementCustomHostNameConfiguration przy użyciu certyfikatu SSL z pliku</span><span class="sxs-lookup"><span data-stu-id="a25ad-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="a25ad-113">To polecenie tworzy i inicjuje wystąpienie polecenia **PsApiManagementCustomHostNameConfiguration** for Portal.</span><span class="sxs-lookup"><span data-stu-id="a25ad-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="a25ad-114">Następnie tworzy nową usługę ApiManagement z niestandardową konfiguracją nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="a25ad-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="a25ad-115">Przykład 2. Tworzenie i inicjowanie wystąpienia parametru PsApiManagementCustomHostNameConfiguration przy użyciu klucza tajnego z zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="a25ad-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="a25ad-116">To polecenie tworzy i inicjuje wystąpienie polecenia **PsApiManagementCustomHostNameConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="a25ad-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="a25ad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a25ad-117">PARAMETERS</span></span>

### <span data-ttu-id="a25ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25ad-118">-DefaultProfile</span></span>
<span data-ttu-id="a25ad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a25ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a25ad-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="a25ad-120">-DefaultSslBinding</span></span>
<span data-ttu-id="a25ad-121">Określa, czy wartość jest tajny i powinna być zaszyfrowana.</span><span class="sxs-lookup"><span data-stu-id="a25ad-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="a25ad-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a25ad-122">This parameter is optional.</span></span>
<span data-ttu-id="a25ad-123">Wartość domyślna ma wartość fałszywą.</span><span class="sxs-lookup"><span data-stu-id="a25ad-123">Default Value is false.</span></span>

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

### <span data-ttu-id="a25ad-124">-Hostname (Nazwa hosta)</span><span class="sxs-lookup"><span data-stu-id="a25ad-124">-Hostname</span></span>
<span data-ttu-id="a25ad-125">Niestandardowa nazwa hosta</span><span class="sxs-lookup"><span data-stu-id="a25ad-125">Custom Hostname</span></span>

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

### <span data-ttu-id="a25ad-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="a25ad-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="a25ad-127">Istniejąca konfiguracja certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a25ad-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25ad-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="a25ad-128">-HostnameType</span></span>
<span data-ttu-id="a25ad-129">Typ hosta</span><span class="sxs-lookup"><span data-stu-id="a25ad-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25ad-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a25ad-130">-KeyVaultId</span></span>
<span data-ttu-id="a25ad-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span><span class="sxs-lookup"><span data-stu-id="a25ad-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25ad-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a25ad-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="a25ad-133">Określa, czy wartość jest tajny i powinna być zaszyfrowana.</span><span class="sxs-lookup"><span data-stu-id="a25ad-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="a25ad-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a25ad-134">This parameter is optional.</span></span>
<span data-ttu-id="a25ad-135">Wartość domyślna ma wartość fałszywą.</span><span class="sxs-lookup"><span data-stu-id="a25ad-135">Default Value is false.</span></span>

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

### <span data-ttu-id="a25ad-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="a25ad-136">-PfxPassword</span></span>
<span data-ttu-id="a25ad-137">Hasło do pliku certyfikatu pfx.</span><span class="sxs-lookup"><span data-stu-id="a25ad-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25ad-138">- PfxPath</span><span class="sxs-lookup"><span data-stu-id="a25ad-138">-PfxPath</span></span>
<span data-ttu-id="a25ad-139">Ścieżka do pliku certyfikatu pfx.</span><span class="sxs-lookup"><span data-stu-id="a25ad-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25ad-140">CommonParameters</span></span>
<span data-ttu-id="a25ad-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25ad-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a25ad-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25ad-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a25ad-143">INPUTS</span></span>

### <span data-ttu-id="a25ad-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="a25ad-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="a25ad-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a25ad-145">OUTPUTS</span></span>

### <span data-ttu-id="a25ad-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a25ad-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="a25ad-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a25ad-147">NOTES</span></span>

## <span data-ttu-id="a25ad-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a25ad-148">RELATED LINKS</span></span>

[<span data-ttu-id="a25ad-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a25ad-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="a25ad-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a25ad-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)