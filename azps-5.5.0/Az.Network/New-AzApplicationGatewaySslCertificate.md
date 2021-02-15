---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193691"
---
# <span data-ttu-id="5bd91-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bd91-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5bd91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd91-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd91-103">Tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd91-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5bd91-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bd91-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bd91-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bd91-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd91-106">Polecenie **cmdlet New-AzApplicationGatewaySslCertificate** tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd91-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5bd91-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bd91-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd91-108">Przykład 1. Tworzenie certyfikatu SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd91-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="5bd91-109">To polecenie tworzy certyfikat SSL o nazwie Cert01 dla domyślnej bramy aplikacji i przechowuje wynik w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="5bd91-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="5bd91-110">Przykład 2. Tworzenie certyfikatu SSL przy użyciu klucza KeyVault Secret (klucz tajny bez wersji) i dodawanie go do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5bd91-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="5bd91-111">Uzyskaj klucz tajny i utwórz certyfikat SSL przy `New-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="5bd91-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="5bd91-112">Uwaga: Jeśli w tym miejscu podano klucz secretId bez wersji, brama aplikacji będzie synchronizować certyfikat w regularnych odstępach czasu za pomocą klawisza KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5bd91-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="5bd91-113">Przykład 3. Tworzenie certyfikatu SSL przy użyciu klucza KeyVault Secret i dodawanie go do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5bd91-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="5bd91-114">Uzyskaj klucz tajny i utwórz certyfikat SSL przy `New-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="5bd91-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="5bd91-115">Uwaga: Jeśli wymagane jest zsynchronizowanie certyfikatu przez bramę aplikacji z kluczem KeyVault, podaj klucz secretId bez klucza wersji.</span><span class="sxs-lookup"><span data-stu-id="5bd91-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="5bd91-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bd91-116">PARAMETERS</span></span>

### <span data-ttu-id="5bd91-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5bd91-117">-CertificateFile</span></span>
<span data-ttu-id="5bd91-118">Określa ścieżkę pliku pfx certyfikatu SSL, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd91-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5bd91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd91-119">-DefaultProfile</span></span>
<span data-ttu-id="5bd91-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bd91-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="5bd91-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="5bd91-122">SecretId (uri) klucza tajnego KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5bd91-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="5bd91-123">Użyj tej opcji, gdy trzeba użyć określonej wersji informacji tajnej.</span><span class="sxs-lookup"><span data-stu-id="5bd91-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="5bd91-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5bd91-124">-Name</span></span>
<span data-ttu-id="5bd91-125">Określa nazwę certyfikatu SSL, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd91-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5bd91-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="5bd91-126">-Password</span></span>
<span data-ttu-id="5bd91-127">Określa hasło do protokołu SSL, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd91-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5bd91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd91-128">CommonParameters</span></span>
<span data-ttu-id="5bd91-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd91-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bd91-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd91-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bd91-131">INPUTS</span></span>

### <span data-ttu-id="5bd91-132">Brak</span><span class="sxs-lookup"><span data-stu-id="5bd91-132">None</span></span>

## <span data-ttu-id="5bd91-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bd91-133">OUTPUTS</span></span>

### <span data-ttu-id="5bd91-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bd91-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5bd91-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bd91-135">NOTES</span></span>

## <span data-ttu-id="5bd91-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bd91-136">RELATED LINKS</span></span>

[<span data-ttu-id="5bd91-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bd91-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5bd91-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bd91-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5bd91-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bd91-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5bd91-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bd91-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


