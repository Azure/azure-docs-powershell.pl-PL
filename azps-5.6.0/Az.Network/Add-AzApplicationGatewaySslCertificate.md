---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 4dde5ab085dede4520b26a4fbeb3255cc62c0fe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982490"
---
# <span data-ttu-id="0628e-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0628e-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0628e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0628e-102">SYNOPSIS</span></span>
<span data-ttu-id="0628e-103">Dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0628e-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="0628e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0628e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0628e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0628e-105">DESCRIPTION</span></span>
<span data-ttu-id="0628e-106">Polecenie **cmdlet Add-AzApplicationGatewaySslCertificate** dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0628e-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="0628e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0628e-107">EXAMPLES</span></span>

### <span data-ttu-id="0628e-108">Przykład 1. Dodawanie certyfikatu SSL przy użyciu pfx do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0628e-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0628e-109">To polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, a następnie dodaje do niego certyfikat SSL o nazwie Cert01.</span><span class="sxs-lookup"><span data-stu-id="0628e-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="0628e-110">Przykład 2. Dodawanie certyfikatu SSL przy użyciu klucza KeyVault Secret (klucz tajny bez wersji) do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0628e-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0628e-111">Uzyskaj klucz tajny i odwołuj się do niego, aby dodać go do `Add-AzApplicationGatewaySslCertificate` bramy aplikacji z `Cert01` nazwą.</span><span class="sxs-lookup"><span data-stu-id="0628e-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="0628e-112">Uwaga: Jeśli w tym miejscu podano klucz secretId bez wersji, brama aplikacji będzie synchronizować certyfikat w regularnych odstępach czasu za pomocą klawisza KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0628e-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="0628e-113">Przykład 3. Dodawanie certyfikatu SSL przy użyciu klucza KeyVault Secret (versioned secretId) do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0628e-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0628e-114">Uzyskaj klucz tajny i odwołuj się do niego, aby dodać go do `Add-AzApplicationGatewaySslCertificate` bramy aplikacji z `Cert01` nazwą.</span><span class="sxs-lookup"><span data-stu-id="0628e-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="0628e-115">Uwaga: Jeśli wymagane jest zsynchronizowanie certyfikatu przez bramę aplikacji z kluczem KeyVault, podaj klucz secretId bez klucza wersji.</span><span class="sxs-lookup"><span data-stu-id="0628e-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="0628e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0628e-116">PARAMETERS</span></span>

### <span data-ttu-id="0628e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0628e-117">-ApplicationGateway</span></span>
<span data-ttu-id="0628e-118">Określa nazwę bramy aplikacji, do której to polecenie cmdlet dodaje certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="0628e-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="0628e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0628e-119">-CertificateFile</span></span>
<span data-ttu-id="0628e-120">Określa plik pfx certyfikatu SSL, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0628e-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0628e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0628e-121">-DefaultProfile</span></span>
<span data-ttu-id="0628e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0628e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0628e-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="0628e-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="0628e-124">SecretId (uri) klucza tajnego KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0628e-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="0628e-125">Użyj tej opcji, gdy trzeba użyć określonej wersji informacji tajnej.</span><span class="sxs-lookup"><span data-stu-id="0628e-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="0628e-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0628e-126">-Name</span></span>
<span data-ttu-id="0628e-127">Określa nazwę certyfikatu SSL, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0628e-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0628e-128">— Hasło</span><span class="sxs-lookup"><span data-stu-id="0628e-128">-Password</span></span>
<span data-ttu-id="0628e-129">Określa hasło certyfikatu SSL, które to polecenie cmdlet dodaje.</span><span class="sxs-lookup"><span data-stu-id="0628e-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0628e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0628e-130">CommonParameters</span></span>
<span data-ttu-id="0628e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0628e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0628e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0628e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0628e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0628e-133">INPUTS</span></span>

### <span data-ttu-id="0628e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0628e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0628e-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0628e-135">OUTPUTS</span></span>

### <span data-ttu-id="0628e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0628e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0628e-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0628e-137">NOTES</span></span>

## <span data-ttu-id="0628e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0628e-138">RELATED LINKS</span></span>

[<span data-ttu-id="0628e-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0628e-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0628e-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0628e-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0628e-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0628e-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0628e-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0628e-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


