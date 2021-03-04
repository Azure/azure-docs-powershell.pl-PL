---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: f1b944e2673c9682a0194c4996fa4d2b34fae97b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952154"
---
# <span data-ttu-id="ba012-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba012-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ba012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba012-102">SYNOPSIS</span></span>
<span data-ttu-id="ba012-103">Aktualizuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ba012-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="ba012-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba012-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba012-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba012-105">DESCRIPTION</span></span>
<span data-ttu-id="ba012-106">Polecenie **cmdlet Set-AzApplicationGatewaySslCertificate** aktualizuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ba012-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="ba012-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba012-107">EXAMPLES</span></span>

### <span data-ttu-id="ba012-108">Przykład 1. Aktualizowanie istniejącego certyfikatu SSL w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ba012-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="ba012-109">Zaktualizuj istniejący certyfikat SSL dla bramy aplikacji o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="ba012-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="ba012-110">Przykład 2. Aktualizowanie istniejącego certyfikatu SSL przy użyciu klucza KeyVault Secret (klucz tajny bez wersji) w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ba012-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="ba012-111">Uzyskaj klucz tajny i zaktualizuj istniejący certyfikat SSL przy `Set-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="ba012-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="ba012-112">Przykład 3. Aktualizowanie istniejącego certyfikatu SSL przy użyciu klucza Klucz Tajny w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ba012-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="ba012-113">Uzyskaj klucz tajny i zaktualizuj istniejący certyfikat SSL przy `Set-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="ba012-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="ba012-114">Uwaga: Jeśli wymagane jest zsynchronizowanie certyfikatu przez bramę aplikacji z kluczem KeyVault, podaj klucz secretId bez klucza wersji.</span><span class="sxs-lookup"><span data-stu-id="ba012-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="ba012-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba012-115">PARAMETERS</span></span>

### <span data-ttu-id="ba012-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba012-116">-ApplicationGateway</span></span>
<span data-ttu-id="ba012-117">Określa bramę aplikacji, z którą jest skojarzony certyfikat SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="ba012-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="ba012-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ba012-118">-CertificateFile</span></span>
<span data-ttu-id="ba012-119">Określa ścieżkę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="ba012-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="ba012-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba012-120">-DefaultProfile</span></span>
<span data-ttu-id="ba012-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba012-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba012-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="ba012-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="ba012-123">SecretId (uri) klucza tajnego KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ba012-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="ba012-124">Użyj tej opcji, gdy trzeba użyć określonej wersji informacji tajnej.</span><span class="sxs-lookup"><span data-stu-id="ba012-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="ba012-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ba012-125">-Name</span></span>
<span data-ttu-id="ba012-126">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="ba012-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="ba012-127">— Hasło</span><span class="sxs-lookup"><span data-stu-id="ba012-127">-Password</span></span>
<span data-ttu-id="ba012-128">Określa hasło certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="ba012-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="ba012-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba012-129">CommonParameters</span></span>
<span data-ttu-id="ba012-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba012-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba012-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba012-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba012-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba012-132">INPUTS</span></span>

### <span data-ttu-id="ba012-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba012-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ba012-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba012-134">OUTPUTS</span></span>

### <span data-ttu-id="ba012-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba012-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ba012-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba012-136">NOTES</span></span>

## <span data-ttu-id="ba012-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba012-137">RELATED LINKS</span></span>

[<span data-ttu-id="ba012-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba012-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ba012-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba012-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ba012-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba012-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ba012-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba012-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


