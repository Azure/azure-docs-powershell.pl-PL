---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489970"
---
# <span data-ttu-id="f447d-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f447d-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f447d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f447d-102">SYNOPSIS</span></span>
<span data-ttu-id="f447d-103">Dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f447d-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="f447d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f447d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f447d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f447d-105">DESCRIPTION</span></span>
<span data-ttu-id="f447d-106">Polecenie cmdlet **Add-AzApplicationGatewaySslCertificate** dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f447d-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="f447d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f447d-107">EXAMPLES</span></span>

### <span data-ttu-id="f447d-108">Przykład 1: Dodawanie certyfikatu SSL za pomocą PFX do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f447d-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="f447d-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01, a następnie dodaje do niej certyfikat SSL o nazwie Cert01.</span><span class="sxs-lookup"><span data-stu-id="f447d-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="f447d-110">Przykład 2: Dodaj certyfikat SSL przy użyciu klucza tajnego magazynu kluczy (wersja-minus secretId) do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f447d-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="f447d-111">Uzyskaj klucz tajny i odwołujesz się do niego w `Add-AzApplicationGatewaySslCertificate` celu dodania go do bramy aplikacji o nazwie `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="f447d-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="f447d-112">Uwaga: w tym miejscu jest dostępna wersja — mniej secretId, Brama Application Gateway będzie synchronizować certyfikat w regularnych odstępach z działem.</span><span class="sxs-lookup"><span data-stu-id="f447d-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="f447d-113">Przykład 3: Dodaj certyfikat SSL przy użyciu klucza tajnego magazynu kluczy (wersja z systemem secretId) do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f447d-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="f447d-114">Uzyskaj klucz tajny i odwołujesz się do niego w `Add-AzApplicationGatewaySslCertificate` celu dodania go do bramy aplikacji o nazwie `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="f447d-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="f447d-115">Uwaga: Jeśli aplikacja jest wymagana do synchronizowania certyfikatu z usługą Magazyn klucza, należy podać wersję — mniej secretId.</span><span class="sxs-lookup"><span data-stu-id="f447d-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="f447d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f447d-116">PARAMETERS</span></span>

### <span data-ttu-id="f447d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f447d-117">-ApplicationGateway</span></span>
<span data-ttu-id="f447d-118">Określa nazwę bramy aplikacji, z którą to polecenie cmdlet dodaje certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="f447d-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="f447d-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f447d-119">-CertificateFile</span></span>
<span data-ttu-id="f447d-120">Określa plik PFX certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f447d-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f447d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f447d-121">-DefaultProfile</span></span>
<span data-ttu-id="f447d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f447d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f447d-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="f447d-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="f447d-124">SecretId (identyfikator URI) klucza tajnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f447d-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="f447d-125">Użyj tej opcji, jeśli ma być używana określona wersja sekretu.</span><span class="sxs-lookup"><span data-stu-id="f447d-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="f447d-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f447d-126">-Name</span></span>
<span data-ttu-id="f447d-127">Określa nazwę certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f447d-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f447d-128">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f447d-128">-Password</span></span>
<span data-ttu-id="f447d-129">Określa hasło certyfikatu SSL, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f447d-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f447d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f447d-130">CommonParameters</span></span>
<span data-ttu-id="f447d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f447d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f447d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f447d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f447d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f447d-133">INPUTS</span></span>

### <span data-ttu-id="f447d-134">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f447d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f447d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f447d-135">OUTPUTS</span></span>

### <span data-ttu-id="f447d-136">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f447d-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f447d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f447d-137">NOTES</span></span>

## <span data-ttu-id="f447d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f447d-138">RELATED LINKS</span></span>

[<span data-ttu-id="f447d-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f447d-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f447d-140">Nowe — AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f447d-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f447d-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f447d-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f447d-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f447d-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


