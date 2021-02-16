---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1dd4285b75f8c1c067f15be34a334d4d48fb4f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191643"
---
# <span data-ttu-id="a963f-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a963f-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a963f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a963f-102">SYNOPSIS</span></span>
<span data-ttu-id="a963f-103">Aktualizuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a963f-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="a963f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a963f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a963f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a963f-105">DESCRIPTION</span></span>
<span data-ttu-id="a963f-106">Polecenie **cmdlet Set-AzApplicationGatewaySslCertificate** aktualizuje certyfikat SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a963f-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="a963f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a963f-107">EXAMPLES</span></span>

### <span data-ttu-id="a963f-108">Przykład 1. Aktualizowanie istniejącego certyfikatu SSL w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a963f-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="a963f-109">Zaktualizuj istniejący certyfikat SSL dla bramy aplikacji o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="a963f-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="a963f-110">Przykład 2. Aktualizowanie istniejącego certyfikatu SSL przy użyciu klucza KeyVault Secret (klucz tajny bez wersji) w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a963f-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="a963f-111">Uzyskaj klucz tajny i zaktualizuj istniejący certyfikat SSL przy `Set-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="a963f-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="a963f-112">Przykład 3. Aktualizowanie istniejącego certyfikatu SSL przy użyciu klucza Klucz Tajny w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a963f-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="a963f-113">Uzyskaj klucz tajny i zaktualizuj istniejący certyfikat SSL przy `Set-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="a963f-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="a963f-114">Uwaga: Jeśli wymagane jest zsynchronizowanie certyfikatu przez bramę aplikacji z kluczem KeyVault, podaj klucz secretId bez klucza wersji.</span><span class="sxs-lookup"><span data-stu-id="a963f-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="a963f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a963f-115">PARAMETERS</span></span>

### <span data-ttu-id="a963f-116">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a963f-116">-ApplicationGateway</span></span>
<span data-ttu-id="a963f-117">Określa bramę aplikacji, z którą jest skojarzony certyfikat SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="a963f-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="a963f-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a963f-118">-CertificateFile</span></span>
<span data-ttu-id="a963f-119">Określa ścieżkę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="a963f-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="a963f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a963f-120">-DefaultProfile</span></span>
<span data-ttu-id="a963f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a963f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a963f-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="a963f-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="a963f-123">SecretId (uri) klucza tajnego KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a963f-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="a963f-124">Użyj tej opcji, gdy trzeba użyć określonej wersji informacji tajnej.</span><span class="sxs-lookup"><span data-stu-id="a963f-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="a963f-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a963f-125">-Name</span></span>
<span data-ttu-id="a963f-126">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="a963f-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="a963f-127">— Hasło</span><span class="sxs-lookup"><span data-stu-id="a963f-127">-Password</span></span>
<span data-ttu-id="a963f-128">Określa hasło certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="a963f-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="a963f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a963f-129">CommonParameters</span></span>
<span data-ttu-id="a963f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a963f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a963f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a963f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a963f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a963f-132">INPUTS</span></span>

### <span data-ttu-id="a963f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a963f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a963f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a963f-134">OUTPUTS</span></span>

### <span data-ttu-id="a963f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a963f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a963f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a963f-136">NOTES</span></span>

## <span data-ttu-id="a963f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a963f-137">RELATED LINKS</span></span>

[<span data-ttu-id="a963f-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a963f-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a963f-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a963f-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a963f-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a963f-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a963f-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a963f-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


