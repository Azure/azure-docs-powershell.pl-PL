---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/stop-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7018dc8d6951be8d1a08f4f1d1f5d615810dafab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898446"
---
# <span data-ttu-id="dc3b9-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="dc3b9-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="dc3b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3b9-103">Anuluje operację certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc3b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc3b9-104">SYNTAX</span></span>

```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc3b9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc3b9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3b9-106">Polecenie cmdlet **stop-AzureKeyVaultCertificateOperation** anuluje operację certyfikatu w usłudze Magazyn kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-106">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="dc3b9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc3b9-107">EXAMPLES</span></span>

### <span data-ttu-id="dc3b9-108">Przykład 1: anulowanie operacji na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="dc3b9-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="dc3b9-109">To polecenie anuluje operację certyfikatu TestCert02.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="dc3b9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc3b9-110">PARAMETERS</span></span>

### <span data-ttu-id="dc3b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3b9-111">-DefaultProfile</span></span>
<span data-ttu-id="dc3b9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dc3b9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dc3b9-113">-Force</span></span>
<span data-ttu-id="dc3b9-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc3b9-115">-Name</span></span>
<span data-ttu-id="dc3b9-116">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b9-117">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="dc3b9-117">-VaultName</span></span>
<span data-ttu-id="dc3b9-118">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-118">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b9-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc3b9-119">-Confirm</span></span>
<span data-ttu-id="dc3b9-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3b9-121">-WhatIf</span></span>
<span data-ttu-id="dc3b9-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3b9-123">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3b9-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3b9-125">CommonParameters</span></span>
<span data-ttu-id="dc3b9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3b9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3b9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3b9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc3b9-128">INPUTS</span></span>

## <span data-ttu-id="dc3b9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc3b9-129">OUTPUTS</span></span>

### <span data-ttu-id="dc3b9-130">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="dc3b9-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="dc3b9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc3b9-131">NOTES</span></span>

## <span data-ttu-id="dc3b9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc3b9-132">RELATED LINKS</span></span>

[<span data-ttu-id="dc3b9-133">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="dc3b9-133">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="dc3b9-134">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="dc3b9-134">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

