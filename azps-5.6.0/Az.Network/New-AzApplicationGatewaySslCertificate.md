---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 84465161d726108749e09d4a928e22aea8050c92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015057"
---
# <span data-ttu-id="87751-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87751-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="87751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87751-102">SYNOPSIS</span></span>
<span data-ttu-id="87751-103">Tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87751-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="87751-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87751-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87751-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87751-105">DESCRIPTION</span></span>
<span data-ttu-id="87751-106">Polecenie **cmdlet New-AzApplicationGatewaySslCertificate** tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87751-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="87751-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87751-107">EXAMPLES</span></span>

### <span data-ttu-id="87751-108">Przykład 1. Tworzenie certyfikatu SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87751-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="87751-109">To polecenie tworzy certyfikat SSL o nazwie Cert01 dla domyślnej bramy aplikacji i przechowuje wynik w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="87751-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="87751-110">Przykład 2. Tworzenie certyfikatu SSL przy użyciu klucza KeyVault Secret (klucz tajny bez wersji) i dodawanie go do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="87751-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="87751-111">Uzyskaj klucz tajny i utwórz certyfikat SSL przy `New-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="87751-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="87751-112">Uwaga: Jeśli w tym miejscu podano klucz secretId bez wersji, brama aplikacji będzie synchronizować certyfikat w regularnych odstępach czasu za pomocą klawisza KeyVault.</span><span class="sxs-lookup"><span data-stu-id="87751-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="87751-113">Przykład 3. Tworzenie certyfikatu SSL przy użyciu klucza KeyVault Secret i dodawanie go do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="87751-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="87751-114">Uzyskaj klucz tajny i utwórz certyfikat SSL przy `New-AzApplicationGatewaySslCertificate` użyciu.</span><span class="sxs-lookup"><span data-stu-id="87751-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="87751-115">Uwaga: Jeśli wymagane jest zsynchronizowanie certyfikatu przez bramę aplikacji z kluczem KeyVault, podaj klucz secretId bez klucza wersji.</span><span class="sxs-lookup"><span data-stu-id="87751-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="87751-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87751-116">PARAMETERS</span></span>

### <span data-ttu-id="87751-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="87751-117">-CertificateFile</span></span>
<span data-ttu-id="87751-118">Określa ścieżkę pliku pfx certyfikatu SSL, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87751-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="87751-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87751-119">-DefaultProfile</span></span>
<span data-ttu-id="87751-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87751-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87751-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="87751-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="87751-122">SecretId (uri) klucza tajnego KeyVault.</span><span class="sxs-lookup"><span data-stu-id="87751-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="87751-123">Użyj tej opcji, gdy trzeba użyć określonej wersji informacji tajnej.</span><span class="sxs-lookup"><span data-stu-id="87751-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="87751-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87751-124">-Name</span></span>
<span data-ttu-id="87751-125">Określa nazwę certyfikatu SSL, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87751-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="87751-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="87751-126">-Password</span></span>
<span data-ttu-id="87751-127">Określa hasło do protokołu SSL, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87751-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="87751-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87751-128">CommonParameters</span></span>
<span data-ttu-id="87751-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87751-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87751-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87751-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87751-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87751-131">INPUTS</span></span>

### <span data-ttu-id="87751-132">Brak</span><span class="sxs-lookup"><span data-stu-id="87751-132">None</span></span>

## <span data-ttu-id="87751-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87751-133">OUTPUTS</span></span>

### <span data-ttu-id="87751-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87751-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="87751-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87751-135">NOTES</span></span>

## <span data-ttu-id="87751-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87751-136">RELATED LINKS</span></span>

[<span data-ttu-id="87751-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87751-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="87751-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87751-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="87751-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87751-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="87751-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87751-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


