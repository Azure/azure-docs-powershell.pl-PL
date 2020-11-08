---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063313"
---
# <span data-ttu-id="e9b82-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b82-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e9b82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9b82-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b82-103">Aktualizuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e9b82-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="e9b82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9b82-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9b82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9b82-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b82-106">Polecenie cmdlet **Set-AzApplicationGatewaySslCertificate** AKTUALIZUJE certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e9b82-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="e9b82-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9b82-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b82-108">Przykład 1: Aktualizowanie istniejącego certyfikatu SSL w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e9b82-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e9b82-109">Zaktualizuj istniejący certyfikat SSL dla bramy Application Gateway o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="e9b82-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="e9b82-110">Przykład 2: Aktualizowanie istniejącego certyfikatu SSL przy użyciu klucza tajnego magazynu kluczy (wersja-mniej secretId) w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e9b82-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e9b82-111">Uzyskaj klucz tajny i zaktualizuj istniejący certyfikat SSL przy użyciu `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="e9b82-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="e9b82-112">Przykład 3: Aktualizowanie istniejącego certyfikatu SSL przy użyciu klucza tajnego magazynu kluczy w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e9b82-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e9b82-113">Uzyskaj klucz tajny i zaktualizuj istniejący certyfikat SSL przy użyciu `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="e9b82-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="e9b82-114">Uwaga: Jeśli aplikacja jest wymagana do synchronizowania certyfikatu z usługą Magazyn klucza, należy podać wersję — mniej secretId.</span><span class="sxs-lookup"><span data-stu-id="e9b82-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="e9b82-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9b82-115">PARAMETERS</span></span>

### <span data-ttu-id="e9b82-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b82-116">-ApplicationGateway</span></span>
<span data-ttu-id="e9b82-117">Określa bramę aplikacji, z którą jest skojarzony certyfikat SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="e9b82-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b82-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e9b82-118">-CertificateFile</span></span>
<span data-ttu-id="e9b82-119">Określa ścieżkę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="e9b82-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="e9b82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b82-120">-DefaultProfile</span></span>
<span data-ttu-id="e9b82-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b82-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b82-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="e9b82-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="e9b82-123">SecretId (identyfikator URI) klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e9b82-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="e9b82-124">Użyj tej opcji, jeśli ma być używana określona wersja sekretu.</span><span class="sxs-lookup"><span data-stu-id="e9b82-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="e9b82-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9b82-125">-Name</span></span>
<span data-ttu-id="e9b82-126">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="e9b82-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="e9b82-127">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="e9b82-127">-Password</span></span>
<span data-ttu-id="e9b82-128">Określa hasło certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="e9b82-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b82-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b82-129">CommonParameters</span></span>
<span data-ttu-id="e9b82-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b82-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b82-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b82-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b82-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9b82-132">INPUTS</span></span>

### <span data-ttu-id="e9b82-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b82-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9b82-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9b82-134">OUTPUTS</span></span>

### <span data-ttu-id="e9b82-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b82-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9b82-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9b82-136">NOTES</span></span>

## <span data-ttu-id="e9b82-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9b82-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9b82-138">Dodaj-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b82-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e9b82-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b82-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e9b82-140">Nowe — AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b82-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e9b82-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b82-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


