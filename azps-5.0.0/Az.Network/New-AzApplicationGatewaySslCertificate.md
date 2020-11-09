---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: a5a1533038f8e11a30dd3fdeedd590b8186597b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318012"
---
# <span data-ttu-id="5bde0-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bde0-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5bde0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bde0-102">SYNOPSIS</span></span>
<span data-ttu-id="5bde0-103">Tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bde0-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5bde0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bde0-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bde0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5bde0-105">DESCRIPTION</span></span>
<span data-ttu-id="5bde0-106">Polecenie cmdlet **New-AzApplicationGatewaySslCertificate** tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bde0-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5bde0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bde0-107">EXAMPLES</span></span>

### <span data-ttu-id="5bde0-108">Przykład 1: Tworzenie certyfikatu SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bde0-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="5bde0-109">To polecenie tworzy certyfikat SSL o nazwie Cert01 dla domyślnej bramy Application Gateway i zapisuje wynik w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="5bde0-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="5bde0-110">Przykład 2: Utwórz certyfikat SSL przy użyciu klucza tajnego magazynu kluczy (wersja-mniej secretId) i dodaj go do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5bde0-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="5bde0-111">Uzyskaj klucz tajny i Utwórz certyfikat SSL przy użyciu `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="5bde0-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="5bde0-112">Uwaga: w tym miejscu jest dostępna wersja — mniej secretId, Brama Application Gateway będzie synchronizować certyfikat w regularnych odstępach z działem.</span><span class="sxs-lookup"><span data-stu-id="5bde0-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="5bde0-113">Przykład 3: Utwórz certyfikat SSL przy użyciu klucza tajnego magazynu kluczy i dodaj go do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5bde0-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="5bde0-114">Uzyskaj klucz tajny i Utwórz certyfikat SSL przy użyciu `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="5bde0-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="5bde0-115">Uwaga: Jeśli aplikacja jest wymagana do synchronizowania certyfikatu z usługą Magazyn klucza, należy podać wersję — mniej secretId.</span><span class="sxs-lookup"><span data-stu-id="5bde0-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="5bde0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bde0-116">PARAMETERS</span></span>

### <span data-ttu-id="5bde0-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5bde0-117">-CertificateFile</span></span>
<span data-ttu-id="5bde0-118">Określa ścieżkę pliku PFX certyfikatu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bde0-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5bde0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bde0-119">-DefaultProfile</span></span>
<span data-ttu-id="5bde0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bde0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bde0-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="5bde0-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="5bde0-122">SecretId (identyfikator URI) klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bde0-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="5bde0-123">Użyj tej opcji, jeśli ma być używana określona wersja sekretu.</span><span class="sxs-lookup"><span data-stu-id="5bde0-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="5bde0-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5bde0-124">-Name</span></span>
<span data-ttu-id="5bde0-125">Określa nazwę certyfikatu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bde0-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5bde0-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="5bde0-126">-Password</span></span>
<span data-ttu-id="5bde0-127">Określa hasło protokołu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bde0-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5bde0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bde0-128">CommonParameters</span></span>
<span data-ttu-id="5bde0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bde0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bde0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bde0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bde0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bde0-131">INPUTS</span></span>

### <span data-ttu-id="5bde0-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5bde0-132">None</span></span>

## <span data-ttu-id="5bde0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bde0-133">OUTPUTS</span></span>

### <span data-ttu-id="5bde0-134">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bde0-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5bde0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bde0-135">NOTES</span></span>

## <span data-ttu-id="5bde0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bde0-136">RELATED LINKS</span></span>

[<span data-ttu-id="5bde0-137">Dodaj-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bde0-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5bde0-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bde0-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5bde0-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bde0-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5bde0-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bde0-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


