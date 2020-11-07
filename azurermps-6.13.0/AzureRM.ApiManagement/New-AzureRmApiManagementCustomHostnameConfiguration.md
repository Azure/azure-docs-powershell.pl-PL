---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717985"
---
# <span data-ttu-id="c6315-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6315-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="c6315-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6315-102">SYNOPSIS</span></span>
<span data-ttu-id="c6315-103">Tworzy wystąpienie `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="c6315-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6315-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6315-104">SYNTAX</span></span>

### <span data-ttu-id="c6315-105">NoChangeCertificate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c6315-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6315-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="c6315-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6315-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="c6315-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6315-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6315-108">DESCRIPTION</span></span>
<span data-ttu-id="c6315-109">Polecenie cmdlet **New-AzureRmApiManagementCustomHostnameConfiguration** jest poleceniem pomagającym, które tworzy wystąpienie **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c6315-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="c6315-110">To polecenie jest używane w przypadku polecenia cmdlet New-AzureRmApiManagement i Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c6315-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="c6315-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6315-111">EXAMPLES</span></span>

### <span data-ttu-id="c6315-112">Przykład 1: Tworzenie i Inicjowanie wystąpienia PsApiManagementCustomHostNameConfiguration przy użyciu certyfikatu SSL z pliku</span><span class="sxs-lookup"><span data-stu-id="c6315-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="c6315-113">To polecenie tworzy i Inicjuje wystąpienie **PsApiManagementCustomHostNameConfiguration** dla portalu.</span><span class="sxs-lookup"><span data-stu-id="c6315-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="c6315-114">Następnie tworzona jest nowa usługa ApiManagement z niestandardową konfiguracją nazw hostów.</span><span class="sxs-lookup"><span data-stu-id="c6315-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="c6315-115">Przykład 2: Tworzenie i Inicjowanie wystąpienia PsApiManagementCustomHostNameConfiguration przy użyciu klucza tajnego z zasobu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="c6315-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="c6315-116">To polecenie tworzy i Inicjuje wystąpienie **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c6315-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="c6315-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6315-117">PARAMETERS</span></span>

### <span data-ttu-id="c6315-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6315-118">-DefaultProfile</span></span>
<span data-ttu-id="c6315-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6315-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6315-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="c6315-120">-DefaultSslBinding</span></span>
<span data-ttu-id="c6315-121">Określa, czy wartość jest kluczem tajnym i czy ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="c6315-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="c6315-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c6315-122">This parameter is optional.</span></span>
<span data-ttu-id="c6315-123">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="c6315-123">Default Value is false.</span></span>

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

### <span data-ttu-id="c6315-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="c6315-124">-Hostname</span></span>
<span data-ttu-id="c6315-125">Nazwa hosta niestandardowego</span><span class="sxs-lookup"><span data-stu-id="c6315-125">Custom Hostname</span></span>

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

### <span data-ttu-id="c6315-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="c6315-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="c6315-127">Konfiguracja istniejącej konfiguracji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c6315-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="c6315-128">-Nazwa_hostatype</span><span class="sxs-lookup"><span data-stu-id="c6315-128">-HostnameType</span></span>
<span data-ttu-id="c6315-129">Typ hostnamea</span><span class="sxs-lookup"><span data-stu-id="c6315-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6315-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c6315-130">-KeyVaultId</span></span>
<span data-ttu-id="c6315-131">KeyVaultId do poufnego przechowywania niestandardowego certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="c6315-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="c6315-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c6315-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="c6315-133">Określa, czy wartość jest kluczem tajnym i czy ma być szyfrowana.</span><span class="sxs-lookup"><span data-stu-id="c6315-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="c6315-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c6315-134">This parameter is optional.</span></span>
<span data-ttu-id="c6315-135">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="c6315-135">Default Value is false.</span></span>

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

### <span data-ttu-id="c6315-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="c6315-136">-PfxPassword</span></span>
<span data-ttu-id="c6315-137">Hasło do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="c6315-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="c6315-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="c6315-138">-PfxPath</span></span>
<span data-ttu-id="c6315-139">Ścieżka do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="c6315-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="c6315-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6315-140">CommonParameters</span></span>
<span data-ttu-id="c6315-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6315-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6315-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6315-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6315-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6315-143">INPUTS</span></span>

### <span data-ttu-id="c6315-144">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="c6315-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="c6315-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6315-145">OUTPUTS</span></span>

### <span data-ttu-id="c6315-146">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6315-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="c6315-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6315-147">NOTES</span></span>

## <span data-ttu-id="c6315-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6315-148">RELATED LINKS</span></span>

[<span data-ttu-id="c6315-149">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6315-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="c6315-150">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6315-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
